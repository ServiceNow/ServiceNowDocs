---
title: Goal Framework for SPM release notes
description: Version history for the Goal Framework for SPM on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-goal-framework-spm.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Goal Framework for SPM release notes

Version history for the Goal Framework for SPM on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.8.0 - June 2026**

    Changed: Updated platform directives for Cobalt Raven ACLs and scoping bypass.

-   **Version 2.7.0 - March 2026**
    -   New:
        -   Added anAssigned Entity field for Targets, enabling association of targets with an organizational entity.
        -   Added aCancelled state option for Goals and Targets.
        -   Updated reference fields to display only active Strategic Plans and Strategic Priorities.
-   **Version 2.6.0 - December 2025**
    -   Changed: Users with the sn\_gf\_goal\_admin role can update system properties specific to Goals.
    -   Fixed: Fixed value of target's actuals when target automation is enabled for PA indicator target source.
-   **Version 2.5.0 - August 2025**
    -   Changed:
        -   Goals marked inactive will not be displayed in the Goals list when searched for in the Primary goal/Parent goal reference fields.
        -   Goals can now be associated with product model, valuestream, strategic program and initiative from their respective reference fields in the Goals list view.
-   **Version 2.4.1 - May 2025**

    Fixed: The Check-in due date is not updated when the Actual value in a breakdown is cleared.

-   **Version 2.4.0 - February 2025**
    -   Fixed:
        -   Actual value consistency when target distribution is changed from cumulative to non-cumulative.
        -   Support of negative numbers in target actuals to display in the progress tab of the target.
        -   Actuals handling on moving target start date to a future date.
-   **Version 2.3.0 - November 2024**
    -   New:
        -   Ability to have daily, weekly, and monthly breakdowns of targets apart from quarterly and yearly.
        -   The Progress tab in the target side panel displays a graphical visualization of the target's progress over the target's duration.
        -   Ability to easily enter or update actuals for the target through the side panel and cell context menu.
        -   Ability to view historical updates of target actuals.
        -   Activity stream is enabled in the Target and Goals full details record page.
        -   Target distribution dropdown to provide cumulative/noncumulative target value distribution over the time period.
        -   Ability to extend targets without any loss of data.
    -   Changed:
        -   The Breakdown interval field has been removed and target breakdown creation is driven only by the Check-in frequency field.
        -   Migration job \(Migrate Breakdown Interval To Checkin frequency\) to enable upgrade customers for a seamless transition from breakdown interval to check-in frequency.
        -   Ability to modify the unit of measure, start value, final target value, check-in frequency, and target value distribution without any data loss.
    -   Removed: The Breakdown interval and Cumulative target fields are deprecated.
-   **Version 2.2.3 - August 2024**
    -   Fixed:
        -   The Primary target field in the planning item gets updated when target field is updated in the existing record in the Goal/Target Relationship related list.
        -   The Target value of the yearly breakdown \(for target type minimize\) displays yearly target value.
-   **Version 2.2.2 - June 2024**

    Fixed: Defect fix to manage scope issues for ppm entities such as demand and project.

-   **Version 2.2.0 - May 2024**
    -   New:
        -   Ability to associate work or planning items to either targets or goals.
        -   The Target field has been added to the Goal/Target Relationship \(m:m\) table to support an association of a target with work.
        -   The Primary target field has been added to all planning item tables to support an association of a target with planning item.
        -   Auto-populate the Primary goal when the Primary target field is populated for a work or planning item.
    -   Changed:
        -   The Goals Relationship \(m:m\) table has been renamed to Goal/Target Relationship.
        -   The Primary goal field has been renamed to Primary on the Goal/Target Relationship table.
        -   The "Actual Value Source Configuration" section has been renamed to "Target Automation". Also, the Automate actual value option has been moved to the Target Automation section on the Target form.
        -   The default value for the Cumulative target field has been changed to true on the Target form. The Target value is cumulatively distributed across the quarters for cumulative targets.
    -   Fixed: Contributors of the target can edit target breakdowns and actual values.
-   **Version 2.1.0 - November 2023**

    New:

    -   Ability to manage targets cumulatively over quarterly or yearly intervals.
    -   Added the sn\_gfa.target\_breakdown\_decimals system property to set the desired number of decimals to be visible on the target breakdown values.
    -   Added the sn\_apw\_advanced.spw\_goal\_user\_read role to Business Stakeholder \[business\_stakeholder\] users, so that they can access the Goals page within Strategic Planning Workspace, by default.
-   **Version 2.0.0 - August 2023**

    New:

    -   Ability to set quarterly intervals/breakdowns for long-term targets to easily update and manage the targets.
    -   Ability to add remarks to capture the highlights for the actual value update.
-   **Version 4.1.2 - June 2023**

    Fixed: Addressed internal build quality issues.

-   **Version 1.1.1 - May 2023**

    Internal mandate related to ACLs.

-   **Version 1.1.0 - February 2023**

    Goal Framework for SPM \(Strategic Portfolio Management\), formerly known as Advanced Goal Framework, empowers leaders to better track how work contributes to strategy and monitor goal progress in real-time by enabling target actuals to be collected and aggregated automatically within the ServiceNow AI Platform.


