---
title: Impact Health Content release notes
description: Version history for the ServiceNow Impact Health Content application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-impact-health-content.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Impact version history release notes, ServiceNow Store version history release notes]
---

# Impact Health Content release notes

Version history for the ServiceNow® Impact Health Content application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.0.3 - September 2026**
    -   New: As part of the ongoing modernization of Platform Health content, 244 Scan Engine definitions have been introduced, including migrated Health Assessment content and new platform health definitions. These definitions include a combination of system property validations, statistical analysis checks, conditional rule evaluations, and custom script-based assessments, expanding coverage across platform health, governance, and configuration standards.
        -   150 definitions are global and apply to all customer instances.
        -   94 definitions are associated with specific ServiceNow applications or plugins and are evaluated only when the corresponding application is installed and active.
-   **Version 5.0.2 - August 2026**

    Fixed: Corrected sn\_SE10422 to prevent false-positive findings when Policy Actions share the same variable and order across different Catalog Items. The definition now validates the parent Catalog Item before generating a finding.

-   **Version 4.0.3 - July 2026**
    -   Changed: sn\_SE10061 – Enhanced the Catalog UI Policy Action definition to evaluate the Value action and Field message type fields, improving validation coverage.
    -   Fixed:
        -   sn\_SE10292 – Fixed an issue where the definition could block the creation of records in the Number column and generate incorrect findings during update set scans.
        -   sn\_SE10513 – Fixed an issue where the definition could incorrectly block the creation of Scheduled Imports and Data Sources.
-   **Version 3.0.3 - June 2026**

    Fixed definition behaviour for sn\_SE10096 during update set scans.

-   **Version 2.1.1 - April 2026**
    -   Fixed:
        -   Updated definition behavior for sn\_SE10418, sn\_SE10302,sn\_SE10249
        -   Updated definition behavior for sn\_SE10545, sn\_SE10575, sn\_SE10281, sn\_SE10468
        -   Updated short descriptions for sn\_SE10083, sn\_SE10064, sn\_SE10639
    -   Removed: Deactivated outdated or unused definitions: sn\_SE10173, sn\_SE10305, sn\_SE10287, sn\_SE10476
-   **Version 2.0.2 - March 2026**
    -   Changed:
        -   Added applicable table conditions so the definition runs only where relevant \(sn\_SE10561\).
        -   Improved definition prefix consistency \(Definition Prefix fix\) to keep definition naming/behaviour consistent.
        -   Enhanced definition behaviour for sn\_SE10439 to improve results quality.
    -   Fixed:
        -   Fixed definition behaviour for sn\_SE10203.
        -   Fixed definition behaviour for sn\_SE10545.
    -   Removed: Deactivated outdated/unused definitions: sn\_SE10626, sn\_SE10261, sn\_SE10558, sn\_SE10174, sn\_SE10582, sn\_SE10492
-   **Version 1.1.1 - February 2026**
    -   Fixed:
        -   Improved accuracy of few definitions to reduce false positives.
        -   Corrected internal definition naming inconsistencies to improve stability and consistency across scans.
-   **Version 1.0.3 - December 2025**

    The Impact Health Content App is a ServiceNow application that provides a comprehensive library of Scan Engine \(SE\) definitions for instance health monitoring. This app extends ServiceNow's Scan Engine functionality by delivering pre-configured health check rules that help administrators identify security misconfigurations, performance issues, manageability concerns, and configuration recommended practices across their ServiceNow instances.


**Parent Topic:**[ServiceNow Store - Impact version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-impact-highlight.md)

