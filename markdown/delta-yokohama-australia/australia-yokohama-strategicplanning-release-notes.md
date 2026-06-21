---
title: Combined Strategic Planning release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Strategic Planning from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-strategicplanning-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 27
breadcrumb: [Products combined by family]
---

# Combined Strategic Planning release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Strategic Planning from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Strategic Planning release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Strategic Planning to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

After upgrading to Strategic Planning v4.7.0, the following changes apply to user preferences:

-   Custom view settings previously saved under user preferences will be cleared. You must reapply these changes and create views as needed. For instructions, see [Create a portfolio plan view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-portfolio-plan-view-spw&family=yokohama&ft:locale=en-US) and [Create a free-form roadmap view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-free-form-roadmap-view-spw&family=yokohama&ft:locale=en-US).
-   Customizations made to the Timeline and Kanban views in the **Roadmap** tab, and the Kanban view in the **Prioritization** tab at the portfolio plan level, will be copied to the Default view of the portfolio plan. Similarly, any customizations made to the Timeline and Kanban views in the free-form roadmap will also be copied to the Default view of the free-form roadmap.

</td></tr><tr><td>

Zurich

</td><td>

After upgrading to Strategic Planning v4.8.0, the existing **Investment type** and **Investment class** fields will appear as **Investment type \(Deprecated\)** and **Investment class \(Deprecated\)** respectively across the Planning page including in the Prioritization and Roadmap views and in the Scenario Planning page. The values from these deprecated fields will be automatically copied to the new **Investment type** and **Investment class** fields.

 If you previously applied filters or personalized your view using the deprecated fields, you must update those configurations to use the new **Investment type** and **Investment class** fields across the workspace—including in the Prioritization and Roadmap views on the Planning page, as well as in the Scenario Planning page.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Strategic Planning.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Dashboards for data analysis and decision-making](https://www.servicenow.com/docs/access?context=dashboards-in-spw&family=yokohama&ft:locale=en-US)**

Use dashboards to view key data and metrics, enabling you to monitor performance, track progress, and make informed decisions related to ideas, feedback, planning, and execution. Dashboards consolidate data from multiple sources into a single, easily digestible format. Each widget within a dashboard displays key data and metrics and may include visualizations. The default dashboards include the Product Idea Dashboard, Feedback Dashboard, Strategy Execution Dashboard, and Execution Dashboard.

You can create or edit dashboards, copy an existing dashboard and customize it as needed, and share dashboards to collaborate with business stakeholders who have access to the portfolio plan.

-   **[Create and share views for portfolio plans and free-form roadmaps](https://www.servicenow.com/docs/access?context=managing-portfolio-plan-views-spw&family=yokohama&ft:locale=en-US)**

For portfolio plans - Create, edit, and switch between views with display preferences such as column selection, grouping, and filtering for portfolio plans. You can create personal views that are private to you, or public views that can be shared with stakeholders who have access to the portfolio plan. The portfolio plan view saves your display preferences across the **Prioritization**, **Roadmap**, **Capacity**, and **Financials** tabs.

**Note:** Views are available only for the Planning module and are supported in live mode, but not in scenario mode.

For free-form roadmaps - Create, edit, and switch between views with display preferences such as grouping, milestones selection, dependencies selection, and tracking mode for free-form roadmaps. You can create personal views that are private to you, or public views that can be shared with stakeholders who have access to the free-form roadmap.

-   **[Write planning item skill](https://www.servicenow.com/docs/access?context=refine-text-with-write-planning-item-skill&family=yokohama&ft:locale=en-US)**
    -   Improve record quality and user satisfaction by enabling AI assistance in the **Description** field across all Strategic Planning Workspace forms, including product idea, demand, epic, project, capability, feature, and story.
    -   Enable text refinement with the **Elaborate** and **Shorten** options on planning items to support product managers and agile team members in creating and editing content more effectively.
-   **[Plan efficiently with additional pre-defined lenses](https://www.servicenow.com/docs/access?context=lens-alignment-planner-workspace&family=yokohama&ft:locale=en-US)**

Using the Digital Product lens, portfolio managers can plan, prioritize, and roadmap the work in the Strategic Planning Workspace based on the digital products by aligning with the business strategy.

The lens is supported with the work items, epic, and product idea. With the Digital Product lens, you can also do high-level planning using the Product Enhancement entity. By default, the Product Enhancement entity is enabled for high-level planning.

-   **[Cycle time report for Agile teams in EAP dashboards](https://www.servicenow.com/docs/access?context=eap-agile-team-dashboard&family=yokohama&ft:locale=en-US)**

Analyze how long the stories take for your Agile team to move from an in-progress state to completion. Each bubble on the chart represents a story and the chart shows stories completed in the past 30 days. You can compare the cycle times of stories that have different story points and review the trend in the time taken by the team to complete them.

Using this data, identify the stories that took longer to complete and analyze the reasons so that you can draft an action plan to optimize the team's cycle time in the future.

-   **[Kanban configuration for EAP teams](https://www.servicenow.com/docs/access?context=agile-configurations-in-eap&family=yokohama&ft:locale=en-US)**

Use the Kanban configuration for teams that don't prefer to work in an iteration-based schedule. You can activate the predefined Kanban configuration and add teams to your Agile structure or you can modify an existing configuration by setting the **Planning calendar** field to **None**.

-   **[Column filters in EAP Backlog](https://www.servicenow.com/docs/access?context=using-eap&family=yokohama&ft:locale=en-US)**

Quickly find the work items that you need by using column-level filters for the data on your EAP Backlog. You can filter on any column that is displayed on the **Backlog** tab.

-   **[Generate stories from epics and features using Now Assist for EAP](https://www.servicenow.com/docs/access?context=generate-stories-from-epics-now-assist-eap&family=yokohama&ft:locale=en-US)**

Break down epics and features into stories using the Now Assist Agile story generation skill in the EAP workspace. Using the available details such as name, description, docs content, and any existing stories, Now Assist provides story recommendations for your epic or feature. You can let Now Assist generate stories using its initial recommendations or you can choose to split or combine the story recommendations before prompting Now Assist to create the stories.

-   **[View financial data of your planning items at portfolio level](https://www.servicenow.com/docs/access?context=using-portfolio-financials-spw&family=yokohama&ft:locale=en-US)**
    -   View the rolled-up financial costs and benefits data of your planning items such as Epics, Demands, and Projects at the portfolio level for different time scales and ranges.
    -   View the Budget, Planned, Variance, Actuals, and Remaining Estimates of the financials costs by expense type or cost type.
    -   View the Forecasts, Actuals, and Variance of monetary benefits.
-   **[Create a manage financial scenarios of planning items](https://www.servicenow.com/docs/access?context=optimizing-scenarios-in-strategic-planning&family=yokohama&ft:locale=en-US)**
    -   Optimize your portfolio by creating financial scenarios to validate and arrive at a profitable outcome.
    -   Plan and manage the budget of planning items in simulation mode for efficient financial planning and to help prevent overspending.
    -   Manage prioritization and budget allocation of the planning items to meet business priorities.
    -   Compare scenarios financially and automatically allocate the planned budget to planning items from approved scenarios.
    -   Enable the **new budget allocation** property \(**sn\_invst\_pln.enable\_budget\_allocation\_v2**\) to perform financial analysis in scenario planning and take effective decisions by data-driven insights.
-   **[Real-time collaboration for EAP Docs](https://www.servicenow.com/docs/access?context=docs-for-eap-teams-and-planning-items&family=yokohama&ft:locale=en-US)**

Edit a doc page concurrently with multiple other editors. Colored cursors denote the current location of editors on the page. You can choose to show or hide these indicators.

The real-time collaboration feature for docs is also available for planning items in the Strategic Planning Workspace. See [Docs for planning items](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&family=yokohama&ft:locale=en-US).

**Note:** To use the full functionality of Docs v6.6.0 within Strategic Planning Workspace, ensure that you upgrade Strategic Planning Workspace to v4.5.0. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).


</td></tr><tr><td>

Zurich

</td><td>

-   **[Strategic Planning and AI Control Tower](https://www.servicenow.com/docs/access?context=better-together-with-other-apps-spw&family=zurich&ft:locale=en-US)**

Categorize your strategic priorities, goals, planning items, and execution items—projects and demands as Artificial Intelligence to track and monitor strategy progress from the AI Control Tower workspace.

Use the **Type** field for strategic priorities, the **Category** field for goals, the **Investment type** field for planning items - to classify them as Artificial Intelligence and monitor their progress in the AI Control Tower workspace.

-   **[Integrate Enterprise Agile Planning \(EAP\) with Atlassian Jira](https://www.servicenow.com/docs/access?context=spw-jira-landing&family=zurich&ft:locale=en-US)**

Facilitate execution of the work planned in EAP and executed in Jira. With this integration, enable seamless tracking of work across tools with bidirectional sync between Jira and EAP. Key updates made in one system, such as a status change or field update for Epics and Stories, will automatically reflect in the other. This integration ensures your team can collaborate and track development efforts without switching contexts, reducing manual effort and improving visibility across platforms.

-   **[Enterprise Agile Planning \(EAP\) integration with CWM](https://www.servicenow.com/docs/access?context=agile-sprint-planning-in-cwm&family=zurich&ft:locale=en-US)**

Enhance visibility, planning, and execution for your teams with seamless integration between EAP and CWM.

For Agile teams managing non-agile work items such as incidents and change tasks, this integration bridges the gap by automatically creating a dedicated Space and Board in CWM. Agile work is seamlessly brought over via Connected Work, while EAP sprints are reflected directly in CWM’s Sprint planning view, thus enabling unified planning across work types. Teams can plan work for their sprints and update work status directly from the CWM Board, with performance reports in EAP dynamically reflecting these changes. This integration enables teams to manage their full scope of work from a single, connected workspace.

-   **[Dynamic data linking in Docs](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&family=zurich&ft:locale=en-US)**

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Portfolio plan enhancements](https://www.servicenow.com/docs/access?context=create-portfolio-plans-in-alignment-planner-workspace&family=zurich&ft:locale=en-US)**
    -   Create portfolio plans for AI-related items by applying a filter on the planning item tables, setting the **Investment type** field value to **Artificial Intelligence** during portfolio plan creation. This allows you to focus exclusively on AI-related items.
    -   With the sn\_align\_core.apw\_admin role, you can update the following system properties:
        -   **sn\_align\_core.planning\_item\_types\_allow\_list** - Defines the planning item types that can be configured and allowed for a portfolio plan.
        -   **glide.ui.sn\_align\_core\_dependency\_activity.fields** - Enables activity stream for the dependency formatter fields.
        -   **sn\_align\_ws.gantt\_show\_higher\_planning\_upper\_entities** - Enables display of entire hierarchy of lens structure from top to bottom in prioritization hierarchy view for high-level portfolio plans.
        -   **sn\_align\_ws.portfolio\_plan\_items\_limit** - Defines the number of planning items to be loaded on the planning page.
-   **[Roadmap enhancements](https://www.servicenow.com/docs/access?context=roadmaps-in-alignment-planner-workspace&family=zurich&ft:locale=en-US)**
    -   Create custom themes for your roadmap bar colors to align with your organization’s standards.
    -   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans.
    -   View the roadmap-level milestone row while scrolling down the Roadmap page.
    -   Use different icons to distinguish item-level milestones.
    -   Match milestone colors with their status labels across the roadmap, milestone popover, and side panel. For example, a missed milestone displays the same color in all locations.
    -   With the sn\_align\_core.apw\_admin role, you can define the number of milestone items to be loaded in the Roadmap tab. The **sn\_align\_ws.item\_milestone\_limit** system property allows you to define the number of milestone items to be loaded in the Roadmap tab.
    -   With the sn\_align\_core.apw\_admin role, you can define the list of planning item types that can be created in a free-form roadmap. The **sn\_align\_ws.freeform\_planning\_items\_creation\_list** system property allows you to define the list of planning item types that can be created in a free-form roadmap.
-   **[Scenario planning enhancements](https://www.servicenow.com/docs/access?context=enable-scenario-planning-in-strategic-planning&family=zurich&ft:locale=en-US)**

With the sn\_align\_core.apw\_admin role, you can enable or disable the scenario planning feature. The **sn\_align\_ws.is\_scenario\_planning\_disabled** system property allows you to enable or disable the scenario planning feature.

-   **[Quick filters enhancements](https://www.servicenow.com/docs/access?context=managing-backlog-alignment-planner-workspace&family=zurich&ft:locale=en-US)**

Apply filters using string-type and boolean field values across the Planning page and Scoring page to view the required dataset. These filters are saved as part of your user preferences, enabling you to access the same filtered data when you log back in and continue your planning seamlessly.

-   **[Investment type and Investment class fields on the Planning item table](https://www.servicenow.com/docs/access?context=planning-item-form&family=zurich&ft:locale=en-US)**

The **Investment type** and **Investment class** fields have been added to the Planning item \[sn\_align\_core\_planning\_item\] table to enable these attributes to be defined at the parent planning item level.

A new value, **Artificial Intelligence**, has also been added to the **Investment type** field to categorize a planning item as an Artificial Intelligence initiative.

-   **[Goal management enhancements](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&family=zurich&ft:locale=en-US)**
    -   With the sn\_gf\_goal\_admin role, you can update goal-specific system properties:
        -   **sn\_align\_ws.goal\_hierarchy.max\_records** - Defines the number of targets to load on the Hierarchy tab in the Targets view. The default value is 250.
        -   **glide.ui.sn\_gf\_goal\_activity.fields** - Enables activity stream for fields of the goals.
    -   Experience faster loading of goals data, even when large volumes of data are present.
    -   With the sn\_gf.goal\_admin role, you can edit any goal and target as needed, even when you aren’t the owner or contributor of a goal or target.
    -   With both the sn\_gf\_goal\_admin and sn\_apw\_advanced.spw\_goal\_user roles, you can edit target breakdowns as needed.
-   **[Financial enhancements](https://www.servicenow.com/docs/access?context=using-financials-spw&family=zurich&ft:locale=en-US)**
    -   View only the planned costs of your planning items to track the total cost of your planning items.
    -   Use Display mode to switch between focused views to better plan and track the financials of your planning items.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate and track labor cost for sub-projects, based on the resource assignments of your sub-projects and planning items such as features and capabilities.

</td></tr><tr><td>

Australia

</td><td>

-   **[Epic status assessment](https://www.servicenow.com/docs/access?context=assess-epic-status-now-assist-eap&family=australia&ft:locale=en-US)**

Automatically evaluate epic health across six risk dimensions using the Epic status assessment skill in Enterprise Agile Planning. Now Assist analyzes story health, blocked stories, dependencies, progress, timeline, and ownership to return a red, yellow, or green status with plain-English reasoning. Portfolio managers can quickly assess epic risks without manually reviewing stories, timelines, and assignments by selecting the **Epic status** button on the epic record page.

-   **[AI-generated insights for portfolio plans](https://www.servicenow.com/docs/access?context=view-portfolio-insights&family=australia&ft:locale=en-US)**

Gain AI-generated insights for planning items within a portfolio plan using the Portfolio insights skill. Identify planning items that are delayed beyond their planned end date, have delayed starts, or have misalignments between planned and approved dates. Monitor active projects that show early risk indicators but have not yet experienced delays.View AI-generated top root causes and recommended actions for each insight category to help address delays and misalignments effectively.

Users with the sn\_align\_core.apw\_admin role assigned can configure severity thresholds and scoring factors for planning items to control how the Portfolio insights skill classifies insight severity as Critical, Medium, or Low.

-   **[Story generation for epics in Agile Development 2.0 and EAP](https://www.servicenow.com/docs/access?context=generate-stories-quickly-for-eap-and-agile-2-0&family=australia&ft:locale=en-US)**

Generate a complete user story, including title, description, and acceptance criteria, directly from an epic instead of creating one. By providing one or two lines of context, you can generate a story and edit inline before saving. This skill is available in both Agile Development 2.0 and EAP.

-   **[Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=demand-workspace&family=australia&ft:locale=en-US)**

Next Experience for Demand Management delivers a unified experience for managing strategic and operational demands in Strategic Planning. This Next Experience interface consolidates demand creation, assessment, collaboration, and conversion in one place, eliminating context switching and reducing reliance on the classic Demand Workbench.

-   **[Create and manage demands in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-demands-dmnd-wpc&family=australia&ft:locale=en-US)**
    -   Create and manage a demand in Next Experience for Demand Management using guided tabs that help you define alignment, estimate costs, and confirm readiness as you build out the demand.
    -   Collaborate on demands through Docs, with execution and planning synced.
    -   View, add, and edit cost plans and budgeting details using related lists.
-   **[Use Playbooks in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-playbooks-in-dw&family=australia&ft:locale=en-US)**

Help teams manage demands with greater structure and consistency using Playbook in Next Experience for Demand Management.

Playbooks enable you to define multiple governance processes across the organization using a low‑code/no‑code configuration experience. Create clear stages and guided activities from demand intake to completion by using a default playbook or creating a custom playbook to support your organization’s multiple demand management processes.

-   **[Associate AI systems with demands in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-playbooks-in-dw&family=australia&ft:locale=en-US)**

Use a playbook activity in Next Experience for Demand Management to associate AI systems with a demand. You can link impacted systems and add new ones directly within the demand workflow.

-   **[Summarize demands using Now Assist for SPM](https://www.servicenow.com/docs/access?context=summarize-demand-in-demand-workspace&family=australia&ft:locale=en-US)**

Generate a concise, structured summary of any demand using the demand summarization skill through the **Summarize** button in the demand form. The skill reviews the demand fields and helps create a clear summary of the demand.

-   **[Strategy and Goals](https://www.servicenow.com/docs/access?context=strategy-goals-landing-page&family=australia&ft:locale=en-US)**

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
        -   With Now Assist for Strategic Portfolio Management \(SPM\), generate measurable targets for your goals to reduce the effort of defining clear success criteria, and gain actionable insights to identify at‑risk goals, assess forecasted status, and act on AI‑driven recommendations.
-   **[AI-generated insights for goals](https://www.servicenow.com/docs/access?context=generate-insights-for-goal&family=australia&ft:locale=en-US)**
    -   Generate AI‑powered insights using the goal insights skill to gain predictive, actionable visibility into goal health. By analyzing the goal, goal targets, subgoals, and aligned work, the system delivers data‑driven insights that help goal owners and contributors manage risks proactively and improve goal outcomes. Insights include AI-forecasted status, confidence of achieving the goal, targets at risk, and aligned work or recommendations that have been delayed or stalled.
    -   View the AI-forecasted status for goals and targets in the grid, generated automatically via the Goal insights generation scheduled job, along with the rationale for the generated status.
    -   Configure run frequency and set of goals to run the Goal insights generation scheduled job as need. The job is inactive by default.
-   **[Portfolio plan goals enhancements](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&family=australia&ft:locale=en-US)**
    -   Owners and contributors are notified when they’re mentioned in a goal, target, or when comments are added.
    -   Define targets across multiple organizational levels with the Assigned entity field in the target form. This enables targets created at higher levels \(for example, Company\) to be directly assigned to lower levels \(for example, Business Unit, Department\), eliminating redundant subgoal creation, and streamlining overall goal management.
-   **[Portfolio plan enhancements](https://www.servicenow.com/docs/access?context=create-portfolio-plans-in-alignment-planner-workspace&family=australia&ft:locale=en-US)**
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
-   **[Plan efficiently with additional pre-defined lenses](https://www.servicenow.com/docs/access?context=lens-alignment-planner-workspace&family=australia&ft:locale=en-US)**

Use the Planning item lens to plan, prioritize, and roadmap work in Strategic Planning Workspace directly with planning items, without configuring organization structure, programs, portfolios, or products. The lens supports all enabled work item types, such as projects and demands, and can be used as a standalone lens or alongside other lenses.

-   **[Hierarchy tab for EAP teams](https://www.servicenow.com/docs/access?context=eap-hierarchy-tab&family=australia&ft:locale=en-US)**

Gain visibility into how your work connects to broader organizational goals by viewing the complete work item hierarchy directly in the EAP workspace. Expand any epic to see its capabilities, features, and stories across Solution Trains, ARTs, and Agile Teams without switching between multiple screens or running separate reports.

Customize your view by selecting which columns appear in the hierarchy grid and adjusting column widths to match your workflow. Your column preferences persist across sessions, so your configured view is ready each time you return.

The Hierarchy tab requires your admin to enable it through the **sn\_apw\_advanced.enable\_hierarchy\_view** system property. See [Enable Hierarchy tab in EAP](https://www.servicenow.com/docs/access?context=hierarchy-enable-eap&family=australia&ft:locale=en-US).

-   **[Open EAP work items in new browser tab](https://www.servicenow.com/docs/access?context=using-eap&family=australia&ft:locale=en-US)**

Open work items from the EAP Backlog and Hierarchy pages in a new browser tab, so you never lose your context. Right-click any work item, or use the item options menu, to open its full details in a separate tab. This feature lets you review and compare multiple work items side by side without losing your current view.

-   **[Move work items to the top or bottom in EAP Backlog](https://www.servicenow.com/docs/access?context=schedule-work-items-into-iterations-in-eap-backlog&family=australia&ft:locale=en-US)**

Promote an urgent story to the top of a sprint or push deprioritized work to the bottom of a long backlog without dragging items across multiple pages. Right-click any story, feature, capability, or epic in the EAP Backlog, iteration, or team grid and select **Move to top** or **Move to bottom** to re-prioritize the work item in one action. Prioritization changes take effect across all pages, so you can act on shifting priorities even when the work item is far from its target position.

-   **[Live updates in the EAP Hierarchy tab](https://www.servicenow.com/docs/access?context=eap-hierarchy-tab&family=australia&ft:locale=en-US)**

Keep working in your hierarchy without breaking your flow each time you create a work item. When you create a work item with the Hierarchy tab open, it is added to your current view immediately, so you don't need to refresh the page to see a new story, feature, capability, or epic. A new top-level item appears alongside the existing top-level items for the selected portfolio configuration. A new child item appears under its parent when that parent is expanded.

-   **[Active work first in the EAP Backlog](https://www.servicenow.com/docs/access?context=using-eap&family=australia&ft:locale=en-US)**

Plan and prioritize without sifting through completed or cancelled work. The Backlog section of the EAP Backlog tab now hides completed and cancelled work items by default, so the list shows only what your teams have to work on. Sprint and Planning Interval \(PI\) sections continue to show all work items, giving you visibility into both ongoing and finished work for each iteration.

Admins can change these settings for either sections using two new system properties: `sn_apw_advanced.show_inactive_items_in_backlog_list` for the Backlog section and `sn_apw_advanced.show_inactive_items_in_iteration` for iteration sections.

-   **[Admin role enhancements in Feedback](https://www.servicenow.com/docs/access?context=components-installed-with-product-feedback&family=australia&ft:locale=en-US)**

The read role sn\_align\_core.pf\_read and write role sn\_align\_core.apw\_admin are added to the following system properties in Feedback and Product idea:

    -   sn\_apw\_advanced.product\_feedback\_allowed\_non\_planning\_items\_for\_link\_item
    -   sn\_apw\_advanced.product\_feedback\_product\_idea\_filters
    -   sn\_apw\_advanced.product\_feedback\_feedback\_filters
    -   sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address
-   **[Financials for planning items](https://www.servicenow.com/docs/access?context=using-financials-spw&family=australia&ft:locale=en-US)**
    -   Migration of financial baselines:
        -   Migrate the financial baselines of projects, which includes investment currency support.
        -   While migration, financial baselines will now include actuals, costs, benefits, and budget values from the project currency to the investment currency.
    -   Streamlined currency fields while using multicurrency:
        -   New and existing customers will now see only investment currency fields in demand and project records.
        -   Planned costs, actual costs, planned benefits, actual benefits, and budget fields are included in the financial baselines.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Strategic Planning features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Changes in planning item forms](https://www.servicenow.com/docs/access?context=epic-form&family=yokohama&ft:locale=en-US)**

The dates in the **Planned start date** and **Planned end date** fields are editable for all planning item types other than Demand and Project planning item types. Also, the **State** field is editable for EAP planning items and its child items.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Investment type and Investment class fields](https://www.servicenow.com/docs/access?context=planning-item-form&family=zurich&ft:locale=en-US)**

The **Investment type** and **Investment class** fields have been deprecated from the Project and Demand planning item tables. These fields are now created at the parent level in the Planning item \[sn\_align\_core\_planning\_item\] table.

-   **[Goal management](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&family=zurich&ft:locale=en-US)**

By default, only active goals—those goals with the **Active** field set to **true**—are displayed across the workspace. This change applies to the **Dashboards** and **Goals and targets** tabs on the Goals page, the **Goal**/**Parent goal** reference fields in all applicable tables, and all relevant dashboards.

-   **[Default related list view changes for Stories](https://www.servicenow.com/docs/access?context=create-single-or-multiple-child-items-for-epic-in-eap&family=zurich&ft:locale=en-US)**

In the Stories list for an Epic, Feature, or Capability in the Enterprise Agile Planning workspace, the Assignment group and Sprint columns in the default related list view are replaced with the EAP team and Iteration columns.

-   **[Enhancements to tables in Docs](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&family=zurich&ft:locale=en-US)**
    -   Resize the column width of a table per your preference.
    -   Add color to single or multiple table cells.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 2](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   **[Demand summarization skill enhancements](https://www.servicenow.com/docs/access?context=demand-summary-demand-classic&family=australia&ft:locale=en-US)**

The demand summarization skill incorporates data from related entities when generating a summary. In addition to demand record fields, the summary includes insights from demand tasks, cost plans, monetary and non-monetary benefit plans, resource assignments, and work notes. The generated summary covers business requirements, timeline, risks, stakeholder comments, cost, effort, monetary and non-monetary benefits, and ROI.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Strategic Planning features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Strategic Planning features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

The **Investment class** and **Investment type** fields have been deprecated from the Project \[sn\_align\_core\_project\] and Demand \[sn\_align\_core\_demand\] tables.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Strategic Planning.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Strategic Planning by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Strategic Planning we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Strategic Planning we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Strategic Planning, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Strategic Planning we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Strategic Planning we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   Reduce time and effort by using story recommendations from Now Assist to break down your epics and features in Enterprise Agile Planning \(EAP\).
-   Collaborate in real time on docs with multiple editors.
-   View the rolled-up financial costs and benefits data of your planning items on the new **Financials** tab in the Planning page.
-   View the financial data of planning items while creating multiple prioritization scenarios for efficient use of budget and to get better ROI.
-   Use dashboards to monitor performance, track progress, and make informed decisions related to ideas, feedback, planning, and execution.
-   Create, edit, and switch between views with display preferences for portfolio plans and free-form roadmaps.
-   Enhance the quality of planning item descriptions by enabling AI assistance.

 See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Categorize your strategic priorities, goals, planning items, and execution items—projects and demands as Artificial Intelligence to track and monitor their progress from the AI Control Tower workspace.
-   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans. View the roadmap-level milestone row while scrolling down the Roadmap page. Use different icons to distinguish item-level milestones.
-   Apply filters using string-type and boolean field values to view the desired data on the Planning and Scoring pages.
-   Work on financial planning for various planning items such as Capabilities, Features, and so on.
-   View the planned costs of your planning items for the past fiscal periods.
-   Use Display mode to switch between different views of the financials record page.
-   Create and manage monetary benefit plans to capture and track projected and actual benefits.
-   Manage and run projects in various global currencies besides the functional currency using multicurrency.
-   Generate labor cost on sub-projects based on the resource assignments.

 See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Create and manage demands from the Next Experience for Demand Management in Strategic Planning. Guide demand managers and users through predefined stages and actions for each demand process using Playbooks in Next Experience for Demand Management.
-   Link AI systems to a demand using a playbook activity in Next Experience for Demand Management. Generate a concise summary of a demand using the demand summarization skill.
-   Use boards in Strategy and Goals to group and manage strategic priorities and objectives for your organization. Use the goal insights skill to generate insights for goals to gain predictive, actionable visibility into goal health.
-   Send notifications to target owners or contributors to ensure timely updates of target actuals. Define targets across multiple organizational levels with the Assigned entity field in the target form.
-   Consistent financial reporting across all baselines by support of investment currency on migrated financial baselines.
-   Simplified user experience and focus on investment level financials view on investment currency fields for new customers. Complete and accurate currency data in all financial baselines for existing customers are now upgraded to include investment currency values.

 See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

