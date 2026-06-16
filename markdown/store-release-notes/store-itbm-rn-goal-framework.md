---
title: Goal Framework release notes
description: Version history for the ITBM Goal Framework application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-goal-framework.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Goal Framework release notes

Version history for the ITBM Goal Framework application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.13.0 - June 2026**

    Changed: Updated platform directives for scoping bypass and Cobalt Raven ACL changes.

-   **Version 4.12.1 - April 2026**

    Fixed: Resolved an issue that prevented users from updating the assigned entity type and assigned entity for a goal.

-   **Version 4.12.0 - March 2026**
    -   New:
        -   Added anAssigned Entity field for targets, enabling association of targets with an organizational entity.
        -   Introduced aCancelled state option for Goals and Targets.
        -   Updated reference fields to display only active Strategic Plans and Strategic Priorities.
    -   Changed: Users with the sn\_ppm\_read role now have read access to the Primary Goal, Primary Target, and Strategic Priority fields on the Demand record.
-   **Version 4.11.0 - December 2025**

    Changed: Removed the flow\_designer role from the goal\_admin role.

-   **Version 4.10.0 - August 2025**
    -   New:
        -   A new category, Artificial Intelligence, has been introduced for Goals.
        -   A new type, Artificial Intelligence, has been introduced for Strategic priorities.
    -   Changed:
        -   Users with the sn\_gf\_goal\_admin role can now edit all goals and targets, regardless of whether they are the owner or contributor of a goal or target.
        -   Goals marked as inactive will no longer be displayed in the Goals list by default.
-   **Version 4.9.0 - May 2025**
    -   Fixed:
        -   The label name is showing as Base value instead of Start value in the error message.
        -   The label name is showing as Target value instead of Final target value in the error message.
        -   When the Check-in frequency is set to Weekly on Sunday for a target, the check-in due date is populated with the previous Friday's date instead of the next Friday's date.
-   **Version 4.8.0 - February 2025**
    -   Fixed:
        -   Check-in due date support for custom date format.
        -   Fixed warning message on clearing actuals of targets.
-   **Version 4.7.0 - November 2024**
    -   New:
        -   Baseline reference field is added in the Target table
        -   Added class field in strategic priority and target table to enable extension of these tables: Target \[sn\_gf\_goal\_target\] and Strategic Priority \[sn\_gf\_strategy\]
    -   Changed:
        -   Label changes:
            -   Review frequency to Check-in frequency
            -   Base value to Start value
            -   Target value to Final target value
            -   Actual value to Actuals to date
            -   Review due date to Check-in due date
        -   Check-in due date calculation logic is updated to improve its usability
    -   Removed: Fortnightly option in Check-in frequency \(formerly known as Review frequency\) is no longer supported for new customers
-   **Version 4.5.0 - August 2024**
    -   Changed: The length of the Name field for Strategic Plan, Strategic Priority, Goal, and Target has been increased to 255 characters.
    -   Fixed: The Primary target field in the planning item gets updated when the Target field is updated for the existing record in Goal/Target relationship related list.
-   **Version 4.4.1 - June 2024**
    -   Fixed:
        -   Defect fix to manage scope issues for ppm entities such as demand and project.
        -   Change the protection policy of a few scripts to read only to fix stale errors on updating of target records.
-   **Version 4.4.0 - May 2024**
    -   New: Supporting changes for aligning work items to targets. \(Note: Strategic Planning needs to be installed for this feature to work\)
    -   Changed: The Primary goal field in the Goal Relationship m:m table has been renamed to Primary.
    -   Fixed: Targets of Yes/No type display choices in the logged-in user's language.
-   **Version 4.3.1 - February 2024**
    -   Fixed:
        -   Removed planning item as a type from goals relationship, for standard portfolio plan users
        -   Restored backward compatibility of goal framework with older version of portfolio plan
-   **Version 4.3.0 - November 2023**

    Changed: Added sn\_gf.goal\_user\_read role to Business Stakeholder so that the users with the Business Stakeholder role can view Goals and related records on the platform lists and forms by default.

-   **Version 4.2.1 - September 2023**
    -   Fixed:
        -   The Actual value field on the Target form was not editable by the user.
        -   The Review frequency field on the Target form was not editable by the user.
        -   Issue related to the Target's progress which is not properly set when there is no actual value.
-   **Version 4.2.0 - August 2023**
    -   New:
        -   Users can now set qualitative targets by defining a custom unit of measure with desired choices. The available new unit of measure for qualitative targets is 'Yes / No'.
        -   Added a new option in the 'Status' column, 'None' for both Goals and Target forms.
    -   Changed: The default value for thesn\_gf.weighted\_average\_enabled property has been changed to true. When the property is enabled, the logic calculates the progress of goals from their sub-goals and targets considering the value populated in the Impact on goal / Impact on parent goal field. Users can disable the property from the Goal Preferences page.
-   **Version 4.1.1 - May 2023**

    Internal mandate related to ACLs.

-   **Version 4.1.0 - February 2023**
    -   New: Ability to create goal relationship on SAFe features.
    -   Changed:
        -   The Weight field on the Goal form has been renamed to Impact on parent goal.
        -   The Weight field on the Target form has been renamed to Impact on goal.
            -   The values for this field have been updated to \(0\) No impact, \(1\) Neutral, \(2\) Moderate, \(3\) High, \(4\) Very high, and \(5\) Maximum.
        -   The existing fields on the Goal form, Company, Business Unit, Department, and Portfolio have been consolidated into two fields, Assigned entity type and Assigned entity. This assigned entity represents the ownership of a goal from organization perspective.
-   **Version 4.0.0 - November 2022**
    -   New: Import your existing goals and targets data \(that are defined outside Goal Framework\) from a spreadsheet to the Goal Framework tables.
    -   Changed:
        -   The Check in frequency field has been renamed to Review frequency on the Target form.
        -   The Review due date field has been added to the Target form.
        -   \(For existing Alignment Planner Workspace users\) The Planning Organization field has been hidden and made non-mandatory on the Goal form. Note: When you install the Alignment Planner Workspace for the first time, the Planning Organization field doesn't appear on the Goal form.
    -   Removed: Removed Planning Organization related validations
-   **Version 3.0.0 - May 2022**
    -   New: Restrict the access for a target record to specific users by enabling the Confidential field on the target form if ESG is installed.
    -   Fixed: If the planning organization for a goal, work, or planning item \(if a goal relationship is already established\) is changed to an unsupported planning organization, the application now notifies this as an error.
-   **Version 2.0.0 - February 2022**
    -   New:
        -   Associating work with goals is allowed based on the planning organization hierarchy.
        -   A new field, Team is added to the Goal \[sn\_gf\_goal\] form, to specify the user group that is responsible in achieving the goal.
        -   Create a goal relationship with planning items of type initiative and big rock where the items contribute to achieving the goal.
        -   If you are a SAFe user, you can associate SAFe epics with goals so the work being done to accomplish goals and meet targets are easily visible.
        -   If you are an APW user, after installing APW, you can use the guided setup to help you with the required core configuration. This guided setup includes steps to set your goal preferences and migrate the existing goals data to Goal Framework.
-   **Version 1.0.0 - September 2021**

    Goal Framework enables strategic planning and helps define and construct strategic priorities and associated goals for the organization. This application facilitates personas such as strategy officers, the SRO, ePMO, and portfolio managers to track strategy execution by associating work and planning items such as demand, project, and portfolio to the defined goals.


**Parent Topic:**[ServiceNow Store - Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itbm-highlight.md)

