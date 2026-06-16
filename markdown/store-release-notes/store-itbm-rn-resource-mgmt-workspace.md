---
title: Resource Management Workspace release notes
description: Version history for the Resource Management Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-resource-mgmt-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Resource Management Workspace release notes

Version history for the Resource Management Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 5.7.0 - June 2026**
    -   Features:
        -   Copy a Resource Assignment
        -   Efforts are now redistributed on extending  or reducing the resource assignment.
        -   Edit the efforts for resource assignments with Actual values captured.
        -   Smarter schedule selection for unassigned assignment's Heatmaps.
        -   Resource Finder UI updates.
    -   Fixes:
        -   Performance improvements.
        -   Workspace loading and navigation.
        -   Form and inline-edit behavior.
        -   Move/CPAAM data integrity.
        -   Allocation-fetch pagination edge case.
    -   Removed: Resource Finder dependency.
-   **Version 5.5.0 - May 2026**
    -   New:
        -   Resource Finder enables Project Managers and Resource Managers to quickly identify and assign the best-fit resource to an unassigned Resource Assignment directly from the Project Workspace \(PWS\) or Resource Management Workspace \(RMW\). Launched from the "Find Resource" context menu on an unassigned RA, the modal is automatically scoped to the assignment's date range and primary planning attributes \(such as role\), and surfaces candidate resources alongside their availability in the workspace's configured units \(FTE/PD/Hours, Monthly/Weekly\). When the AI skill is enabled, resources are ranked with a fit score and AI-generated rationale, with availability accessible via a toggle; when AI is disabled, availability is shown by default. From the results, Resource Managers can apply manual filters, view a requested-effort comparison with capacity indicators and select resources to seamlessly transition into the existing Assign modal flow.
    -   Fixed: In the Resource Management Workspace, the default assignment method in the Assign Work modal has been changed from "Assign resources automatically" to "Assign resources manually," giving Resource Managers direct control over resource selection by default.
-   **Version 5.4.2 - April 2026**
    -   Fixed:
        -   Improved performance while assigning assignments to users. Faster assignment creation for long-duration and multi-user allocations.
        -   Field-level editable ACLs are honored in Resource Management Workspace by evaluating permissions at the row level using the current record context. This ensures ACL conditions based on record values \(for example, restricting edits when the status is Approved\) are correctly honored.
-   **Version 5.4.0 - March 2026**
    -   New: Resource assignment fields can now be used as rate model entities, with parent assignments using their own rate lines and child assignments following their respective rate lines.
    -   Fixed:
        -   Resource assignments migrated from Demands without dates will load correctly in Resource Management Workspace.
        -   Renaming a Resource Card automatically updates the card name in the breadcrumb navigation path within the Resource Management Workspace.
        -   Fixed a JavaScript to slightly increase assign flow and ensured proper handling of leftover hours during distribution.
-   **Version 5.3.0 - December 2025**
    -   New:
        -   Realign option to adjust resource assignment dates to honour the change in dates a planning item.
        -   Ability to update Resource Rate field for resource assignments directly from the top-tray of resource cards.
        -   Filter top tray in resource cards.
        -   Ability to choose effort distribution during the assign flow.
        -   Support for granular admin role changes
    -   Changed:
        -   Enabled copying of work notes for all operations like assign, unassign, and reassign in the RM workspace.
        -   Added an information message to update effort from the resource cards view.
        -   Added assignment date validation in the Move modal.
        -   Allow overallocation when extending a resource assignment.
        -   Display an error message when assignment dates are updated outside the task duration.
        -   Display error messages when editing attributes on assignments that have actuals
        -   Display an error message when a user attempts to move an assignment with actuals populated.
    -   Fixed:
        -   Fixed an issue where field-level ACLs were not applied to editable fields in the Resource Management workspace
        -   Resolved an issue where Assignment\_type was not copied to the new assignment during a split operation in RM workspace
        -   Additional filters in the Resource Board creation modal were not functioning correctly when the board type was set to Worktype
        -   Employee profile dates are not honored during reassignment operation in the RM workspace
        -   Honor group-level average daily FTE and custom schedules when heatmap values are updated in the RM workspace
        -   Fixed an issue when switching to FTE view with Group By enabled in the top grid of the RM workspace
        -   Not considered user preference for language when displaying resource status values
        -   Unable to edit resource rate for user type resource assignment
        -   Corrected inaccurate data displayed in the allocation modal for traditional resource plans
        -   Fixed an issue where Group and Role fields were set toundefined when updated from the bottom tray
        -   Unable to perform unassign operation on the resource assignments created on demand
        -   Fixed an issue where the bottom grid did not refresh when moving an unassigned resource assignment in the RM workspace
-   **Version 5.2.0 - August 2025**
    -   New:
        -   Move capability for resource assignments in Resource management workspace.
        -   Description for all assignment operations in Resource management workspace.
    -   Changed:
        -   Showing operational work type as a label for operational resource assignments in RM workspace.
        -   Added info message during backend processing of resource allocations on assignment creation.
    -   Fixed:
        -   Start and end dates of resource assignments in the Resource management workspace are not updating correctly when the system was set to a custom date format.
        -   Resources could not be allocated if the assignment date range fell outside the board's date range.
        -   Heatmap in the Resource Management workspace is not display complete data.
        -   Actuals were cleared when the status of a resource assignment was updated from the Resource management workspace.
        -   Resource management workspace failed to load when the security plugin was installed and a user had a requested operational resource plan.
        -   Accessibility issues.
-   **Version 5.1.2 - July 2025**
    -   Fixed:
        -   Actuals are cleared off when the status of the resource assignment is changed
        -   The bottom tray isn't refreshing when a work is assigned
        -   The allocation module stale data issue occurs when it's opened without refreshing
        -   Allocate resources when assignment date range is outside the resource board date range
        -   The CPAAM effort table and resource aggregate monthly and weekly tables are not updated when assigning an unassigned work
-   **Version 5.1.1 - May 2025**
    -   New:
        -   Landing page for the workspace. Configurable overview dashboard for resource managers based on all resources with the ability to filter down based on attributes.
        -   Ability to edit all resource assignments, group assignments, and operational group assignments within the workspace.
        -   Ability to request/extend resource assignments.
    -   Fixed:
        -   Improved performance of the RMW bottom tray.
        -   In the top tray of RMW, the hours are set to zero in the heatmap view when user provides negative hours.
        -   In the top tray of RMW, effort is shown as blank if a negative value is entered in the effort column.
-   **Version 5.1.0 - February 2025**
    -   New:
        -   Allocation modal updated for user cell and group cell.
        -   Open assignment and Open parent assignment options from the row context menu options to open the details page of resource assignment.
    -   Fixed:
        -   Editing the allocation values updates next week allocations in Weekly view when the resource management first day of week property is set to Sunday.
        -   Magnifying glass or Lookup icon is not working for the references fields in the New Resource Assignment Modal.
-   **Version 5.0.3 - December 2024**

    Fixed: Resource Board does not load if the number of users for a criteria is too high.

-   **Version 5.0.0 - November 2024**
    -   New:
        -   Ability to group resource board assignments.
        -   Supporting 'exclude\_status\_from\_availability' property in Resource Management Workspace calculations.
    -   Fixed:
        -   Improved loading time of resource board page.
        -   Accessibility issues of Resource Management Workspace.
        -   Ability to update child resource assignment status.
        -   Minor bugs.
-   **Version 4.0.1 - August 2024**
    -   New:
        -   Create a Resource Board by Filtering the Type of task.
        -   Split assigned resource assignments for a Resource.
        -   Create New Resource Assignments in Resource Management Workspace \(including operational assignments\).
        -   View or hide additional columns to top tray using side menu.
        -   Alarm indicator to identify changes made to a resource assignment.
        -   Ability to view actuals vs. planned efforts in Resource Management Workspace.
    -   Fixed minor bugs
-   **Version 3.0.1 - June 2024**

    Fixed: Issue with classic resource plans not being visible in Resource Management Workspace.

-   **Version 3.0.0 - May 2024**
    -   New:
        -   Reassign and unassign resources using the drag and drop feature.
        -   Edit allocated hours of the resource assignments using the inline editing of the top tray.
        -   Drag and drop to reassign or unassign resources.
        -   Export the resource grid data to Excel and CSV.
    -   Fixed: Minor defects
-   **Version 2.0.1 - February 2024**
    -   New:
        -   Filter the unassigned tasks within the lower tray.
        -   View the resource assignments allocation using the allocation heatmap.
        -   Assign resources to unassigned work.
        -   Save different resource board views.
        -   Have visibility into resource status \(approve, pending, unapproved\)
        -   View resource capacity and allocation details on the allocation heatmap modal
        -   Chat with the task owners via Microsoft Teams
-   **Version 1.0.0 - November 2023**
    -   The Resource Management Workspace is designed to help Resource Managers streamline their tasks and work efficiently.
    -   It provides a centralized platform focusing on resource management; allowing you to oversee, manage, and resolve resource-related issues easily. This workspace consolidates all your resource management activities in one place giving you a complete view of your resources and projects.
    -   It helps you to quickly allocate resources, identify conflicts, resolve issues on-demand, and collaborate with team members effectively.

