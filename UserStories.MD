# User Story

## 1. Dashbord

### User Story #1: User managment

**As an** administrator, **I want** to manage users within the certificate management system **so that** I can control access levels and ensure secure and organized account management.

* **Acceptance Criteria** : Administrators can add, edit, and remove users, assign roles to control access, and reset passwords. Role-based access ensures users have the right permissions, and activity logs track actions for accountability.

### User Story #2: Overview of Certificates

**As an** IT administrator, **I want** to see an overview of all SSL/TLS certificates in a centralized dashboard **so that** I can monitor their status and ensure timely renewals.

* **Acceptance Criteria** :
  * Dashboard displays a list of certificates with key details: name, status (active, expiring, expired), expiration date, and associated application/service.
  * Certificates are sorted by expiration date by default, with filters for status, application, and environment (e.g., production, staging).
  * Expiring certificates are highlighted to indicate priority.
  * Clicking on a certificate opens a detailed view displaying metadata (e.g., issuer, domain, validity period, encryption strength).
  * View includes history of renewals and past status changes (active, expired).
  * Role based visibility

### User Story #3: Search and Filter Functionality

**As an** IT administrator, **I want** to search for certificates by status, expiration date, application, or associated environment **so that** I can quickly locate certificates that need attention.

* **Acceptance Criteria** :
* Search bar allows searching by certificate name, domain, or application.
* Filters for certificate status (active, expiring, expired), environment, application, and issuer.
* Ability to combine filters and sort results (e.g., all expiring certificates in production, sorted by expiration date).

## 2. Import Certficate

**User Story #1** : As an  **IT administrator** , I want to import existing SSL/TLS certificates from external sources so I can centrally manage them within the certificate management tool.

* **Acceptance Criteria** :
  * Users can upload certificates in various formats (e.g., PEM, PFX).
  * Option to upload private keys and CA bundles with certificates.
  * Validation of certificate format, expiration, and private key compatibility.
  * Confirmation message upon successful import.

 **User Story #2** : As a  **network security officer** , I want to verify that all imported certificates meet organizational security standards, ensuring that all certificates are compliant with company policies.

* **Acceptance Criteria** :
  * Certificates are validated against predefined security standards (e.g., encryption strength, expiration threshold).
  * Detailed error messages for failed imports due to policy violations.

## 3. **Auto Renewal**

 **User Story #1** : As a  **system administrator** , I want to enable auto-renewal for certificates to ensure uninterrupted security and avoid certificate expirations that could cause outages.

* **Acceptance Criteria** :
  * Option to enable/disable auto-renewal for each certificate.
  * Renewal is attempted X days before expiration if enabled.
  * A notification is sent upon successful or failed auto-renewal attempts.

## **4. Agentic Approach to Install Certificate**

**User Story #1** : As a  **DevOps engineer** , I want an agent on each server to check for updates to SSL/TLS certificates and pull newly renewed certificates automatically, ensuring the server always has an updated certificate without manual intervention.

* **Acceptance Criteria** :
  * Configurable agent installed on each server that checks for new certificates based on set intervals or triggers.
  * Agents can securely pull renewed certificates when available.
  * Real-time status updates for each server indicating certificate pull status.

## 5. Payment

 **User Story #1** : As a  **billing manager** , I want to purchase certificates and enable automated payments for renewals, so we have a streamlined and uninterrupted payment experience.

* **Acceptance Criteria** :
  * Secure checkout for certificate purchases with multiple payment methods (credit card, bank transfer, digital wallet).
  * Option to save payment details for future use and auto-renewal charges.
  * Notifications for successful payments and failed transactions.

## 6. Notification

### User Story #1: Notifications for Expiring Certificates

**As a** DevOps engineer, **I want** to see alerts on the dashboard for certificates that are approaching expiration **so that** I can take action to renew them before they expire.

* **Acceptance Criteria** :
  * Certificates expiring within 30, 15, or 7 days are flagged with notifications or color-coded indicators.
  * Users can click on an alert to view details about the certificate and renewal options.
  * Alerts are customizable, allowing users to set reminder thresholds (e.g., 45 days before expiration).

## 7. SSO Integration
