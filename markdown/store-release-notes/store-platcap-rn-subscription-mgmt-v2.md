---
title: Subscription Management v2 release notes
description: Version history for the Subscription Management v2 application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-subscription-mgmt-v2.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 5
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# Subscription Management v2 release notes

Version history for the Subscription Management v2 application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 6.4.3 - June 2026**

    Version update for backend only, with no customer-facing changes.

-   **Version 6.1.4 - June 2026**

    Version update for backend only, with no customer-facing changes.

-   **Version 6.4.1 - May 2026**

    Version update for backend only, with no customer-facing changes.

-   **Version 6.1.3 - May 2026**

    Version update for backend only, with no customer-facing changes.

-   **Version 6.4.0 - April 2026**

    Version update for backend only, with no customer-facing changes.

-   **Version 6.1.1 - March 2026**
    -   New: Monitor and track Workflow Data Fabric capability usage with visibility into tokens use rates by capability
    -   Changed:
        -   Now Assists usage resets automatically on contract anniversary dates and draws from a fixed annual pool. Unused assists do not roll over.
        -   To streamline subscription allocation, the manual user-based allocation workflow has been removed for administrators who never used it. Administrators who have used the manual workflow still retain access to it.
        -   Allocation details for user-based products are now hidden from the overview section to prevent misinterpretation of status when allocations are incomplete. For questions about per-user product usage, please contact your Account Executive.
-   **Version 6.0.2 - January 2026**
    -   Changed:
        -   Now Assist consumption will move from a rolling 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. With this change, usage will show the assists that have been used so far in the contract year, instead of always displaying a trailing 365-day view.
        -   KB article with detailed explanation of usage calculations added to the Now Assist Usage dashboard
-   **Version 6.0.0 - December 2025**
    -   Changed:
        -   Now Assist Usage
            -   Demonstration instances are now excluded from the total Assist usage count to help ensure accurate reporting of assists consumption.
            -   Introduced a new accrual time field to display when Now Assist data was last accrued, helping customers assess data recency across instances.
        -   User-Based Products
            -   Allocation details for user-based products are now hidden from the overview section to prevent misinterpretation of status when allocations are incomplete. For questions about per-user product usage, please contact your Account Executive.
-   **Version 5.1.0 - August 2025**
    -   New in this release
        -   Now Assists by domain name for instances with domain separation enabled
        -   Monitor Workflow Data Fabric capability usage and view the token use rate of each capability
-   **Version 5.0.6 - July 2025**
    -   New in this release:
        -   Manage Custom Application and Table mapping via platform
            -   Map any missing custom applications and tables in Subscription Management to a subscription directly from the Custom Applications list or the Custom Table Inventory list.
        -   Domain separation for user-based subscriptions
            -   Subscription Management now allows users to view subscribers by domain for user-based subscriptions.
    -   Fixed: High-priority performance fixes
-   **Version 5.0.6 - July 2025**
    -   New in this release:
        -   Manage Custom Application and Table mapping via platform
            -   Map any missing custom applications and tables in Subscription Management to a subscription directly from the Custom Applications list or the Custom Table Inventory list.
        -   Domain separation for user-based subscriptions
            -   Subscription Management now allows users to view subscribers by domain for user-based subscriptions.
    -   Fixed: High-priority performance fixes
-   **Version 5.0.0 - May 2025**
    -   New in this release:
        -   Manage Custom Application and Table mapping via platformMap any missing custom applications and tables in Subscription Management to a subscription directly from the Custom Applications list or the Custom Table Inventory list.
        -   Domain separation for user-based subscriptionsSubscription Management now allows users to view subscribers by domain for user-based subscriptions.
-   **Version 4.2.0 - February 2025**
    -   New in this release:
        -   Subscription allocation counts according to active users View the total number of active users in a product subscription. Only active users count toward the subscription allocation totals that appear throughout Subscription Management.
        -   Allocate subscriptions to all recommended groups Select all recommended groups when allocating subscriptions.
        -   Support for on-premise installation Manage subscription usage using Subscription Management on-premise.
        -   Recommended subscription reasoning Determine why a subscription is recommended by Subscription Management when mapping custom tables or custom applications.
    -   Changed in this release:
        -   Allocation charts reflect only active users The Allocation summary and Allocation history charts on the subscription details page reflect only subscriptions allocated to active users for each month following the upgrade.
        -   Auditing App Engine V1 usage The App Engine Usage dashboard has been restored.
    -   Removed in this release: The Custom tables chart has been removed from the subscription details page.
-   **Version 4.1.0 - November 2024**
    -   New in the release:
        -   Subscription allocation counts according to active users - View the total number of active users in a product subscription. Only active users count toward the subscription allocation totals that appear throughout Subscription Management.
    -   Changed in this release:
        -   Allocation charts reflect only active users -The Allocation summary and Allocation history charts on the subscription details page reflect only subscriptions allocated to active users for each month following the upgrade.
        -   Removed in this release:
        -   The Custom Tables chart has been removed from the subscription details page.
-   **Version 3.3.1 - November 2024**
    -   New:
        -   Monitor Now Assist usage
            -   View an account-level summary of your Now Assist entitlements and track Now Assist usage across all your instances.
        -   Monitor Now Assist creators
            -   View an account-level summary of your Creator Plus entitlements and track allocations across all your instances.
    -   Fixed: Licensing entitlement engine bug fixes only.
-   **Version 4.0.0 - August 2024**
    -   New: Monitor cloud capacity
        -   View an account-level summary of your cloud capacity and track usage across all your instances.
-   **Version 3.2.1 - August 2024**
    -   New:
        -   Monitor Now Assist usage
            -   View an account-level summary of your Now Assist entitlements and track Now Assist usage across all your instances.
        -   Monitor Now Assist creators
            -   View an account-level summary of your Creator Plus entitlements and track allocations across all your instances.
    -   Fixed: Performance improvements
-   **Version 3.1.0 - June 2024**
    -   New:
        -   Monitor Now Assist usage: View an account-level summary of your Now Assist entitlements and track Now Assist usage across all your instances
        -   Monitor Now Assist creators: View an account-level summary of your Creator Plus entitlements and track allocations across all your instances
    -   Fixed: Performance improvements
-   **Version 2.1.0 - June 2024**

    Fixed: Performance improvements.

-   **Version 3.0.0 - May 2024**
    -   New:
        -   Monitor Now Assist usage
            -   View an account-level summary of your Now Assist entitlements and track Now Assist usage across all your instances.
        -   Monitor Now Assist creators
            -   View an account-level summary of your Creator Plus entitlements and track allocations across all your instances.
-   **Version 2.3.1 - March 2024**
    -   Fixed:
        -   Minor system updates
        -   Performance improvements
        -   Fixed a bug related to license role detection and recommendations
-   **Version 2.3.0 - February 2024**

    Subscription Management gives you visibility and control of your subscriptions in an enhanced user interface that prioritizes actionable data and provides an easy way to allocate subscriptions using recommended groups. Use Subscription Management to get a real‑time view of allocation and entitlement usage with reports showing your usage over time. Monitor your subscriptions to stay within compliance and make informed decisions about your subscription usage and purchases.


**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

