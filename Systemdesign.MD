# System Architecture for Certificate Management Solution with SSO Integration

This architecture is designed for a scalable and secure certificate management solution on AWS, supporting **auto-renewal**, **SSO integration via OIDC**, and **certificate storage and delivery** to agents.

---

## 1. Architecture Overview

The architecture is divided into three main components:

- **Authentication and Access Control**: Manages user authentication with SSO integration and token-based access control.
- **Core Certificate Management Services**: Handles certificate lifecycle management, renewal, and compliance verification.
- **Data Storage and Notification Services**: Manages certificate storage, metadata, and notifications for administrators.

---


# Complete Architecture Diagram for Certificate Management System with Agent Authentication Outside

```mermaid
graph TD
    %% External Actors
    subgraph "External (Customer Environment)"
        User[User - Web Console] -->|Login and Manage Certificates| Cognito[Okta or AWS Cognito]
        User -->|Access Web Console| WebConsole[Web Console]
  
        Agent[Agent on Customer Server] -->|Authenticate with Cognito and Obtain Token| Cognito
        Agent -->|Poll for Certificate Updates with Token| APIGateway[API Gateway]
        Agent -->|Receive Certificate and Status| ClientSystem[Client System for Certificate Installation]
    end

    %% AWS Components for Authentication and Access Control
    subgraph "Authentication and Access Control (AWS)"
        Cognito -->|OIDC/OAuth Token Issuance| APIGateway
        APIGateway -->|Token Validation, mTLS, & Secure Routing| CertificateService[ECS/EKS - Certificate Management Service]
    end

    %% Core Certificate Management Services in AWS
    subgraph "Core Certificate Management Services (AWS)"
        CertificateService -->|Access Metadata| Postgres[PostgreSQL - Certificate Metadata]
        CertificateService -->|Store/Retrieve Certificates| S3Bucket[S3 - Certificate Storage]
        CertificateService -->|Queue Renewal Requests| SQSQueue[SQS - Renewal Queue]
    end

    %% Certificate Renewal Processing in AWS
    subgraph "Certificate Renewal Processing (AWS)"
        SQSQueue -->|Process Queue| RenewalProcessor[ECS/EKS - Renewal Processor]
        RenewalProcessor -->|Request CA Renewal| CAService[ECS/EKS - CA Integration Service]
        CAService -->|Store Renewed Cert| S3Bucket
    end

    %% Notifications and Monitoring in AWS
    subgraph "Notifications and Monitoring (AWS)"
        APIGateway -->|Log API Access| CloudWatch[CloudWatch - Logs and Alarms]
        RenewalProcessor -->|Notify on Events| SNS[SNS - Notifications]
        CAService -->|Log Renewal Processing| CloudWatch
    end

    %% IAM Access Policies for Security
    APIGateway -->|Access Policies via IAM| IAM[AWS IAM]
```


**Route Separation** : Within API Gateway, we will define separate routes (e.g., `/agent/*` and `/console/*`) for the Agent and Web Console APIs This separation allows you to apply different access controls, monitoring configurations depending on the actor making the request. We will also apply `mTLS` agent related apis
