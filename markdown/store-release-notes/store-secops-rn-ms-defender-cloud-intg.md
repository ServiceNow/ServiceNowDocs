---
title: Microsoft Defender for Cloud Integration for Security Operations release notes
description: Version history for the Microsoft Defender for Cloud Integration for Security Operations application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-ms-defender-cloud-intg.html
release: store
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Vulnerability Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Microsoft Defender for Cloud Integration for Security Operations release notes

Version history for the Microsoft Defender for Cloud Integration for Security Operations application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.8.0 - December 2025**

    Fixed: Minor fixes.

-   **Version 2.7.3 - June 2025**

    Fixed: To address an error that was occurring with skiptoken, the integration uses the nextLink parameter for pagination requests.

-   **Version 2.7.0 - November 2024**

    Fixed: After completion of an ASC integration that brings in Azure cloud resources, cloud resource type of the Assets are mapped to right cloud resource types.

-   **Version 2.6.0 - August 2024**

    Improvements to support test group population in the Configuration Tests table for Microsoft Defender for Cloud Integration for Security Operations.

-   **Version 2.5.2 - May 2024**

    Fixed: Permissive roles for third-party integrations. The role is now restricted so that the administrator of the corresponding integration has the ability to configure the integration.

-   **Version 2.4.2 - August 2023 \(Vancouver\)**

    New:

    -   On running the integrations, the Last Pass field will be populated on the test results.
    -   Introduced the comprehensive integration for the Microsoft Defender for Cloud Integration to update the last seen of the test result with the current date for the unhealthy test results.
-   **Version 2.3.0 - February 2023**

    Changed: Framework updates to use 'Security Support Common' common code instead of Vulnerability Response.


