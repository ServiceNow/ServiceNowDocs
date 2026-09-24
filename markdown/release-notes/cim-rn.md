---
title: Certificate Inventory and Management release notes
description: The ServiceNow Certificate Inventory and Management application discovers, inventories, and manages the life cycle of TLS certificates across your infrastructure. See the following sections for release notes by version.The 4.4.0 release extends automated certificate management to DigiCert ACME, Sectigo Universal ACME, Sectigo Public ACME, and custom ACME-compatible certificate authorities \(CAs\), and supports CyberArk PVWA for private key storage and DER and PKCS12 certificate formats.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/cim-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Certificate Inventory and Management, CIM, TLS, Certificate discovery, Certificate renewal, Certificate authority, 4.4.0]
breadcrumb: [ITOM Visibility release notes, IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Certificate Inventory and Management release notes

The ServiceNow® Certificate Inventory and Management application discovers, inventories, and manages the life cycle of TLS certificates across your infrastructure. See the following sections for release notes by version.

## About Certificate Inventory and Management

-   Maintain a centralized inventory of TLS certificates discovered through port scans, URL scans, certificate authorities, cloud providers, file imports, and bulk upload.
-   Prevent outages by tracking expiration dates and notifying certificate owners through email, Microsoft Teams, and Slack before certificates expire.
-   Automate certificate requests, renewals, and revocations through routing policies that connect to your certificate authorities and external vaults.

See [Certificate Inventory and Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/cert-inventory-mgmt.md) for more information.

## Activation requirements

-   **Activation information**

    Install Certificate Inventory and Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[ITOM Visibility release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itom-visibility-rn.md)

## Version 4.4.0

The 4.4.0 release extends automated certificate management to DigiCert ACME, Sectigo Universal ACME, Sectigo Public ACME, and custom ACME-compatible certificate authorities \(CAs\), and supports CyberArk PVWA for private key storage and DER and PKCS12 certificate formats.

### What's new

-   **[Extended ACME capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/exploring-acme.md)**

    Request, renew, and revoke certificates through DigiCert ACME, Sectigo Universal ACME, and Sectigo Public ACME CAs using automated flows. If your organization uses a different CA that is compatible with the ACME protocol, you can add it and use it to extend automated certificate management to that CA.

-   **[CyberArk PVWA private key storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/configure-mid-server-automatic-cert-renewal.md)**

    Store private keys in CyberArk PVWA during automated certificate operations, in addition to HashiCorp Vault and Azure Key Vault.

-   **[Certificate format support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/certificate-routing-policy-field-values.md)**

    Receive issued certificates in DER binary or PKCS12 format, instead of PEM format.


