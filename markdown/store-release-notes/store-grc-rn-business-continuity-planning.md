---
title: GRC: Business Continuity Planning release notes
description: Version history for the GRC: Business Continuity Planning on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-grc-rn-business-continuity-planning.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Governance, Risk, and Compliance release notes, ServiceNow Store release notes]
---

# GRC: Business Continuity Planning release notes

Version history for the GRC: Business Continuity Planning on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 11.0.2 - June 2026 \(Australia\)**
    -   New:
        -   New Feature - Gantt chart for plan
            -   Gantt chart view for Recovery tasks is now available. Users can view Recovery tasks in a Gantt chart timeline, select a start date for the view, and see planned durations directly on the timeline.
            -   Task reordering is now supported through insert.
            -   Quick edit and side panel editing for Recovery tasks. Users can now quickly edit Recovery tasks directly from the related list using a side panel, provided they have the appropriate access.
            -   Relative start and end times are automatically calculated for tasks.\*\* When dependencies or planned durations are updated, the system auto-calculates and updates the relative start and end times for each Recovery task.
            -   Gantt view now supports pagination. Users can load subsets of tasks, select page sizes \(10, 20, 50, 100\), and use "Show more" to load additional tasks.
        -   New Feature - Recovery Tasks for Plans
            -   Admins can create and manage recovery task template, recovery task template group ,loss scenarios and recovery strategies, including many-to-many relationships between recovery strategies, loss scenarios, plan templates, and recovery task template/template groups. UI actions allow adding task templates/template groups.
            -   Auto-add of recovery strategies and recovery tasks from plan templates. When creating a plan from a plan template, mandatory loss scenarios, recovery strategies, and recovery tasks are automatically created and linked.
            -   Automated addition of assets and dependencies.\*\* When assets are added to plan scope, they are automatically included in loss scenarios and dependencies are updated accordingly.
            -   UI actions for managing recovery task template, recovery task template groups. Users can add multiple recovery tasks to a template group or create recovery task templates directly from the UI.
    -   Changed: BCP expiration date logic has been enhanced. The expiration date is now automatically set to one year from approval, with support for user overrides and system property configuration.
-   **Version 10.0.2 - March 2026**

    Minor defect fixes.

-   **Version 9.1.2 - December 2025 \(Zurich\)**
    -   New:
        -   Cross plan task dependency
            -   Recovery tasks inside Business Continuity Plan \(BCP\) can now be linked to tasks from other plans, provided they belong to a direct parent plan. These will be carried across to event tasks.
            -   A new “Associated Plans” tab has been introduced to easily view and manage these cross-plan connections
        -   Phases
            -   Introduced phases to categorize tasks across different stages of a recovery event, such as Preparation, Recovery, Validation, and Return to Normal, for clearer progress visibility
            -   Shipped some out of box phases: Preparation, Recovery, Recovery Validation, Return to Normal, Return to Normal Validation, Post-incident review
        -   Asset recovery level
            -   A new option which allows users to mark impacted assets as Partially Recovered or Recovered upon task completion
        -   Include in Actual Crisis or Exercise
            -   Users can now specify whether a task should be included in an actual crisis or exercise scenario
        -   Exclude from Time Calculation
            -   A new option lets users mark tasks that should not be factored into overall time calculations
    -   Changed: Replaced "Related plan" and "Parent plan" tabs with "Associated Plan" tab in BCP record
-   **Version 9.0.1 - August 2025**
    -   New:
        -   Generate Word report using the template and the Report Generation API and UI actions with pop-up to select template
        -   Create Word template, data relationships, content configurations, setup manifest file and design word template for BCP
-   **Version 8.1.4 - July 2025**

    Fixed: Query match error for BCM planner persona while doing contains search.

-   **Version 8.1.3 - June 2025**

    Fixed: PDF generation is not working correctly when Hungarian characters are used.

-   **Version 8.1.1 - May 2025**
    -   Updated:
        -   Identified and fixed event mapping for UI action assignments
        -   Added progress bar for Update dependencies in BCP
    -   Fixed:
    -   -   Auto refresh doesn't save documentation when Update dependencies is clicked
-   Generated PDF doesn't have localized strings
-   **Version 8.0.2 - February 2025**
    -   Changed:
        -   Scope/related assets/asset dependencies should render the assets on the PDF for Planning
        -   Remove the related plans that are not associated with at least one task
    -   Fixed:
        -   onClick naming should be unique for UI actions created to the same form
        -   Added security data filters for data visualization and Gantt chart
-   **Version 7.1.2 - November 2024**
    -   Changed: Review sandbox access from client callable scripts
    -   Fixed:
        -   Security table ACL bypass issue
        -   RTO, RPO, recovery tier does not reset after update dependencies is clicked
        -   Removing a plan or related plan that activate another plan - it shows an error message but deletes the record
-   **Version 7.0.1 - August 2024**
    -   New:
        -   Added planned order and planned duration field for Plan tasks
        -   Added tag asset and asset scope field for recovery task
    -   Changed:
        -   Improved primary and related assets, shows relationships with hierarchical and list view
        -   Made BIA a reference field for Plan scope
        -   Removed cyclic dependencies for plan, to support planned order
    -   Fixed:
        -   BCM Plan PDF showing asset RTO/RPO as 'None' when they are not
        -   Before removing the related asset dependencies, it should check whether it is being used in Recovery strategies, tasks, etc.
        -   BCM Workspace Canvas Error​ - 414 URI Too Large
        -   "Do you want to save changes?" modal in Business Continuity Workspace &gt; Planning section was not saving changes when clicked
-   **Version 6.1.4 - July 2024**

    Fixed: Fixed app compatibility for the glide family releases.

-   **Version 6.1.3 - June 2024**
    -   Changed: Updated UIB workspace controller for BCM
    -   Fixed:
        -   Security fix for table/field ACL misconfiguration
        -   Security fix for Glide encoded query ACL bypass
        -   Refresh tab issue on the workspace
-   **Version 6.0.4 - February 2024**
    -   New:
        -   Added configuration to set manual or automated updates from CMDB or BIA
        -   Added dependency update support from CMDB and BIA in planning
        -   Added email notification for updates from CMDB and BIA
    -   Fixed:
        -   Fixed ad-hoc plan with start date time
        -   Fixed missing new button in the recovery strategy tab
        -   Fixed documentation section in PDF
        -   Fixed number of tasks in related plans
        -   Fixed related assets in BCP from BIA
        -   Fixed item picker UI, primary scope asset is not populated
-   **Version 5.0.2 - August 2023**
    -   New:
        -   Added planning in the new BCM Next Experience workspace
        -   Added pending plan activities in My Task
        -   Added a new homepage tab for planning
        -   Added a new overview page with a stepper component for states
        -   Added planning modules in the List view
        -   Added new UI page for Scope tab in BCP
        -   Added new UI page for Documentation tab in BCP
    -   Fixed: Recovery task to use BIA and manually added related plans
-   **Version 4.1.0 - May 2023**
    -   Fixed:
        -   Lookup reference drop-down fields in BCP. Will support system property for displaying the number of items in the drop-down.
        -   Fixed BCP business rule that's throwing Java error
        -   Fixed documentation 404 error when uploading an image
-   **Version 4.0.1 - February 2023**
    -   Fixed:
        -   BCM admin is unable to see a chart of dependencies from cmdb\_datacenter.
        -   Inside the BCM workspace, a grouping of recovery tasks does not work &amp; when the 'Refresh list' is clicked no task gets displayed.
        -   Performance issue, BCM - Adding a plan with 15000 tasks to an event is being canceled due to transaction quota rules.
        -   Security Bug
        -   Approval and Approval history tabs are not enabled in the workspace view - Plans and Events.
        -   BCP tab, related assets are not pulled in automatically.
-   **Version 3.0.4 - December 2022**

    Fixed: Fixed parent POM in order to remove the redundant GLIDE-INF folder and content contained within.

-   **Version 3.0.2 - August 2022**
    -   New:
        -   For BCM event scoping changes, create the related assets and related plans in the plan form
        -   For BCM event scoping changes, open the dependencies field in the recovery tasks to accommodate the tasks irrespective of the scope
        -   For BCM event scoping changes, create the dependencies and pre-requisite UI in the plan form
        -   For BCM event scoping changes, categorize tasks - Pre-requisites, tasks, and check
    -   Fixed:
        -   Fixed security gaps for HTML injections
        -   Copy plan is failed when the recovery strategy doe not have dependencies covered
        -   Plan ADD UI action brings the scope and related assets to Rome but this is not working on SD onwards
-   **Version 2.3.1 - March 2022**
    -   New:
        -   Ability to copy plan.
        -   Ability to delete plan document sections and edit section title and subtitle.
        -   Enabled multi-language support and included translations.
    -   Changed: Subheading/section description in the plan documentation, which was fetched from the documentation template is now copied to the plan and can be edited.
-   **Version 2.2.2 - November 2021**
    -   New:
        -   Ability to set up multiple levels of approvers and route plans for approval
        -   Ability to define dependencies among plan recovery tasks
        -   Ability to group and report plan recovery tasks
        -   Plan document sections are ordered according to plan templates
    -   Changed:
        -   Lifecycle UI action behavior is modified to accommodate approval flow
        -   Plan is set as read-only in Pending approval, Approved and Archived states
        -   Plan PDF template layout
-   **Version 2.1.1 - June 2021**
    -   New: Support to add related assets to loss scenarios based on BIA dependencies
    -   Fixed: Minor fixes in PDF generation
-   **Version 2.0.1 - March 2021**
    -   New:
        -   Support for different plan authoring types
        -   Ability to link BIA to plan asset/scope
        -   Define recovery tasks at plan/recovery strategy/documentation
        -   Recovery tasks can be assigned to recovery teams
    -   Changed:
        -   Plan assets are now defined under 'scope' tab of the plan
        -   Support to define plan authoring type in plan templates
-   **Version 1.0.2 - October 2020**
    -   New:
        -   All new user experience for Business Continuity and Disaster Recovery Planning
        -   Streamlined integration with ServiceNow CMDB for business processes and asset inventories
        -   Role-based workspace with customizable reports and dashboards

**Parent Topic:**[ServiceNow Store - Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-grc.md)

