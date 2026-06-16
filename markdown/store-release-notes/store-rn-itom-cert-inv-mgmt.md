---
title: Certificate Inventory and Management release notes
description: Version history for the IT Operations Management Certificate Inventory and Management app on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-cert-inv-mgmt.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - ITOM Visibility release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Certificate Inventory and Management release notes

Version history for the IT Operations Management Certificate Inventory and Management app on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.2.0 - June 2026**
    -   New:
        -   Integration with CyberArk Certificate Manager SaaSManage certificates by using the certificate management capabilities of CyberArk Certificate Manager SaaS while maintaining centralized visibility and control through ServiceNow Certificate Inventory and Management.
        -   Integration with Azure Key VaultStore your private keys in Azure Key Vault during automated certificate operations by selecting Azure Key Vault as an external vault provider when setting up routing policies.This feature is supported starting with the Brazil release.
        -   Integration with Microsoft TeamsGet certificate notifications and start renewal workflows directly from Microsoft Teams channels.
        -   Manage certificate notifications from a centralized formView and manage all email and Microsoft Teams certificate notifications from the Certificate notification policy form. This form enables you to configure which events trigger email notifications and specify recipients for each event type.
        -   Access Service Catalog forms for certificate request, renewal, and revocation processes from the Certificate Management workspace.
    -   Fixed:
        -   Fixed an issue where CIs in the installed certificate table showed empty Name values.
        -   Retired certificates no longer generate renewal tasks.
        -   Fixed an issue where the issuer and root\_issuer fields were both set to the same intermediate certificate in a certificate chain, causing inconsistent issuer selection.
-   **Version 4.0.1 - March 2026**
    -   New:
        -   Introducing seamless certificate renewal via Microsoft Outlook – streamline TLS certificate renewals by handling approvals and updates directly within your existing email workflow, reducing friction and missed expirations.
        -   Introducing CMDB Data Certification for TLS certificates – ensure accurate certificate ownership and accountability by validating and certifying ownership data directly in your CMDB, improving compliance and audit readiness.
    -   Fixed:
        -   Unique certificate records are updated from the Retired state to the Install state when a certificate is re-discovered again.
        -   New private key format \(PKCS8\) is now supported in Certificate management credentials.
        -   Fixed vulnerabilities found in the external issuer image.
        -   Fixed routing policy workflow failure on CSR details mismatch.
-   **Version 3.14.0 - December 2025**
    -   Fixed:
        -   Corrected decoding of IPV6 IP address from CSR
        -   Multiple security bug fixes
-   **Version 3.12.0 - September 2025**
    -   Automating manual tasks like requesting a new certificate and renewing expired certificates can increase the productivity of the public-key infrastructure \(PKI\) team by ~30% and help to digitize manual workflows.
    -   The TLS Certificate management store application provides a platform-based approach to the lifecycle management of TLS certificates. This solution combined with task fulfillment can provide a methodical approach to the request management and renewal management process.
-   **Version 3.8.2 - August 2025**
    -   New:
        -   Added archiving rules for unique certificates and their associated records.
        -   TLS Certificate request automated flow now supports EJBCA with ACME.
        -   Added the ability to discover root certificates stored off-site and connect them to the certificate chain.
    -   Fixed:
        -   Domain ID is resetting in 'Discovery Certificate Captured' and 'Discovery Device Complete' script actions.
        -   No longer creating tasks for Retired Certificates Discovered by the "Amazon AWS - Certificates Manager" pattern
        -   Resolved discrepancies in the root issuer name
        -   Polling job implemented for Microsoft CA Manual Approval flow
        -   Other less significant issues have also been addressed in this version
-   **Version 3.6.3 - July 2025**
    -   New:
        -   The outdated CIM Dashboard's image has been updated to match the Coral UI theme, improving visual consistency and user experience
        -   Improvements in the certificate notification job.
            -   Introduced two new system properties to limit the notification for expired certificates:
                -   sn\_disco\_certmgmt.most\_recent\_discovery\_days\_considered\_to\_create\_renewal\_task: The number of days is considered for querying expired certificates to create a renewal task based on their Most Recent Discovery date, with a default value of 7 days
                -   sn\_disco\_certmgmt.valid\_to\_days\_considered\_to\_create\_renewal\_task: If the last\_discovered field is empty, this property is used to check if the certificate expired within the past 7 days \(or the value of the property\)
-   **Version 3.6.0 - November 2024**
    -   New: CSR Generation can now be generated on the ServiceNow instance itself \(supported only on Y+ instances\).
    -   Fixed:
        -   Resolved: Certificate Management Flow is not working as expected with Secure Mode Mid
        -   Resolved: Issues with the certificate valid to and from dates.
        -   Resolved: "DigiCert - Certificate Management" pattern setting invalid value "none" to service\_type field
        -   Resolved: \[Upgrade from Vancouver/Washington to itommerge\] Amazon AWS - Certificates Manager pattern is failing with error after AWS Cloud Discovery
        -   Resolved: If SAN in CSR is an IP Address, it is being converted to hexadecimal in the form's "Subject Alternative Name" field.
        -   Resolved: Certificate inventory and management - Microsoft CA new certificates have inconsistent new line control characters.
-   **Version 3.4.0 - May 2024**
    -   New:
        -   Populate all the attributes of the imported certificates using IRE.
        -   ACME support for multiple Certificate authorities, and validating the automated certificate renewals
        -   Cloud certificate discovery patterns have been integrated directly into the Certificate Inventory Management application, keeping these patterns housed within the app.
        -   Discovering certificates from AWS, Azure, and GCP certificate managers and populating the cmdb\_ci\_certificate.
        -   the app reconciles the certificates discovered with IP/Port scanner with certificate discovered from Cert Manager CA Pattern
    -   Fixed:
        -   "Multiple CAs on Host" error still observed during Microsoft CA certificate request
        -   DigiCert - New Certificate automation flow is not getting certificate id in response
        -   DigiCert - Certificate Management pattern - expired certificates are discovered with state 'issued'
        -   In related lists, Certificates are sorted based on nonexistent field 'valid\_upto', instead of the expected 'valid\_to' field
        -   Path attribute unecesarilly added for sn\_disco\_certmgmt\_cmdb\_installed\_certificate
        -   When parsing certificate subject-names allow spaces in between attributes of the certificate
        -   Application Servers table \(cmdb\_ci\_app\_server\) does not allow user to distinguish between the records in the table when the 'Request New Certificate \(Automated\)' catalog request is submitted
-   **Version 3.3.0 - November 2023**
    -   Changed: Accessibility WCAG 2.1
    -   Fixed:
        -   Rectified Certificate Authority Discovery Payload populating special Characters for subject\_organization field
        -   app-itom-external-issuer helm chart can be deployed using --namespace tag
-   **Version 3.1.0 - August 2023**

    What's New:

    Certificate management workspace: Explore the brand-new workspace experience.

    - Certificate Inventory Dashboard and Insights.

    - PKI Workflow Insights.

    - Certificate lifecycle management views.

    Support cert-manager integration.

    cert-manager adds certificates and certificate issuers as resource types in Kubernetes clusters and simplifies the process of obtaining, renewing, and using those certificates.

-   **Version 3.0.6 - June 2023**

    Fixed: Decryption bug fixes.

-   **Version 3.0.0 - May 2023**
    -   Fixed:
        -   Minor bug fixes
        -   Added support for multiple Microsoft CAs on same host.
        -   Added support for using intermediate server instead of CA server for Microsoft CA.
-   **Version 2.4.0 - February 2023**

    Minor fixes.

-   **Version 2.3.2 - November 2022**

    What's New:

    -   Automation of certificate fulfillment for Microsoft Active Directory Certificate Services
    -   Employee Center experience for Certificate request, renewal, and revoke operations
    -   Visibility to Certificate chain from Unique certificate form view
-   **Version 2.1.0 - May 2022**

    New: Entrust CA Policy Automation for certificate request, renewal, and revoke operations.

-   **Version 1.3.19 - March 2022**
    -   Fixed:
        -   Save UI action was missing in context menu in sysapproval\_approver record.
        -   Warning message or alert in the "Disable CellEdit - State Field" client script appeared when user tried to change the state from approval list view.
-   **Version 1.5.0 - February 2022**
    -   This is a patch release for Certificate Inventory and Management 1.3.8. This 1.5.0 patch release is compatible with the San Diego family release.
    -   Fixed:
        -   "Disable CellEdit - State Field" client script was blocking users from updating values from the "Approval" table list view. This has been removed.
        -   Discovery issues for ECC Algorithm signed certificates for Entrust.
        -   Subject Alternative Name was not getting recognized while decoding CSR if the Subject Alternative Name had X509v3 format.
        -   In the Manual Renew Certificate Service Catalog Form, the Certificate Expiration Date was not converting to local time.
        -   Save UI action was missing in the context menu for sysapproval\_approver record.
        -   Removed the overridden UI actions and added a new UI action “Choose Routing Policy &amp; Approve.”
        -   Earlier Certificates with single certificate in chain were marked as self-signed. Control this behavior by setting the \[sn\_disco\_certmgmt.mark\_self\_signed\_for\_incomplete\_chain\] property. If the property is set to true \(default\), the certificate with incomplete chain is marked as self-signed.
-   **Version 1.3.8 - September 2021**
    -   New:
        -   Service Catalog workflows for users to request, renew and revoke digital certificates.
        -   Policy-based routing framework for PKI administrators to configure the request fulfillment process flows for Digicert Certificate Authority
-   **Version 1.2.1 - August 2020**

    Changed: Added ITOM visibility subscription as a dependency.

-   **Version 1.1.7 - February 2020**
    -   New:
        -   Discovery of TLS Certs from Certificate Authority Vendors - Support discovery TLS certificates from Digicert and GoDaddy Certificate Authority \(CA\). The discovery logic will use the existing pattern framework to discovery/inventory certificates from Digicert and GoDaddy CA.
        -   Bulk import of TLS certs from MID Server - Certificates can be imported from files. You can discover certificates from certificate files by importing the files into the system using pattern-based Discovery. You can only import 1500 certificates at one time.
    -   Fixed: Minor bug fixes
-   **Version 1.0.6 - January 2020**

    The TLS Certificate management store application provides a platform-based approach to the lifecycle management of TLS certificates. This solution combined with task fulfillment can provide a methodical approach to the request management and renewal management process. Automating manual tasks like requesting a new certificate and renewing expired certificates can increase the productivity of the public-key Infrastructure \(PKI\) team by ~30% and help to digitize their manual workflows.


**Parent Topic:**[ServiceNow Store - ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-visibility-landing.md)

