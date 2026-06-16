---
title: Portfolio Planning release notes
description: Version history for the Portfolio Planning on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-itbm-rn-portfolio-planning.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 14
breadcrumb: [ServiceNow Store - Strategic Portfolio Management release notes, ServiceNow Store release notes]
---

# Portfolio Planning release notes

Version history for the Portfolio Planning on the ServiceNow Store.

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
-   **Version 8.9.1 - September 2025**
    -   Fixed:
        -   The following issues applicable to Zurich have been fixed:
            -   Filters are not retained across tabs after refreshing the page.
            -   The page property change handler does not trigger when the page is accessed multiple times.
            -   Context props are undefined when navigating back using the breadcrumb.
-   **Version 8.9.0 - August 2025**
    -   New:
        -   Financials:
            -   Ability to do financial planning on any planning item like Feature, Capabilities, etc.
            -   No dependency on integration with task tables for enabling financials on projects, demands and epics planning items
            -   New 'Display modes' on record financials page to view planned costs and planned vs actuals for all fiscal periods
        -   Portfolio Plans:
            -   The milestone bar now stays fixed at the top of the roadmap during scrolling
            -   Different milestone types are now represented with distinct icons
            -   Quick filters now support both string and boolean type conditions
            -   Roadmap bars display consistent colors across portfolio plans when grouped by the same attribute
    -   Changed:
        -   Portfolio Plans: The milestone limit for roadmap items has been increased from 50 to 100
-   **Version 8.8.0 - May 2025**
    -   New:
        -   Scenario Planning
            -   Define portfolio budget as the target, and do a cost-benefit analysis by trying out different budget combinations for the work items
            -   Populate the budget bottom-up from the forecast or enter a top-down budget value to evaluate different budget approval scenarios
            -   Choose to simulate budget allocation for various time scales like month, quarter, year, or total plan timeline
            -   Flexibility to do financial planning by capex/opex or at additional granularity by labor, software, hardware, and other various categories
            -   Visualize the differences in financials between multiple scenarios through the compare scenarios screen
            -   Auto-populate the approved budget on work items on scenario approval
            -   Optionally convert the prioritized demands to projects on scenario approval
        -   Portfolio Plan views
            -   Create, edit, and switch between views with display preferences such as column selection, grouping, and filtering for portfolio plans
            -   Ability to create personal views that are private to you, or public views that can be shared with stakeholders who have access to the portfolio plan
            -   The portfolio plan view saves your display preferences across the Prioritization, Roadmap, Capacity, and Financials tabs
        -   Dashboards
            -   Use dashboards to view key data and metrics, enabling you to monitor performance, track progress, and make informed decisions related to planning and execution.
            -   Each widget within a dashboard displays key data and metrics and may include visualizations. The default available dashboard is the Execution Dashboard.
            -   Use the out-of-the-box dashboards or create your own dashboards based on your requirements.
    -   Changed:
    -   -   Financial planning:
    -   View the portfolio target and target balance from the last approved scenario to compare latest budget against the defined portfolio target
-   **Version 8.5.1 - April 2025**
    -   Fixed:
        -   When a non-financial/non-goal/non-capacity user creates a portfolio plan, disable and turn off the toggle for the respective modules under "Show/hide modules".
        -   The portfolio is not loading after toggling on the Owner/Item type in Kanban view.
-   **Version 8.5.0 - February 2025**
    -   New:
        -   Financial Planning:
            -   View rolled-up financial costs and benefits data of planning items in the new 'Financials' tab to integrate financial insights into your planning and improve decision-making
            -   Analyze financial data for Demands, and Projects at the portfolio level across varied time scales and ranges for greater flexibility
            -   Monitor Budget, Forecast, Budget vs Forecast Variance, Planned, Actuals, and Remaining Estimates by expense or cost type to improve visibility and precision in financial management
            -   Track Planned, Actuals, and Variance of monetary benefits to maximize ROI and align financial outcomes with business goals
            -   Record estimates and actuals of monetary and non-monetary benefits for planning items using the new Monetary Benefit Plans and Non-Monetary Benefit Plans tabs in the Record details page
-   **Version 8.4.0 - November 2024**
    -   Portfolio Planning \(Planning and Free-form roadmaps\):
        -   New:
            -   Modular portfolio plan - Show or hide modules or features for your portfolio plan to display only the modules that matter to your stakeholders
            -   Ability to quickly filter planning items in the Prioritization page with multi-value field or fields, such as tags, business application, and business capability
            -   Filter roadmap bars in the Roadmap page with multi-value field or fields, such as tags, business application, and business capability
            -   Group roadmap bars by any multi-value field such as tags, business capability, etc.
            -   Scheduled job to generate capacity for all resources as adefined cadence.
        -   Changed: Renamed Copy &lt;planning item type&gt; to Duplicate in the row context menu for creating duplicates of planning items.
    -   Capacity Planning:
    -   -   New:
    -   Select primary attribute to automatically populate resource criteria from the resource assignments of the prioritized planning items.
-   Changed:
    -   View the capacity details for only prioritized planning items.
    -   Enhanced user experience to view the total capacity and total estimate of resource types in the Capacity Planning screen.
    -   Financials:
        -   New:
            -   View cost plans, expense lines, budget, and financial baselines of sub projects at the parent project level. View the financial performance of a project using the rolled up planned and actuals costs in the widgets of parent projects.
-   **Version 8.3.1 - September 2024**
    -   Fixed:
        -   When a user returns to the scenario a second time, the scoring framework columns in the prioritization tab do not display correctly due to a caching issue.
        -   Clearing score when you toggle on/off the In plan for an item in scenario mode.
        -   The hierarchy displays an infinite loading spinner when a portfolio plan is created using the business capability lens that returns no records.
-   **Version 8.3.0 - August 2024**
    -   New:
        -   Financials on planning item records:
            -   New budget allocation capability for portfolio managers that allows budget to be allocated for shorter time periods like fiscal period or quarters
            -   New budget vs cost comparison view for planning items. Owners can compare their latest costs with the approved budget to identify budget overruns
            -   Ability to categorize resource assignments as capital or operational expenditure for more accurate categorization of labor costs generated for demands or projects
            -   Migration capability for admins to move the budget data for on-going demands or projects from classic experience into the next experience. This allows customers to adopt the next experience easily
            -   Compare simple financials data captured in financial baselines using the new compare baselines view for planning items
        -   Scenario Planning:
            -   Create multiple scenarios of the changes to your portfolio plan in a simulation mode. Try out different combinations of prioritized items and their timelines
            -   Compare multiple scenarios to analyze different tradeoff decisions made between scenarios and determine the best plan
            -   Approve the optimal scenario to revise the states and approved dates of the live portfolio plan ensuring the creation of an optimal portfolio plan
            -   View approved scenarios in read-only mode for future reference
        -   High-level planning for programs: Enable high-level planning for program table in Project Program lens to prioritize, score, and roadmap programs \(pm\_program\).
-   **Version 8.2.2 - July 2024**

    Fixed the issue where the text link was not visible on the Goals aligned card in Xanadu.

-   **Version 8.2.0 - May 2024**
    -   New:
        -   Use the Project Program lens to plan, prioritize, and roadmap the work of the programs or portfolios.
        -   Support for inline editing of tags in the prioritization list view.
        -   Support for filtering tags in the quick filters in a portfolio plan.
-   **Version 8.0.1 - March 2024**
    -   Fixed:
        -   The prioritization-hierarchy view was not loading when the user unchecks a few columns from the side panel and clicks on the browser refresh button.
        -   Filters were not retained between the List and Hierarchy views of Prioritization.
-   **Version 8.0.0 - February 2024**
    -   Newly Added:
        -   Financial Planning
            -   Quickly view the financial totals like Estimate at completion, Budget, EAC vs Budget variance, Planned cost, Actuals to date using the new widgets in the financials tab of planning items like projects, demands, and epics
            -   Export the latest financial data and the baseline comparison data to Excel or CSV
            -   View or edit the cost plans and expense lines using a wider side panel
            -   Delete any incorrect or unwanted cost plans using the 'delete' option under the 3dot menu in the grid
            -   Save the user preferences for show/hide columns, changed column width or time scale
            -   Add new expense lines for an un-planned cost type using a 'New Expense line' option
            -   Generate labor costs automatically for demands based on resource assignments using an updated 'Generate labor costs for demands and projects' scheduler
    -   Changed:
        -   Prioritization
            -   Enable inline editing in the Portfolio Plans list.
            -   Export planning items data of the portfolio planto Excel/CSVfrom the Prioritization grid.
            -   Delete a planning item from the Row context menu in the List view
            -   Move a planning item to the top or bottom in the List view to quickly change the order of planning items
            -   Personalize the side panel to display the selected columns stacked at the top of the list followed by the unselected columns sorted in alphabetical order.
            -   The side panel now auto-closes after clicking the Apply button
            -   The existing MoSCoW state values have been updated to 1-Must Have, 2-Should Have, and so on along with the icons.
            -   Quickly rearrange the order or position of columns in the grid by horizontal drag and drop of columns.
    -   Fixed:
        -   Prioritization
            -   Rank by any numeric or choice type attribute
            -   Rank or sort by Moscow column
    -   Important information for upgrading: Starting with v8.0.0, you can access the SPM Pro-licensed features only in Strategic Planning Workspace. If you own an SPM Pro license but still using the SPM Pro-licensed features \(such as Goals, Product Feedback, Hybrid portfolio planning, and additional lenses\) in Portfolio Planning Workspace, you must install Strategic Planning to access such features.
-   **Version 7.1.2 - December 2023**
    -   Fixed:
        -   Few cells don't appear in grey though they are not editable.
        -   The planning item moves to the top and the rank goes empty after editing the planning item in the grid.
-   **Version 7.1.0 - November 2023**
    -   New:
        -   Rank the items in the Prioritization list
            -   Ability to rank the items on the prioritization screen based on any numeric or choice-type planning item attribute such as Planned Cost, Priority, Score, etc.
        -   Read-only role
            -   Read-only role to access portfolio planning in view-only mode. The users with this role won't be able to create/edit portfolio plans and planning items.
        -   Portfolio Plan changes
            -   Copy portfolio plan
            -   Copy item, on the prioritization list
            -   Save the timescale selection on the roadmap timeline view
            -   New free-from roadmap configuration to control what tables to be availalbe for free-form roadmapping
        -   Financial planning on planning items
            -   Create financial baselines on demand or automatically capture the status of financial costs at any given time.
            -   Compare any two financial baselines to easily analyze the changes in cost and report what has caused the variance and when it occurred.
            -   Generate attribute-based labor costs for Demands based on the new resource assignments capability which enables flexible reporting of labor costs for your organizational needs.
        -   Capacity Planning
            -   Use rank of planning items for resource fulfillment in capacity planning.
            -   Filter on planning items in capacity planning.
            -   Warning icons and their interactions in capacity planning.
    -   Changed: Validations have been added for 'sn\_align\_ws.spw\_financial\_user' role, for users to access financial data like Planned costs, Actual costs, etc on the Prioritization list.
-   **Version 7.0.1 - September 2023**

    Fixed: Enhancing the Epic financials with rollup of financial fields value and showing the total values in Financials section.

-   **Version 7.0.0 - August 2023**
    -   -   Across all views of the Prioritization and Roadmap tabs at once. Only choice-list and reference-type fields are supported for filtering.
-   Use the planning attributes to configure the attributes by which you want to do capacity planning.
-   Generate capacity for the teams and different attribute combinations who work on items in a portfolio.
-   Regenerate the capacity in case you want to view the latest data.
-   Add high-level effort estimates using resource assignments on planning items to do capacity planning.
-   Define the set of resources on which you want to create capacity plans.
-   You can quickly view the work items and the capacity by attributes and teams along with the deficit/surplus in one view.
-   Create cost plans and expense lines for Financial planning of Demands and Projects.
-   Generate labor costs based on the resource assignments done for the planning items.
    -   Changed: Add multiple filters in the condition builder while creating a portfolio plan.
    -   Removed: Column-level filters in the Prioritization tab.
-   **Version 6.1.1 - June 2023**
    -   Fixed issues with portfolio planning sharing among users.
    -   The issue with the Hierarchy view of prioritisation with dot walk fields has been fixed.
    -   Entities with no planning items are by default hidden in the hierarchy.
-   **Version 6.1.0 - May 2023**
    -   New:
        -   Added diagnostics for lens setup and planning items global rank population to help ServiceNow admin troubleshoot the data discrepancies and fix them quickly.
        -   Ability to view Done and Cancelled planning items in the prioritization list view.
    -   Fixed:
        -   The Prioritization List view will not display converted demands anymore.
        -   Business stakeholder behavior is corrected. They can no longer create milestones in Portfolio Planning Workspace.
-   **Version 6.0.3 - March 2023**
    -   Fixed:
        -   Stakeholders are losing access to the portfolio plan after one of them edits the plan in strategic planning workspace.
        -   Filters in free-form roadmap creation wizard should use condition set.
-   **Version 6.0.1 - February 2023**

    Portfolio Planning \(formerly known as Alignment Planner Workspace\) provides a planning workspace for traditional portfolio planning to prioritize demand and projects as well as visualize them on the roadmap and track their progress.


