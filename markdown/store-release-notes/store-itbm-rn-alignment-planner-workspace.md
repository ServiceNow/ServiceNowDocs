---
title: Alignment Planner Workspace release notes
description: Version history for the Alignment Planner Workspace application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-alignment-planner-workspace.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 6
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Alignment Planner Workspace release notes

Version history for the Alignment Planner Workspace application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 8.15.0 - June 2026**
    -   New:
        -   Use the Planning item lens to plan, prioritize, and roadmap work directly with planning items, without configuring organization structure, programs, portfolios, or products.
        -   Added partition support for project and demand planning item tables.
        -   View additional status attributes — cost, resource, schedule, and scope — for planning items in Portfolio Planning Workspace. For project planning items, these attributes are synced automatically from the latest published project status report.
        -   Make a portfolio plan public and share the copied link with Portfolio Planning Workspace users, without inviting them individually or as a group.
    -   Fixed:
        -   Fixed an issue where the Kanban filter stopped working after upgrading to Zurich.
        -   Fixed an issue where Demand Type incorrectly defaulted to "Project" when the Category was set to "Operational."
        -   Fixed an issue that caused a roadmap bar to fail to render when the work item's owner was an inactive user.
        -   Fixed an issue where the roadmap appeared empty when navigating to Portfolio Planning via "View Roadmap" from the EA Workspace.
        -   Fixed an issue where the Select Lens option was missing in Hierarchy when the project portfolio lens was set to inactiv
        -   Fixed an issue where users could see a Portfolio's name without having access to that Portfolio.
        -   Fixed an issue where a Portfolio Plan viewer was able to manage access, which exceeded their permission level.
        -   Fixed an issue where an Admin was unable to access the playbook in the Demand Workspace.
        -   Fixed an issue where using the "Move" option to reschedule a resource or task to another date did not update the CPAAM Effort table.
-   **Version 8.14.0 - May 2026**
    -   New:
        -   Added expand and collapse functionality for Portfolio Planning views.
        -   Added the Category, Type, and Description fields to the new demand form view in Demand Workspace.
        -   Added the NACM component for portfolio insights on the planning page.
        -   Added the Demand AI Specialist side panel UX for agent activity visibility on demand records.
        -   Added the ability to copy the link for a portfolio plan via the Share Actions button and Manage Access modal.
    -   Changed: Updated project and demand demo data deadlines and milestones to the key type.
    -   Fixed:
        -   Resolved an issue where collapsing the resizable pane hid the expand button beneath the L1 menu.
        -   Resolved an issue where editing a planned target redirected users to an incorrect tab in the related list.
        -   Resolved an issue in the Free Form Roadmap \(Kanban tab\) where saved view changes were not retained after a page refresh
-   **Version 8.13.0 - March 2026**
    -   Demands:
        -   Unified and streamlined demand management experience with AI-powered demand Playbook, integrated with the AI Control Tower.Note: To use Playbooks in Portfolio Planning, you need at least Playbook version 28.4.1 and ServiceNow Platform version Zurich Patch 7.
        -   Demand Workspace is accessible from the Portfolio Planning Workspace, featuring a redesigned UI and improved navigation.
        -   Key enhancements include priority-based sorting in hierarchy views and dynamic loading of target breakdowns for better performance.
    -   Financials:
        -   Financial baselines support multicurrency.
        -   Labor costs are automatocally generated when there is a change in resource effort allocation at breakdown level without any change to the total requested efforts.
-   **Version 8.11.3 - January 2026**
    -   Fixed:
        -   URL fields are now clickable and support direct navigation.
        -   Quick edit functionality is restored in Level 1 list views.
        -   Approving a portfolio plan scenario no longer removes unapproved scenarios from other portfolio plans.
        -   Fixed few additional issues related to the Portfolio Planning application.
-   **Version 8.11.1 - December 2025**
    -   Roadmaps now support admin-defined custom colour themes for better visual alignment with organisational standards.
    -   Portfolio plans shared with the Viewer setting are now viewable regardless of the user’s read/write access to the associated work.Note: Record pages remain read/write or read-only based on the user’s permissions.
    -   SPW Lists have been uplifted to use the ServiceNow presentation list component for a more consistent user experience.
    -   Guided setup is now available to SPW admins \(apw\_admin role\). Previously, only system admins could access this functionality.
    -   Added the sn\_value\_stream.value\_stream\_admin role, which includes the value\_stream\_user role. This new role provides create, write, and delete access to the cmn\_value\_stream\_category table.
    -   Added capability for the sn\_align\_core.apw\_admin role to update app-specific system properties in app-alignment-planner-core.
-   **Version 5.0.1 - November 2022**
    -   New:
        -   Lenses: Lens indicate the perspective by which planning managers can plan, prioritize, and fund work. For example, depending on your role, you can plan work from the perspective of a delivery organization, strategic investment, or product.
        -   Portfolio plans: Portfolio plans are shareable personalized plans that a planning manager can build using lenses.
        -   Portfolio Prioritization: Rank and analyze the work pipeline for a portfolio plan, to prioritize them into roadmaps.
        -   \(For SPM Pro licensed users\) Automate the actual value of your targets for the goals by collecting the actuals from the tables such as benefit plans, cost plans, surveys/assessments, and PA Indicators.
    -   Changed:
        -   The Backlog page is renamed to Prioritization
        -   Ad Hoc Roadmap is renamed to Free-form roadmaps
        -   The main menu navigation in the workspace is updated to include the following:
            -   Home: Contains navigation to Portfolio Plans, Free-form roadmaps, Goals, Prioritization and Portfolio Roadmap
            -   Lists: Contains lists of entities and planning items associated with all the lenses.
        -   Roadmap preferences are now saved per portfolio plan and not per user. Any personalization settings are applicable to all the users and user groups that a portfolio plan is shared with.
    -   Removed: Planning Hierarchy and Planning Organizations are no longer supported.
-   **Version 4.1.1 - August 2022**

    New:

    -   Backlog changes
    -   -   Edit the backlog items inline.
-   View the Rank as a separate column.
    -   Roadmap side panel UX improvements
-   **Version 4.0.0 - May 2022**
    -   New:
        -   Goals \(OKRs\): Define and manage your goals in APW to accomplish your organizational plans and drive business outcomes. Note: Accessing the Goals module from the workspace requires a Strategic Portfolio Management \(SPM, formerly ITBM\) Pro license.
        -   APW Backlog:
            -   Understand the work pipeline for your organization from a single consolidated view.
            -   Organize the backlog list using the features such as grouping and sorting.
            -   Use data points such as planned cost, planned benefit, and associated goal to review backlog items.
        -   Roadmap item dependencies: Create and manage direct and indirect dependencies at the planning item level on the roadmap.
        -   Apply custom filters to planning hierarchy-based roadmaps.
    -   Fixed: If the planning organization for a work or planning item \(that is associated with a goal already\) is changed to an unsupported planning organization, the application now notifies this as an error.
-   **Version 3.1.0 - February 2022**
    -   New:
        -   Guided setup for configuring APW.
        -   Ability to import work items \(epics\) from Azure Devops into APW, provided the necessary integration app is installed and configured.
        -   Support scrum and SAFe epics using single table in APW.
        -   Next experience modern UI for Alignment Planner Workspace and roadmap component.
-   **Version 3.0.1 - November 2021**
    -   New:
        -   Planning hierarchy: Work on same planning item at two different organisation levels. 
        -   Roadmap Planning:
            -   Track planning items by creating milestones directly from the roadmap view, except for projects.
            -   Update or delete the milestones that you added to your planning items \(except for projects\) so that they reflect any change of plans.
            -   For projects, it is recommended to create or edit milestones from the Project workspace because they may impact the associated project plans. However, these project milestones can be accessed \(read-only mode\) in APW roadmaps when you integrate APW with Project Portfolio Management.
    -   Changed:
        -   Planning item's details are editable in side panel
        -   Converted demands are hidden from the roadmap view
        -   View names used by different entities are changed:
            -   Workspace Preview is now APW Preview
            -   Workspace New is now APW new
            -   Workspace Default is now APW Default
-   **Version 2.0.0 - August 2021**
    -   New:
        -   New module 'Alignment Planner Workspace'.
        -   Organizational planning hierarchy.Roadmaps integrated with planning hierarchy.
        -   Roadmap-level \(planning organization-level\) milestones.
        -   Tracking mode in roadmaps.
        -   Share Ad Hoc roadmaps with users
        -   Ability to zoom in/out on roadmaps to adjust the timescale
    -   Changed: Module to navigate to Adhoc roadmaps is renamed from 'Roadmap Planning' to 'Ad Hoc Roadmaps'.
-   **Version 1.0.1 - February 2021**

    New: Alignment Planner Workspace provides an end-end integrated experience for the ITBM planning personas to plan the organization roadmap and manage it.


