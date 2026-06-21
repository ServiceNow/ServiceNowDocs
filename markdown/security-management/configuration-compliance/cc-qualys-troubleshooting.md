---
title: Resolving Qualys Vulnerability Integration issues
description: Some commonly encountered issues, along with workarounds are discussed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/security-management/configuration-compliance/cc-qualys-troubleshooting.html
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Qualys, Configuration Compliance integrations, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Resolving Qualys Vulnerability Integration issues

Some commonly encountered issues, along with workarounds are discussed.

-   **[Attachments not appearing after import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/configuration-compliance/cc-attachments-not-appearing.md)**  
If attachments are not appearing as expected for data sources or on a security incident after third-party integration imports, check your IP restrictions.
-   **[Modify transform maps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/configuration-compliance/cc-t-ChangeTransformMaps.md)**  
Transform maps are provided with base configurations and are sufficient usually. You can modify transform mappings depending on the needs of your organization.
-   **[Check XML attachment property size](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/configuration-compliance/cc-check-xml-prop-size.md)**  
Verifies that the XML attachment property is sufficient for large files.
-   **[Data retrieval limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/configuration-compliance/cc-limit-data-retrieved.md)**  
By default, there are no restrictions on how data is retrieved from Qualys. Many records can be related to low severity vulnerabilities that a customer is not willing to remediate using their vulnerability response process. Updating the corresponding REST message/method parameters can modify this behavior.
-   **[Qualys Knowledge Base Integration is failing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/configuration-compliance/cc-qualys-kb-integration-failure.md)**  
Resolve Qualys Knowledge Base Integration failure by reducing the payload attachment size received from Qualys to the specified limit.

**Parent Topic:**[Qualys integration with Configuration Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/security-management/configuration-compliance/Qualys-cc-Integration.md)

