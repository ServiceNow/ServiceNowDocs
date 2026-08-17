---
title: Strategic Planning release notes
description: The ServiceNow Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-07-07"
reading_time_minutes: 20
---

# Strategic Planning release notes

The ServiceNow® Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Australia release.

## Strategic Planning highlights for the Australia release

-   Identify similar demand records in Next Experience for Demand Management based on contextual similarity in the name, description, and business case content using the identify similar records AI skill.
-   View and manage cost plans, benefit plans, and expense lines directly from the demand records in the Financials page in Next Experience for Demand Management.
-   Monitor demand distribution, financials, and data quality at a glance using Dashboard in Next Experience for Demand Management.
-   Create and manage demands from the Next Experience for Demand Management in Strategic Planning. Guide demand managers and users through predefined stages and actions for each demand process using Playbooks in Next Experience for Demand Management.
-   Link AI systems to a demand using a playbook activity in Next Experience for Demand Management. Generate a concise summary of a demand using the demand summarization skill.
-   Use boards in Strategy and Goals to group and manage strategic priorities and objectives for your organization. Use the goal insights skill to generate insights for goals to gain predictive, actionable visibility into goal health.
-   Send notifications to target owners or contributors to ensure timely updates of target actuals. Define targets across multiple organizational levels with the Assigned entity field in the target form.
-   Consistent financial reporting across all baselines by support of investment currency on migrated financial baselines.
-   Simplified user experience and focus on investment level financials view on investment currency fields for new customers. Complete and accurate currency data in all financial baselines for existing customers are now upgraded to include investment currency values.

See [Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/alignment-planner-workspace-landing-page.md) for more information.

**Important:** Strategic Planning is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   **[Financials grid for demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/managing-financials-dw.md)**

    Next Experience for Demand Management includes a Financials grid for demand records. This grid shows the demand's cost plans, benefit plans, and baselines. From this grid, users can:

    -   Add cost plans, benefit plans, and expense lines scoped to the demand.
    -   Create and compare baselines for financial data on the demand.
    -   Filter by time scope and personalize the grid columns.
-   **[Demands Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/c_demand_dashboards.md)**

    Next Experience for Demand Management includes a Dashboard menu for demand records. The dashboard opens by default and is organized into three tabs:

    -   Overview
    -   Financials
    -   Data Quality
    Filter dashboard data by department, business unit, portfolio, program, or demand manager. Select a widget, or select **View all** on a list widget, to open the underlying records with the same filters applied.

-   **[Identify similar demands using AI in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/identify-similar-demand-records.md)**

    Detect similar existing demand records when creating or editing a demand using the identify similar records skill. This skill compares the Name, Description, and Business Case fields for contextual similarity.

-   **[RIDAC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/spw-ridac-landing.md)**
    -   Create and associate risks, issues, decisions, actions, and changes \(RIDAC\) with all planning items, goals, and EAP \(Enterprise Agile Planning\) iterations to track planning uncertainties.
    -   Access a dedicated RIDAC menu in Strategic Planning Workspace for quick navigation to RIDAC items.
    -   Manage RIDAC items with granular role-based access—assign read-only or full edit access to team members based on their responsibilities.
    -   Run the scheduled job to populate the planning item field on the existing RIDAC records that were created earlier.
    -   Track RIDAC across multiple scopes—view all RIDAC, project-specific RIDAC, portfolio RIDAC, and program RIDAC in a single unified view.
-   **[Epic status assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/assess-epic-status-now-assist-eap.md)**

    Automatically evaluate epic health across six risk dimensions using the Epic status assessment skill in Enterprise Agile Planning. Now Assist analyzes story health, blocked stories, dependencies, progress, timeline, and ownership to return a red, yellow, or green status with plain-English reasoning. Portfolio managers can quickly assess epic risks without manually reviewing stories, timelines, and assignments by selecting the **Epic status** button on the epic record page.

-   **[AI-generated insights for portfolio plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/view-portfolio-insights.md)**

    Gain AI-generated insights for planning items within a portfolio plan using the Portfolio insights skill. Identify planning items that are delayed beyond their planned end date, have delayed starts, or have misalignments between planned and approved dates. Monitor active projects that show early risk indicators but have not yet experienced delays.View AI-generated top root causes and recommended actions for each insight category to help address delays and misalignments effectively.

    The AI Insights window displays a timestamp indicating when insights were last generated. You can regenerate insights and recommendations if required to see the changes based on the latest available data.

    Users with the sn\_align\_core.apw\_admin role can configure severity thresholds and scoring factors for planning items. These settings control how the Portfolio insights skill classifies insight severity as Critical, Medium, or Low.

-   **[Story generation for epics in Agile Development 2.0 and EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/generate-stories-quickly-for-eap-and-agile-2-0.md)**

    Generate a complete user story, including title, description, and acceptance criteria, directly from an epic instead of creating one. By providing one or two lines of context, you can generate a story and edit inline before saving. This skill is available in both Agile Development 2.0 and EAP.

-   **[Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-workspace.md)**

    Next Experience for Demand Management delivers a unified experience for managing strategic and operational demands in Strategic Planning. This Next Experience interface consolidates demand creation, assessment, collaboration, and conversion in one place, eliminating context switching and reducing reliance on the classic Demand Workbench.

-   **[Create and manage demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/use-demands-dmnd-wpc.md)**
    -   Create and manage a demand in Next Experience for Demand Management using guided tabs that help you define alignment, estimate costs, and confirm readiness as you build out the demand.
    -   Collaborate on demands through Docs, with execution and planning synced.
    -   View, add, and edit cost plans and budgeting details using related lists.
-   **[Use Playbooks in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/use-playbooks-in-dw.md)**

    Help teams manage demands with greater structure and consistency using Playbook in Next Experience for Demand Management.

    Playbooks enable you to define multiple governance processes across the organization using a low‑code/no‑code configuration experience. Create clear stages and guided activities from demand intake to completion using a default playbook or a custom playbook. Custom playbooks support multiple demand management processes across your organization’s multiple demand management processes.

-   **[Associate AI systems with demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/use-playbooks-in-dw.md)**

    Use a playbook activity in Next Experience for Demand Management to associate AI systems with a demand. You can link impacted systems and add new ones directly within the demand workflow.

-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/summarize-demand-in-demand-workspace.md)**

    Generate a concise, structured summary of any demand using the demand summarization skill through the **Summarize** button in the demand form. The skill reviews the demand fields and helps create a clear summary of the demand.

-   **[Strategy and Goals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategy-goals-landing-page.md)**

    Use boards in Strategy and Goals to organize and manage your organization’s strategic priorities and objectives. A board is a collection of strategic plans, priorities, objectives, and key results based on your selected filter criteria—helping you stay focused and manage them effectively.

    -   Managing boards:
        -   Create boards step by step, choosing whether to base them on strategic plans, priorities, goals, or both. Define what items to display using advanced filter conditions.
        -   Build boards tailored to specific goals by entity type and entity, ensuring focus on the goals that matter most.
        -   Share boards with stakeholders to align efforts and drive shared outcomes.
        -   Add boards to your favorites for faster navigation.
    -   Managing strategy and goals using boards:
        -   Create and organize strategic plans, strategic priorities, goals, and key results in a single, focused view.
        -   Associate work or planning items with goals or targets to align your current or future work with your strategic priorities, helping your team achieve goals and targets efficiently.
        -   As the goal or process owner, send notifications to target owners or contributors to ensure timely updates of target actuals.
        -   Target owners and contributors receive reminder notifications for check-in updates before the due date.
        -   With ServiceNow Otto for Strategic Portfolio Management, generate measurable targets for your goals to reduce the effort of defining clear success criteria, and gain actionable insights to identify at‑risk goals, assess forecasted status, and act on AI‑driven recommendations.
-   **AI-generated insights for goals**
    -   Generate AI‑powered insights using the goal insights skill to gain predictive, actionable visibility into goal health. By analyzing the goal, goal targets, subgoals, and aligned work, the system delivers data‑driven insights that help goal owners and contributors manage risks proactively and improve goal outcomes. Insights include AI-forecasted status, confidence of achieving the goal, targets at risk, and aligned work or recommendations that have been delayed or stalled.
    -   View the AI-forecasted status for goals and targets in the grid, generated automatically via the Goal insights generation scheduled job, along with the rationale for the generated status.
    -   Configure run frequency and set of goals to run the Goal insights generation scheduled job as need. The job is inactive by default.
-   **[Portfolio plan goals enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/managing-goals-in-alignment-planner-workspace.md)**
    -   Owners and contributors are notified when they’re mentioned in a goal, target, or when comments are added.
    -   Define targets across multiple organizational levels with the Assigned entity field in the target form. This enables targets created at higher levels \(for example, Company\) to be directly assigned to lower levels \(for example, Business Unit, Department\), eliminating redundant subgoal creation, and streamlining overall goal management.
    -   Status — **Green**, **Yellow**, **Red**, or **None** — rolls up automatically from target breakdowns to the target for targets set to cumulative distribution, and from targets and subgoals to the goal.
-   **[Portfolio plan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/create-portfolio-plans-in-alignment-planner-workspace.md)**
    -   Visualize planning items in lanes with the new Kanban tab in the Planning page and access the Hierarchy tab directly from the same location. These tabs replace the previous access point in the Prioritization tab, offering a more streamlined way to view and manage planning items.
    -   Save filter views specific to the Kanban tab and the Hierarchy tab without affecting views in the Prioritization tab.
    -   View planning items in the new Hierarchy tab on the Planning page, now sorted using global rank when available. Drag and drop is supported for lowest‑level items, enabling you to rerank them within their groups.
    -   Share a portfolio plan using the Copy link option. This provides access to existing users who have access to the portfolio plan.
    -   Make a portfolio plan public and share the copied link with Strategic Planning Workspace users, without inviting them individually or as a group. Note that users accessing a public portfolio plan with the shared link cannot view scenarios within the plan.
    -   Expand or collapse portfolio plan header to maximize screen space while planning.
    -   Edit the default view within a portfolio plan and save changes using the Save view option.
    -   View additional status attributes — cost, resource, schedule, and scope — for planning items in Strategic Planning Workspace. For project planning items, these attributes are synced automatically from the latest published project status report. For other planning items, these attributes can be set manually. Note that project status report attributes synced from the Project status \(project\_status\) table are read-only in Strategic Planning Workspace and can't be edited directly.
    -   Set planning item status to **No status** when a status has not been determined, in addition to the existing **Green**, **Yellow**, and **Red** values, giving planners the flexibility to update the status as needed. By default, the status is set **No status** when a planning item is created.
    -   Display rollup bars at parent levels in the hierarchy view and choose the date type to display — approved, planned, or actual. Use the comparison option to compare date types, such as approved versus planned dates, to identify schedule misalignments.
-   **[Plan efficiently with additional pre-defined lenses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/lens-alignment-planner-workspace.md)**

    Use the Planning item lens to plan, prioritize, and roadmap work in Strategic Planning Workspace directly with planning items, without configuring organization structure, programs, portfolios, or products. The lens supports all enabled work item types, such as projects and demands, and can be used as a standalone lens or alongside other lenses.

-   **[Hierarchy tab for EAP teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/eap-hierarchy-tab.md)**

    Gain visibility into how your work connects to broader organizational goals by viewing the complete work item hierarchy directly in the EAP workspace. Expand any epic to see its capabilities, features, and stories across Solution Trains, ARTs, and Agile Teams without switching between multiple screens or running separate reports.

    Customize your view by selecting which columns appear in the hierarchy grid and adjusting column widths to match your workflow. Your column preferences persist across sessions, so your configured view is ready each time you return.

    The Hierarchy tab requires your admin to enable it through the **sn\_apw\_advanced.enable\_hierarchy\_view** system property. See [Enable Hierarchy tab in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/hierarchy-enable-eap.md).

-   **[Open EAP work items in new browser tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/using-eap.md)**

    Open work items from the EAP Backlog and Hierarchy pages in a new browser tab, so you never lose your context. Right-click any work item, or use the item options menu, to open its full details in a separate tab. This feature lets you review and compare multiple work items side by side without losing your current view.

-   **[Move work items to the top or bottom in EAP Backlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/schedule-work-items-into-iterations-in-eap-backlog.md)**

    Promote an urgent story to the top of a sprint or push deprioritized work to the bottom of a long backlog without dragging items across multiple pages. Right-click any story, feature, capability, or epic in the EAP Backlog, iteration, or team grid and select **Move to top** or **Move to bottom** to re-prioritize the work item in one action. Prioritization changes take effect across all pages, so you can act on shifting priorities even when the work item is far from its target position.

-   **[Live updates in the EAP Hierarchy tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/eap-hierarchy-tab.md)**

    Keep working in your hierarchy without breaking your flow each time you create a work item. When you create a work item with the Hierarchy tab open, it is added to your current view immediately, so you don't need to refresh the page to see a new story, feature, capability, or epic. A new top-level item appears alongside the existing top-level items for the selected portfolio configuration. A new child item appears under its parent when that parent is expanded.

-   **[Active work first in the EAP Backlog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/using-eap.md)**

    Plan and prioritize without sifting through completed or cancelled work. The Backlog section of the EAP Backlog tab now hides completed and cancelled work items by default, so the list shows only what your teams have to work on. Sprint and Planning Interval \(PI\) sections continue to show all work items, giving you visibility into both ongoing and finished work for each iteration.

    Admins can change these settings for either sections using two new system properties: `sn_apw_advanced.show_inactive_items_in_backlog_list` for the Backlog section and `sn_apw_advanced.show_inactive_items_in_iteration` for iteration sections.

-   **[Refresh without losing your place in the EAP Hierarchy tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/eap-hierarchy-tab.md)**

    Selecting Refresh in the Hierarchy tab now reloads your data without collapsing the rows you've already expanded or resetting your scroll position. Rows deleted by someone else are removed silently, and new child items appear under their expanded parent. If the grid displays more than 100 non-root items or 100 stories, you're asked to confirm before all rows are collapsed.

-   **[View or delete a dependency directly from the EAP Planning board](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/work-item-dependencies-in-eap.md)**

    Select a dependency line on the Planning board to open the dependency record in a side panel, without navigating to the work item's full details page. Review the dependent and prerequisite items, or select **Delete** to remove the dependency directly from the panel.

-   **[Backlog and Hierarchy access for CWM connected teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/integrate-eap-with-collaborative-work-management.md)**

    Teams connected to CWM can now access the Backlog and Hierarchy tabs in EAP. Because sprints are started and completed from the CWM Board, the **Start Sprint** and **Complete Sprint** options are hidden in the EAP Backlog for these teams.

-   **[Creating iterations for teams in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/simplified-iteration-creation-in-eap.md)**

    From EAP version 4.17.0, create Planning Intervals and Sprints directly from the Backlog by entering their start and end dates. The underlying planning calendar entries are created for you, so nobody has to define them before teams can plan.

    The following capabilities support this flow:

    -   Users with the new `sn_apw_advanced.eap_scrum_master` role create the first iteration for a set of teams that share a planning calendar. After that timeline exists, users with the `sn_apw_advanced.eap_user` role create the following iterations for the other ARTs and teams that share it.
    -   Select **Have unique calendars** on an EAP configuration to give each ART that you add afterward its own planning calendar. By default, the ARTs in a configuration share one calendar and follow one cadence.
    -   When an Agile Team joins an ART, the in-progress Sprint and the upcoming Sprints are created for that team automatically.
    -   Planning calendar entries that your admin defined earlier remain valid. Teams can continue to create iterations within the timelines that those entries define.
-   **[Admin role enhancements in Feedback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/components-installed-with-product-feedback.md)**

    The read role sn\_align\_core.pf\_read and write role sn\_align\_core.apw\_admin are added to the following system properties in Feedback and Product idea:

    -   sn\_apw\_advanced.product\_feedback\_allowed\_non\_planning\_items\_for\_link\_item
    -   sn\_apw\_advanced.product\_feedback\_product\_idea\_filters
    -   sn\_apw\_advanced.product\_feedback\_feedback\_filters
    -   sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address
-   **[Financials for planning items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/using-financials-spw.md)**
    -   Migration of financial baselines:
        -   Migrate the financial baselines of projects, which includes investment currency support.
        -   While migration, financial baselines will now include actuals, costs, benefits, and budget values from the project currency to the investment currency.
    -   Streamlined currency fields while using multicurrency:
        -   New and existing customers will now see only investment currency fields in demand and project records.
        -   Planned costs, actual costs, planned benefits, actual benefits, and budget fields are included in the financial baselines.

## UI changes

-   **[Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-workspace.md)**
    -   The Demands icon has been added to the Strategic Planning L1 menu to open the All Demands home page.
    -   The **State** field on the **All Demands** page has been color-coded for each state value.
    -   The **Playbook**, **Details**, and **Docs** tabs have been added to the L2 menu of each demand to clearly and consistently group information.
        -   The **Details** tab has been added to add and manage demand information such as financials and resource assignments.
        -   The **Playbook** tab has been added to define clear stages and guided activities to read and follow. Selecting the name of a stage or activity navigates you to that stage or activity in the playbook. The **Skip**, **Update**, and **Mark Complete** options have been added to the activities of the playbook.
        -   The **Docs** tab has been added to view and manage the documentation on the demand.
    -   If you have the AI Control Tower plugin installed and the investment type of the demand is set to artificial intelligence:
        -   The **AI Associations** section in the Demand details is displayed. The following fields are included:
            -   **Product**: Enables you to select the product or system that the demand relates to.
            -   **Impacted AI systems**: Links the impacted AI systems with the demand. You can select existing AI systems from the list or remove systems that are no longer relevant.
        -   The **AI Checkpoint** stage is added to the demand default playbook. This stage includes the **Product** and **Impacted AI systems** fields.
        -   The **Create AI System** option is added to the **Details** page of a demand for users with the sn\_ai\_steward role.
    -   [Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)The **Financials** grid is added to the navigation menu of a demand. It has options to create cost plans, monetary benefits plans, expense lines, and create and compare baselines.
    -   The **Dashboards** menu item is added for demands, providing **Overview**, **Financials**, and **Data Quality** tabs.
    -   The following items have been added to the demand form and are available if you have the identify similar records AI skill activated:
        -   The **Identify similar demands** button, which identifies and displays similar demands.
        -   The **Similar Demands** tab in **Details**, which displays the list of similar demand records identified by AI.
    -   The **AI Overview** tab is added to the navigation menu of a demand. It generates a demand summary on landing if the skill trigger is set to automatic. If the trigger is set to manual, a **Summarize** button is available to generate the summary.
-   **[Changes to Target form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/target-form-egm.md)**

    The following fields have been added to the Target form to support defining targets at multiple organizational levels.

    -   **Assigned entity**
    -   **Company**
    -   **Business Unit**
    -   **Department**
    -   **Portfolio**
    -   **Product model**
    -   **Value stream**
    -   **Initiative**
    -   **Strategic Program**
-   **[Changes to Strategic Priority form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-priority-form.md)**

    The **Status** field has been added to the Strategic Priority form, enabling you to set the status of a strategic priority as **None**, **Green**, **Yellow**, or **Red**.

-   **[Hierarchy and List views in Prioritization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/managing-backlog-alignment-planner-workspace.md)**

    The **Kanban** and **Hierarchy** views have been removed from the Prioritization page and are now available as separate tabs in the Planning page. This change improves navigation by consolidating all planning-related views in one place.


## Changed in this release

[Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md)

-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **[Demand summarization skill enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-summary-demand-classic.md)**

    The demand summarization skill incorporates data from related entities when generating a summary. In addition to demand record fields, the summary includes insights from demand tasks, cost plans, monetary and non-monetary benefit plans, resource assignments, and work notes. The generated summary covers business requirements, timeline, risks, stakeholder comments, cost, effort, monetary and non-monetary benefits, and ROI.

-   **[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/summarize-demand-in-demand-workspace.md)**

    The demand summary is generated in the **AI Overview** tab instead of the **Details** tab. The skill is set to trigger automatically, that is, the summary is generated on landing in this tab. Auto-generation is on by default and applies to demands in Submitted, Screening, Qualified, or Approved states. You can define the trigger to manually trigger as well, where users must select the **Summarize** button to generate the summary.

-   **[AI skills for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/similar-demand-identification-using-now-assist.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[Access execution records from Portfolio Plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/access-demands-from-portfolio-plan-spw.md)**

    The execution URL is updated on the planning item demand. New planning items demand will automatically use the new execution URL. The execution URLs on existing planning item demands continue to work but doesn't reflect the updated navigation. Run the **Update Demand Planning Item Execution URL** scheduled job to update the execution URL on the existing demands.

-   **[Components installed with Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/components-installed-with-enterprise-agile-planning.md)**

    The EAP role hierarchy is updated. The `sn_apw_advanced.eap_admin` role now contains `sn_apw_advanced.eap_scrum_master`, which in turn contains `sn_apw_advanced.eap_user`. The `sn_apw_advanced.eap_admin` role no longer contains `sn_apw_advanced.eap_user` directly.

    As a result, the following actions require the `sn_apw_advanced.eap_scrum_master` role:

    -   Changing the start date or the end date of an iteration.
    -   Creating, editing, and deleting planning calendars and calendar spans.
    Because `sn_apw_advanced.eap_admin` contains `sn_apw_advanced.eap_scrum_master`, users with the admin role keep access to these actions.


## Activation information

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower-landing.md)**

    ServiceNow AI Control Tower enables you to track and monitor all your strategic priorities, goals, targets, planning items, and execution items—projects and demands categorized as Artificial Intelligence in the Strategic Planning Workspace.

-   **[ServiceNow Otto for Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-spm.md)**

    Now Assist enables you to use generative AI skills in multiple SPM apps. With Now Assist for SPM, summarize product feedback, create stories for epics, and generate concise project summaries. You can also rephrase content for docs, create demands through a conversational experience, and gain insights into projects.

-   **[Digital Product Release Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/dpr-workspace.md)**

    ServiceNow Digital Product Release Workspace helps product managers track the planning items associated with the product enhancements that are defined in the Strategic Planning Workspace using the Digital Product lens.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-business-management-rn-landing.md)

