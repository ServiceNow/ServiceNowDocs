---
title: Vendor Management Workspace release notes
description: Version history for the Vendor Management Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itsm-vendor-mgmt.html
release: store
topic_type: reference
last_updated: "2024-11-07"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - IT Service Management release notes, ServiceNow Store release notes]
---

# Vendor Management Workspace release notes

Version history for the Vendor Management Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.5.0 - November 2024**
    -   Fixed:
        -   Fix for ACL Hardening Phase 2 \(2024\)
        -   Addaria-label to now-text-link in the "Vendor Performance" table
        -   Align the pagination control of the "Vendor Performance" table to the bottom
        -   Add l10n support to sn-par-visualization-base on the landing page
-   **Version 3.4.2 - August 2024**

    Changed: KPI groups on vendor management workspace used to display legacy indicators. Legacy indicators have been replaced with the current set of indicators based on the new tables with a 'VMW:' prefix.

-   **Version 3.3.0 - February 2024**
    -   New: Migrate page layout to 3.0
    -   Fixed: ACL bugs
-   **Version 3.1.3 - September 2023**
    -   Fixed:
        -   Change in date range should reflect on all the KPI related pages.
        -   Minor issues related to KPI groups
-   **Version 3.2.0 - August 2023**
    -   -   New:
    -   Localization
    -   PO integration
-   Fixed: Display Vendor KPIs in the KPI Group order
-   **Version 3.1.2 - May 2023**
    -   New:
        -   Add "Vendor Satisfaction", "Vendor Requested Items" and "Manual SLA from External Source" indicators into "Harware" and "Software" KPI Groups
        -   Create "Vendor Properties" page for all vendor related sys propertiesAdding Vendor Admin role to view the vendor properties
        -   Upgrade snc-app-parent@5.0.0.98
    -   Changed:
        -   Hide sidebar in the vendor page since the plugin is optional
        -   Integrate app-optimize-kpi-group-details-common
    -   Fixed:
        -   Fix "Performance" page doesn't load the first timeGrid doesn't show empty value when there is no data for selected dates\(present date\).
        -   Fix Vendor Score opened in KPI breakdown details page doesn't show the Single Score, Time series graph
        -   Fix Vendor scores in the list module doesn't have new configuration changes
        -   Fix missing 'report\_view' ACLs on all tables
        -   Fix Vendor Satisfaction score is not available for vendors
        -   Fix Scores Grid under vendor score breakdowns should be clickable
    -   Removed:
        -   Remove dependency of Service Owner Workspace
        -   Remove dependency of Success Indicator
-   **Version 3.1.0 - February 2023**

    Minor fixes.

-   **Version 3.0.3 - December 2022**

    Changed: updated release version

-   **Version 3.0.0 - August 2022**

    Fixed: minor bug fixes

-   **Version 2.1.1 - June 2022 \(San Diego\)**
    -   Changed:
        -   The Vendor Manager Workspace \(Legacy\) \(com.snc.vlm.vmw\) plugin is planned for deprecation in the San Diego release.
        -   The Vendor Management Workspace \(com.snc.sn\_itsm\_vendor\) plugin is available as a separate subscription.
-   **Version 1.0.6 - June 2022 \(Rome\)**
    -   Changed:
        -   The name Vendor Manager Workspace has been changed to Vendor Manager Workspace \(legacy\)
        -   The app-itsm-vendor has been renamed to Vendor Management Workspace and uses the com.snc.sn\_itsm\_vendor plugin
        -   The above changes were backported to Rome and San Diego
-   **Version 2.0.2 - February 2022**

    New: Vendor Management Workspace has a new, modernized look and feel.

-   **Version 1.0.3 - September 2021**

    The Vendor Management Workspace allows vendor managers to holistically view and manage risk and performance data for all of the vendors they manage. The product works with Continual Improvement Management to create and track initiatives for vendor improvement. Vendor Management also integrates with Performance Analytics to provide unprecedented visibility into vendor performance.


