---
title: External Credential Storage and Management Application release notes
description: Version history for the External Credential Storage and Management Application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-external-credential-storage-mgmt-app.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# External Credential Storage and Management Application release notes

Version history for the External Credential Storage and Management Application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.3.1 - December 2025**

    New: Added  REST API integration option for CyberArk CCP alongside existing AIM SDK to provide more flexible deployment choices with reduced dependency footprint.

-   **Version 1.1.1 - May 2025**

    New: Added support for certificate-based authentication when connecting to Azure Key Vault. This provides a more secure and flexible way to authenticate, especially for enterprise environments that prefer certificate credentials over client secrets.

-   **Version 1.0.2 - August 2024**

    External Credential Storage and Management brings out of the box integrations to external credential storage solutions to store credentials in an external repository rather than directly in a ServiceNow credentials record. The instance maintains a unique identifier for each credential, the credential type \(such as SSH, SNMP, or Windows\), and any credential affinities. The MID Server obtains the credential identifier from the instance, and then uses the resolver to retrieve the identifier from the repository into a usable credential.


