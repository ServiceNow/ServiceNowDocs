---
title: Sales Forecasting release notes
description: Version history for the Sales Forecasting application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-som-sales-forecasting.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Sales Customer Relationship Management version history release notes, ServiceNow Store version history release notes]
---

# Sales Forecasting release notes

Version history for the Sales Forecasting application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.4.1 - September 2026**
    -   Fixed:
        -   Eased restrictions on forecast update, submission and adjustment blockade. Users can perform ioperations on ndependent period and territory while forecast update is ongoing
        -   Teams can customize the filters applied to forecast report views to match their own reporting needs.
        -   If a forecast operation is rejected due to restrictions, a clear and decisive error message is displayed.
        -   The forecast owner is no longer automatically overwritten when the period changes, giving users predictable control over ownership.
-   **Version 4.3.0 - August 2026**
    -   New:
        -   Reopen &amp; Resubmit Forecast Submissions — reopen a completed submission within the same forecast window, edit values,  resubmit; configurable per forecast model with a full audit trail.
        -   Configurable Columns on Forecast Dashboards — show/hide columns and sub-columns, with preferences saved per forecast model.
    -   Changed:
        -   Forecast submissions can be completed independently of the manager's submission state.
        -   Draft submissions automatically include newly added forecast items.
        -   Forecast item reference is now retained on submitted items after a submission is completed.
    -   Fixed:
        -   Users can enter forecast numbers for periods that have no underlying opportunity.
        -   Resolved a forecast calculation crash on cumulative rollup when the source record has an empty owner.
        -   Submitted items appear in the list view immediately after a new submission \(no manual refresh\).
        -   Quota now populates on Sales Team rollup headers when the batch threshold is reduced.
-   **Version 4.2.1 - July 2026**

    Added OOB query range support via new SA-based ACLs for Sales Forecasting Application

-   **Version 4.1.0 - June 2026**

    New: This release includes fixes for known issues to improve stability and reliability. No new features or enhancements have been introduced.

-   **Version 4.0.5 - May 2026**

    Changed: This release includes fixes for known issues to improve stability and reliability. No new features or enhancements have been introduced.

-   **Version 4.0.0 - April 2026**
    -   New:
        -   Support for Product Hierarchy /Product Family Based Forecasting as a secondary dimension
        -   Support for Enabling Forecasting at Base Forecast Object
-   **Version 3.0.1 - March 2026**
    -   New:
        -   Support for multiple forecast models
        -   Support for configurable forecast configuration
        -   Support for on-demand forecast calculation
        -   Support for weekly/monthly multi-period forecast submissions
-   **Version 2.0.0 - December 2025**
    -   New:
        -   Enable sales representatives to submit their forecasts.
        -   Enable sales managers to make adjustments to their forecasts.
        -   Enable sales leaders to view &amp; make their adjustments to the hierarchy forecasts across their sales team hierarchy.
-   **Version 1.1.0 - August 2025**

    New changes in this release: Performance improvements along with accessibility improvements.

-   **Version 1.0.0 - May 2025**

    Sales forecast measures pipeline health to estimate future sales volumes and revenue for a business over a specified period of time.


**Parent Topic:**[ServiceNow Store - Sales Customer Relationship Management version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-sales-order-management-highlights.md)

