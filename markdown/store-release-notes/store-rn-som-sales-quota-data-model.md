---
title: Sales Quota Data Model release notes
description: Version history for the Sales Quota Data Model application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-som-sales-quota-data-model.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Sales Customer Relationship Management version history release notes, ServiceNow Store version history release notes]
---

# Sales Quota Data Model release notes

Version history for the Sales Quota Data Model application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 1.2.4 - September 2026**
    1.  Upgraded @servicenow/sdkfrom ^4.8.1to a pinned 4.9.3and added --emitDictionary=falseto the ci:buildcommand to resolve build failures. Version bumped 1.2.2 → 1.2.3, target bundle retargeted to 2026 Sept.
    2.  Removed stale old-format sys\_choicecomposite keys for sn\_quota\_core\_sales\_quota.type\(individual, rollup\) from keys.tsand regenerated them in the SDK 4.9.3 5-field format. Under SDK 4.9.3 the stale entries were marked deleted:true, generating DELETE XMLs that would have removed legitimate choice values on deployment.
    3.  Merged project/2026augustinto September to carry forward prior fixes.
    4.  Updated ArchiveSalesQuotaITarchival rule tests to use the synchronous API and removed the obsolete SalesQuotaArchiveRuleTest.jsscenarios
-   **Version 1.2.2 - August 2026**

    Fluent based development support added.

-   **Version 1.2.1 - July 2026**

    Added OOB query range support via new SA-based ACLs for the Quota bundle.

-   **Version 1.2.0 - April 2026**

    New: Quota support for product offering family.

-   **Version 1.1.0 - December 2025**

    New: Support for Quota creation for territory based hierarchies.

-   **Version 1.0.0 - May 2025**

    This application enables users to manage sales quotas. It includes the sales quota Data Model and the ability to create and manage sales quota records.


