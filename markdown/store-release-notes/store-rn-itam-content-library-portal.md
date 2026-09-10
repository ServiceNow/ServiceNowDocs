---
title: Content Library Portal release notes
description: Version history for the ITAM Content Library Portal application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itam-content-library-portal.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - IT Asset Management version history release notes, ServiceNow Store version history release notes]
---

# Content Library Portal release notes

Version history for the ITAM Content Library Portal application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.2.2 - September 2026**
    -   New:
        -   Automatic suite license inference: Enable automatic suite inference to calculate the optimal suite license for each software installation based on your actual footprint and entitlements. This feature reduces manual configuration required for the suite on the software model and improves compliance reporting.
        -   Deduplication rules: Choose how closely versions must match before two installs on the same device count as duplicates, on per product level.
        -   Deduplication transparency: Each install now shows which deduplication rule was applied and which install was kept as the active one.
        -   Tiered and volume-based license metrics: Onboard and reconcile entitlements that are sold in tiers or in packs, such as those from IBM and VMware.
    -   Changed:
        -   More accurate duplicate detection: Duplicates are now detected within a single discovery source as well as across sources, and language differences no longer prevent a match. This clears up inflated install counts, such as those caused by Microsoft 365 language packs. The new behavior is applied to your existing installs after you upgrade.
        -   Better choice of active install: When duplicates are found, the most complete and most recent record is kept as the active one. The discovery source no longer influences the choice.
        -   More accurate suite licensing: Related products such as Core Infrastructure Server, Windows Server, and System Center are now considered together during licensing. This avoids licensing the same hardware twice and makes better use of the licenses you already own.
        -   Less noise in product results: Suite Components that cannot be licensed on their own, such as Microsoft SQL Server Analysis Services, now roll up to their suite instead of appearing as separate product results.
-   **Version 4.1.1 - July 2026 \(Australia\)**

    Minor fixes around the product lifecycle during Content updates and content lookup historical data

-   **Version 4.0.4 - July 2026 \(Zurich\)**

    Minor fixes around the product lifecycle during Content updates and content lookup historical data

-   **Version 4.1.0 - March 2026 \(Australia\)**

    Added telemetry definitions.

-   **Version 4.0.3 - September 2025**

    In V4.0.3, Populate historical data for line charts and bar charts automatically.

-   **Version 4.0.2 - August 2025**
    -   New content dashboard is introduced with visibility features to quickly assess the coverage of critical data-points within the Content Library. It provides insights into the availability and growth of data elements across Content Library releases, enabling better expectation management and more informed decision-making.
    -   Users can view aggregated counts of key data-points, including Software \(Publishers, Products, Versions, Lifecycle Records, PPN\) and Hardware \(Manufacturers, Products, Models, Lifecycle Records\).
    -   Bar chart widgets display software data point counts across content versions, with clickable charts that open a new tab showing pre-filtered detailed views for the selected content version.
    -   AI Search results appear in a dynamic tab with card-based display, featuring separate sub-tabs for software \(Publishers, Products, DMAPs, Lifecycles, PPN\) and hardware \(Manufacturers, Products, Models, Lifecycles\) data points, showing filtered counts and relevant fields per category, with a back button to return to the landing page.
-   **Version 3.1.0 - August 2024**

    Migrate pages under 'Content Lookup' tab to layout 3.0.

-   **Version 3.0.1 - November 2023**

    UI improvements when zooming in.

-   **Version 2.0.0 - August 2022**

    New: AI powered search for Hardware Asset Management content.

-   **Version 1.0.1 - December 2021**

    The Content lookup portal gives you visibility into the IT Assets related data stored in the IT Asset Management Content Service via an intuitive user interface.


**Parent Topic:**[ServiceNow Store - IT Asset Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itam-highlight.md)

