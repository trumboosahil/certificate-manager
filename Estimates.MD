# Estimates

## Dashboard Feature Estimates

| **Feature**                         | **Key Components**                                                                                                                                                                                                                                                                                                                                                          | **UI + UX** | **Backend (BE) + Database (DB)** | **QA** | **Deployment** | **Total**     |
| ----------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------- | -------------------------------------- | ------------ | -------------------- | ------------------- |
| **User Management**                 | - Add new users and send setup invitation emails.<br />  - Modify user details and roles; apply changes immediately.<br />  - Securely remove users, retain activity logs. <br />  - Define roles (admin, viewer, operator) with specific permissions. <br />  - Admin-initiated password reset with secure email link. <br />  - Track and export user actions for audits.  | 1.5 weeks         | 4 weeks                                | 1 week       | 0.5 week             | **7 weeks**   |
| **Overview of Certificates**        | - Show certificate details (name, status, expiration date, etc.).<br /> - Sort by expiration, status, or application; filter by specific attributes.<br /> - Visual flags for certificates near expiration. <br /> - In-depth view with metadata, renewal history, and compliance status. <br /> - Role-specific permissions for view/edit. <br /> - Dynamic status refresh. | 2 weeks           | 5 weeks                                | 1 week       | 0.5 week             | **8.5 weeks** |
| **Search and Filter**               | - Search by certificate name, domain, or application.<br />  - Filter by status, environment, application, and issuer.<br />  - Apply multiple filters and sort by expiration or other fields. <br />  - Backend optimization and database indexing for efficient querying.                                                                                                   | 0.5 week          | 2.5 weeks                              | 0.5 week     | 0.5 week             | **4 weeks**   |
| **Expiring Certificates Highlight** | - Configure visual indicators for certificates expiring in 30, 15, or 7 days.<br /> - Users can adjust threshold levels for receiving alerts.<br /> - Highlights visible directly in the certificate overview for quick identification.                                                                                                                                         | 0.5 week          | 1.5 weeks                              | 0.5 week     | 0.5 week             | **3 weeks**   |
| **Detailed Certificate View**       | - Show details like issuer, validity period, encryption strength.<br />- View past renewals and changes in status.<br /> - Compliance indicators to check if certificates meet policy standards (e.g., encryption level).                                                                                                                                                         | 1 week            | 2 weeks                                | 0.5 week     | 0.5 week             | **4 weeks**   |
| **Role-Based Visibility**           | - Define permissions per role (admin, viewer, operator).<br /> - Limit certificate view and edit rights to authorized roles.<br /> - Multi-tenant setup to restrict data per customer organization.                                                                                                                                                                             | 0.5 week          | 1.5 weeks                              | 0.5 week     | 0.5 week             | **3 weeks**   |
| **Certificate Creation**            | - Form to input certificate details (e.g., name, expiration, application).<br /> - Specify production, staging, or testing environment.<br /> - Only authorized roles can create certificates. <br /> - Ensure new certificates are scoped to the correct tenant for SaaS setup.                                                                                               | 1 week            | 2.5 weeks                              | 0.5 week     | 0.5 week             | **4.5 weeks** |
| **Certificate Update**              | - Update fields like expiration date, application, or environment.<br /> - Restrict edit permissions to authorized roles.<br />  - Ensure updates are tenant-specific for secure multi-tenant environments.                                                                                                                                                                     | 0.5 week          | 1.5 weeks                              | 0.5 week     | 0.5 week             | **3 weeks**   |
| **Certificate Deletion**            | - Allow authorized roles to remove certificates.<br /> - Keep deletion records for compliance and audit purposes.                                                                                                                                                                                                                                                                | 0.5 week          | 1.5 weeks                              | 0.5 week     | 0.5 week             | **3 weeks**   |

## Import Certficate

Summary for Import Certificate Feature

| Task                         | Estimated Time         |
| ---------------------------- | ---------------------- |
| UI Design and Development    | 1-2 weeks              |
| Backend Development          | 3-4 weeks              |
| Agent Development            | 1 week (if applicable) |
| QA Testing                   | 1-2 weeks              |
| Scalability and Optimization | 1 week                 |

### Additional Notes

* **Security** : This feature involves careful handling of certificates and private keys, compliance checks, and security considerations, which require rigorous development and testing.
* **Integration** : If additional integrations with external sources are needed (e.g., specific CAs), those may add to the timeline.
* **Future Scalability** : The solution should be designed to handle a high volume of imports in a secure, efficient manner to meet enterprise needs.

## Renewal

Final Timeline Summary for Auto-Renewal Feature

| Task                         | Estimated Time |
| ---------------------------- | -------------- |
| UI Design and Development    | 1-2 weeks      |
| Backend Development          | 3-4 weeks      |
| Agent Development            | 3-4 weeks      |
| QA Testing                   | 2-3 weeks      |
| Scalability and Optimization | 1-2 weeks      |
