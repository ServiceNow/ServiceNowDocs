---
title: Common Plugin for SecOps SIEM integration release notes
description: Version history for the Common Plugin for SecOps SIEM integration on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-common-plugin-siem-integrations.html
release: store
topic_type: reference
last_updated: "2025-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Common Plugin for SecOps SIEM integration release notes

Version history for the Common Plugin for SecOps SIEM integration on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.14 - September 2025**

    Fixed: Fixed the reference field matching in domain separation environment.

-   **Version 11.0.13 - November 2023**
    -   Changed: Updated jQuery UI libraries to the latest version.
    -   Fixed: Accessibility issues in security mapping fields on the Profile page.
-   **Version 11.0.11 - May 2023**

    Fixed: \[Localization - Hardcoded String\] - Missing $\{""key""\} call in &lt;sn\_event\_ingestion&gt; fix.

-   **Version 11.0.9 - September 2022**

    Changed: Performance fix.

-   **Version 11.0.8 - May 2022**

    Fixed: When there is a Business Rule on Observable/CI, and task M2M records which update the SIR fields automatically. This occurs since SIR was not persisted at the creation time using SIEM, and the SIR fields are not getting updated. This issue has been fixed, and now SIR would persist first in DB, and then the M2M records are created.

-   **Version 11.0.6 - March 2022**
    -   Changed: Updated AngularJS library version.
    -   Fixed: Fixed Breadcrumb tabs functionality while saving the profile.
-   **Version 11.0.5 - December 2021**

    Fixed: UI fixes.

-   **Version 11.0.4 - May 2021**

    Changed: Moved the RCA \(Restricted Caller Access\) records to the correct target scope.


**Parent Topic:**[ServiceNow Store - Security Incident Response release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/sn-store-rn-secops-sir.md)

