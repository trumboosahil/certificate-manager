**Tool to manage SSL\TLS certs

# SAAS Based certficate manager

Customer portal

* BackOffice Dashboard: Provides a single point for complete visibility and control over all the certificates being issued\used by various organizations. Having adequate filters like company wise, cert type, environments, etc to have the proper view.
* GUI and Api support for Certificate creation: Robust GUI for the customers to create and manage certificate, Api’s to do the same actions which can be automated for managing certs lifecycle.
* Access control and security: Implementing Role base access control and security features like 2FA, access token and ddos protection is essential to keep the application running in a healthy way.
* Analytics and metrics: To provide customers with a better view of how their certificates are being used, etc.
* Auto-installation of certficates at server

## Customer portal

### Create certficate/ Import

### Maintain Expiry

### **Renewal and Auto-Renewal** :

* **Manual Renewal** : Offer users the option to manually renew certificates as they approach expiration.
* **Auto-Renewal** : Integrate with third-party APIs (e.g., Let's Encrypt or other Certificate Authorities) to support automatic certificate renewals. Open-source options may be leveraged to handle the auto-renewal functionality at scale.

### Notification

### Agent approach for installation and certaficate renewal

Create an agent-based solution for customers who need certificates to be automatically installed on their servers. The agent can be deployed on servers to install and periodically renew certificates directly.

### Payment processing

Integrate payment processing for a subscription model, allowing customers to pay for the platform and potentially for add-on features like premium support or additional certificate types.

## Admin Dashboard

The admin dashboard is a backend management panel for administrators and support teams to manage and support customer accounts.

* **Visibility and Control** :
  * A single point of control to view and manage all customer accounts and certificates across different organizations. The admin dashboard would include detailed filtering options to drill down by company, certificate type, environment (e.g., dev, test, staging, production), and other relevant criteria.
* **Customer Support Tools** :
  * Provide the same capabilities as the customer portal, allowing admins to troubleshoot customer issues, renew certificates on behalf of customers, and adjust settings when needed.

## Other non priority features :

1. Multiple environment support :  within the organization there can be multiple environments like dev, test, staging and production. The tool should support creating and managing or the different environments certificates.
2. Additional Security features : Compliance certifications like PCI DSS and GDPR can build up trust among marketing.
3. Robust support channel : Providing 24/7 dedicated support and help customers troubleshoot, integrating popular communication channels like whatsapp can add value in the offering.

![](https://lh7-qw.googleusercontent.com/docsz/AD_4nXdNi68mbESaKeLji82FqYi6Q2482q9ix5qA8YaFIwU-SQJBeTckSiB4TUxVTkjiBzQa09yvromXQ31gx8-d4NjdyK5gvhXfux3fcTGTDcmysVrwYIuRmdHbcPqUtd3lPM34jipRqYiyXPOUuxQ8ZsN78nmY?key=SqB5g-wMQhF7uwZyMNd0vpgl)

![](https://lh7-qw.googleusercontent.com/docsz/AD_4nXfxYcHn1Ud54N_JnZuahPnw9fSl1bU_xvzd1IUwfGKmm9fRFzfSeI1fQKf38_MCfaZrs1oRijqYsmeEcQU2M7SHz5J2sCYDLDNdZ4IBsRGBY4IRnaBVYsHH4WQJnMGPyRmH0h2Ew4wuHi4pNsHKcENAznRf?key=SqB5g-wMQhF7uwZyMNd0vpgl)

**