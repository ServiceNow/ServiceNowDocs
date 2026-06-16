---
title: Project Workspace release notes
description: Version history for the Project Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-project-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 12
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Project Workspace release notes

Version history for the Project Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 7.3.0 - June 2026**
    -   Performance Enhancements to AI Project Plan Generation.
    -   Ability to Export RIDAC to CSV, Excel
    -   Auto Sync of Resource assignments with task
    -   Copy a Resource Assignment option in PWS to copy and create new resource assignment.
    -   Open Resource Assignment option in PWS
    -   Option to create a new resource assignment from PWS using the resource form
-   **Version 7.2.1 - May 2026**
    -   New:
        -   Supporting changes for AI Project Creation from Documents, Generate Tasks, AI-recommended Risks, AI Status Reports \(template-based generation and skill chaining\).
        -   Resource Finder modal for unassigned Resource Assignments, displaying fit score and AI rationale \(with AI skill on\) and availability view, enabling direct-to-assign flow.
    -   Fixed: Field-level ACLs are now honored in the Resource Grid of the Project workspace.
-   **Version 7.1.0 - March 2026**
    -   New:
        -   Rename to "Resource Assignments" on Planning
        -   Australia\|HAM hardware request integration with SPM
        -   \[GenAI\]Add "AI Insights" in L2
        -   Home page perf optimization
        -   \[GenAI\]AI status report changes
        -   RMW grid via UXF interop config
        -   "Generate Labour Costs" UI migration for demand
        -   Honor column-level custom ACLs on planning
    -   Fixed:
        -   \[GenAI\]Infinite loading on LLM failure
        -   BR not throwing error in resource assignment
        -   New rate\_model changes
        -   Disable Comment in Activity section for project user
        -   Switching effort types mid-assignment issues
        -   Risk/Issues/Action missing related items on Analytics
        -   AI Gradient missing for button/alert
        -   PRJTask missing after template applied without refresh
        -   Uneditable Decision Status in RIDAC
        -   Subproject Key Milestone not on status report
        -   Delete Status Report creates empty record
        -   "Configure Project Insights" missing when already configured/scheduled
        -   Schedule Baseline not created from details
        -   Resource Plan End Date next day vs prj end date
        -   Prj card Start/End Date label not updated
        -   \[Ext\]Cost Trend Analysis not translated
        -   Status report inserting with empty prj
        -   Resource/cost plan not deleted on child task removal from planning console
        -   Date Pickers ignore 1st day of Week in Planning
        -   Repeated record opens without refresh causes longer load times
        -   Can't delete cost plans
        -   Prj class display order varies by language
        -   "Resources not synced" bug with dd/MM/yyyy
        -   PWS breaks with false filter conditions
        -   tsp1 Phase creates pm\_project\_task instead of tsp1\_project\_task
-   **Version 7.0.0 - December 2025**
    -   New:
        -   Introduced Playbooks within Project Workspace to support guided, standardized project execution. Shipped two out-of-the-box \(OOB\) Playbooks to help teams get started quickly
        -   Status report enhancements
            -   Added a Status field to Status Reports so project managers can set and communicate the current state of each report
            -   Enabled Status Report Duplication without a modal. Static content is automatically copied; dynamic content is regenerated using the latest Status Report snapshot
            -   Non-editable dynamic blocks are now disabled in Edit mode to prevent modification of system-generated data
        -   Optimised the Planning page data fetch logic to improve the reference field data fetch
        -   Home page Project modal changes
            -   Create from template modal
            -   Added new fields to the New Project modal
        -   Updated RIDAC page to provide a more efficient R1 panel experience
        -   \[A11y\] Support Reflow 400% zoom for project workspace
        -   Enabled creation of labor cost plans on sub-projects
        -   Added support for Benefit Plans within Financials to improve planning and reporting accuracy
        -   Introduced multi-currency support on work items
        -   Users can now allocate effort from an unassigned Resource Assignment \(RA\) in any way they choose — fully to one resource, fully across multiple resources, or partially to one or multiple resources while the unassigned RA retains any remaining effort
    -   Fixed:
        -   New Button is not displayed for Project tasks and Subprojects tabs in details page for Customer projects
        -   Loading Screen Issue When Applying Template to Sub Project
        -   The side menu is not loading in the Project Workspace after Global Search
        -   "Export Project Status" in the New Project Workspace is not working for the TeamSpace or TSP tables
        -   "Constraint Type" field options not being translated
        -   \[Japanese Localization\] - When creating a new project in Project Workspace, the project classes selection are still in English
        -   Provided a button to remove the subproject from the top Project through sub project related list
        -   New Project Workspace in the "Grid" fields are showing 'Days' even though it's configured as "Hours"
        -   Exporting Project into CSV from Project workspace. Doesnot export Additional Assignees list
        -   Activity stream in Project Workspace does not show the user names for updates to project tasks
        -   Deleting a record from the related list of a Project record on Project Workspace redirects to different pages
        -   Project workspace - Create project modal is going in to infinite loading on clicking creating after providing template name
        -   Projects cannot be Exported from Strategic Planning Workspace
        -   Project Baselines taking longer to load in New Project Workspace when having more than 3000 tasks
        -   Project Template not Syncing with Portfolio \(pm\_portfolio\) when the project is created from Project Workspace
        -   Project Workspace Filter for Related Lists Conditions does not show results
        -   During export of sub-projects from project workspace along with subproject records, it's parent hierarchy records are also being exported
        -   Inconsistent Project State Behavior: Project Workspace sets overall State to 'Closed Complete' when all Tasks are 'Closed Incomplete', while Native UI sets it to 'Closed Incomplete'
        -   508 Compliance in Project Workspace
-   **Version 6.3.2 - September 2025**

    This is a dummy release created to add the dependency on the September version of the Doc component

-   **Version 6.3.0 - August 2025**
    -   New:
        -   Redirection to resource management workspace from project workspace
        -   Ability to sync resource assignments of the project when project is closed
        -   Updates made on the status report form are reflected in the Status Report document when the property sn\_pw.status\_report\_doc\_read\_only is set to true
        -   New 'Display modes' on record financials page to view planned costs for all fiscal periods and planned vs actuals for all fiscal period
    -   Fixed:
        -   No projects shown and filter failed to work on the Project Workspace for some users
        -   Roll up field value is not honoured when update is made on planning page grid
        -   Copy status report makes copy even if user cancels
        -   Task checklists are not refreshing when switching between tasks in the Project Workspace
        -   Updates made on the status report form are not reflected in the document content when the property is set to false
        -   Cost plan and breakdowns honor ACLs in the new Financials page
-   **Version 6.2.4 - July 2025**
    -   Fixed:
        -   The Resource assignment grid in the 'Planning' tab of the Project Workspace wasn't loading because of a bad request error
        -   Some planning page modals were not closing properly
        -   In the PWS bottom tray, hours are doubled if the allocation dailies are more than the allocation batch size provided
-   **Version 6.2.0 - May 2025**
    -   New:
        -   Ability to copy/duplicate status reports
        -   Ability to request/extend resource assignments
    -   Fixed:
        -   When submitting a status report on New project workspace without mandatory fields, it keeps loading indefinitely
        -   In the Project Workspace, RIDAC states were shown as integers and were not editable from the list
-   **Version 6.1.0 - February 2025**
    -   New:
        -   Added checklist at the project and project task level in planning and details page
        -   Ability to import status reports created from the classic workspace
    -   Changed: Status reports on the new Project workspace will now be read only unless they are marked editable explicitly
    -   Fixed:
        -   Fixed issues related to project workspace column user preferences
        -   Minor other bugs
-   **Version 6.0.1 - January 2025**

    Fixed: The issue with widgets in the Analytics tab of the project workspace not loading for Yokohama instances has been fixed.

-   **Version 6.0.0 - November 2024**

    New: New status reports component.

-   **Version 5.2.3 - October 2024**

    Fixed issue with adjusting gantt progress bars when date format is dd MMM yyyy.

-   **Version 5.2.0 - August 2024**
    -   New:
        -   Home page
            -   Ability to view projects in List view along with the cards view on home page.
        -   Planning page
            -   Ability to toggle between hours, person days and FTE on the resource assignment grid.
            -   Ability to view actuals on the resource assignment grid.
            -   Ability to create agile phase.
        -   Financials page
            -   New Budget allocation capability for portfolio managers that allows budget to be allocated for shorter time periods like fiscal period or quarter apart from years.
            -   New budget vs cost comparison view for project managers to compare their latest costs with the approved budget to identify budget overruns.
            -   Ability to categorize resource assignments as Capital or operational expenditure for more accurate categorization of labor costs generated for the demands or projects.
            -   Migration capability for admins to move the budget data for on-going demands or projects from classic experience into the next experience supporting customers to adopt the next experience easily.
            -   Compare simple financials data captured in financial baselines using the new compare baselines view in the project workspace.
    -   Changed:
        -   Improved performance on project workspace save flow.
        -   Any user action that affects resource allocation on an approved assignment will now show a confirmation modal.
    -   Fixed: Minor bugs.
-   **Version 5.1.3 - July 2024**
    -   Fixed:
        -   Analytics dashboard is not loading in upgrade scenario is fixed.
        -   Enabling resource plan toggle on by default for new customers and for upgraded customers only if there are no classic resource plans.
-   **Version 5.1.2 - June 2024**

    Changed: Enabling resource planning by default for new customers.

-   **Version 5.1.0 - May 2024**
    -   New:
    -   -   Financials: Ability to migrate financial baselines from classic UI to the new project workspace using UI actions or a scheduled job
-   Docs: Ability to create project docs that provides the ability to manage ideas, take notes, collaborate with team members, and create documentation. Project managers can save an existing page as template and use the template for the same or other projects.
-   Provide "recalculate resource cost" on resource assignments for projects/demands with rate model on them.
-   Analytics dashboard in next experience
    -   Changed: Financials: In the 'New cost plan' form, 'cost duration' option has been renamed to 'cost distribution' with respective options to make more user friendly.
-   **Version 5.0.1 - March 2024**

    Fixed issues with Creation of New cost plans, cost plan breakdowns, resource plans, expense lines and benefit plans on Details Page.

-   **Version 5.0.0 - February 2024**
    -   Newly added:
        -   Project Details Page
            -   A project details page in next experience to show all the details of the project.
            -   Details page with all the sections and related lists from the classic project details page.
        -   Financial Planning
            -   Quickly view the financial totals like Estimate at completion, Budget, EAC vs Budget variance, Planned cost, Actuals to date using the new widgets in the financials screen for Projects.
            -   Flexibility to configure the widgets as per your organization's needs.
            -   Export the latest financials data and the baseline comaparison data to excel or csv.
            -   Clearly view or edit the cost plans and expense lines using a wider side panel.
            -   Delete any incorrect or unwanted cost plans using the 'Delete' option using the 3-dot menu in the grid.
            -   Save the user preferences for show/hide columns, changed column width or time scale.
            -   Create expense lines to capture unplanned costs using the 'New Expense line' option in the cost screen.
            -   Using the better together integration with Source-to-pay applications, automatically get the cost plans created based on Purchase orders and expense lines created for the actual costs based on the Invoices logged in the Procurement process.
            -   Switch to the new attribute based RM-Financials process using the migrate resource plans option which migrates existing labor cost plans created based on classic resource plans to new attribute-based labor cost plans along with resource plans.
-   **Version 4.2.0 - November 2023**
    -   New:
        -   Full row edit support in Resource Assignment grid.
        -   User preferences for Display summary task, Bar labels, Dependency lines.
        -   Create financial baselines for Projects manually or automatically using a scheduled job to capture the status of financial costs at any given time.
        -   Compare any two financial baselines to easily analyze the changes in costs, report what caused the variance and when it occurred.
    -   Fixed: Usability and functional issues.
-   **Version 4.1.1 - September 2023**

    Fixed: Fixed usability issues on dependency cell editor.

-   **Version 4.1.0 - August 2023**
    -   New:
        -   Financials in Project Workspace:
            -   Create and edit cost plans conveniently from the side-panel.
            -   Reforecast the planned costs with the new in-line editing feature.
            -   View a streamlined perspective, showcasing the actual costs for the past and planned costs for the future for the entire time scope of the work.
            -   Get a better comprehensive solution by viewing the EAC, ETC, and Actuals to date of each cost plan for the total time scope and the yearly breakdowns.
            -   Generate labor cost plans depending on the attribute-based resource assignments for entire scope of the planning item.
            -   Create expense lines against the cost plans easily from the side panel with the associated cost plan details pre-populated.
            -   Easily view the list of expense lines against the cost plans in the side panel and make any updates.
        -   Support for Resource movement when tasks are moved in the project.
        -   New Allocation model to show users allocation for a month/week.
    -   Minor fixes.
-   **Version 4.0.0 - May 2023**
    -   New:
        -   Resource assignments on Project workspace
        -   New views - Grid only, Gantt only, Both
    -   Fixes
-   **Version 3.1.1 - May 2023**

    Fixed: Updated dependent application version to fix an issue.

-   **Version 3.1.0 - February 2023**

    Bug fixes.

-   **Version 3.0.1 - May 2023**

    Fixed: Updated dependent application version to fix an issue.

-   **Version 3.0.0 - November 2022**
    -   New RIDAC page provides a single view to manage all Risks, Issues, Decisions, Actions, and Requests Changes within a project.
    -   Create, Edit, Convert, and Associate RIDAC records
    -   Filter and sort RIDAC records
    -   Group by RIDAC type
    -   Personalize RIDAC columns.
-   **Version 2.1.0 - August 2022**
    -   New:
        -   Improve visibility into task dependencies by adding external dependencies to the project.
        -   Perform row context actions on multiple tasks together. The row context menu of the project tasks in the grid view now includes options to indent, unindent, and delete these rows at once.
        -   Search to fill in reference field information. While filling in reference fields such as Project manager, Assigned to, or Assignment group, you can now look up the record you need using the search option.
-   **Version 2.0.1 - May 2022**
    -   New:
        -   Manage and plan large projects with over 10,000+ tasks
        -   Directly navigate to a Sub Project via Project Workspace homepage
        -   Toggle between parent and subproject on planning page
        -   Use advanced settings including: turn on/off autosave, change date/time preferences, toggle automatic vs manual calculation
        -   Exit to any classic project workspace page from planning page.
        -   Add and indent task shortcuts on Gantt
        -   View baseline start date, end date, and variance details in list view
        -   Receive platform and email notifications when a task is assigned to you
-   **Version 1.0.0 - February 2022**
    -   New:
        -   Updated UI and UX
        -   Performant scheduling
        -   New homepage features:
            -   My Projects and All Projects tabs
            -   Search by assignee or project name
            -   Quick sort options
            -   Switch to classic workspace
        -   New planning console features:
            -   Autosave edits
            -   Single and multi-row drag and drop
            -   Copy and paste of cells and rows
            -   Rearrange columns
            -   Sort and filter columns
            -   Expand and collapse rows
            -   Bulk edit of cells
            -   Right-click action menu
            -   Dependency type-ahead in the data grid
            -   Draw dependencies in the timeline view
            -   Display and compare up to two baselines at same time
            -   Attach files and chat with stakeholders within planning console

**Parent Topic:**[ServiceNow Store - Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itbm-highlight.md)

