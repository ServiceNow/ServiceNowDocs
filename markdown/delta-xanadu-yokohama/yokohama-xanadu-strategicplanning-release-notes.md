---
title: Combined Strategic Planning release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Strategic Planning from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-strategicplanning-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 17
breadcrumb: [Products combined by family]
---

# Combined Strategic Planning release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Strategic Planning from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Strategic Planning release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Strategic Planning to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

After upgrading to Strategic Planning v4.3.2, run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job. This scheduled job migrates the existing values in the **Review frequency** and **Breakdown interval** fields to the **Check-in frequency** field in the target records. For more information on how these values are migrated for targets with different values, see [Target breakdowns migration](https://www.servicenow.com/docs/access?context=target-breakdowns-migration-spw&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

After upgrading to Strategic Planning v4.7.0, the following changes apply to user preferences:

-   Custom view settings previously saved under user preferences will be cleared. You must reapply these changes and create views as needed. For instructions, see [Create a portfolio plan view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-portfolio-plan-view-spw&family=yokohama&ft:locale=en-US) and [Create a free-form roadmap view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-free-form-roadmap-view-spw&family=yokohama&ft:locale=en-US).
-   Customizations made to the Timeline and Kanban views in the **Roadmap** tab, and the Kanban view in the **Prioritization** tab at the portfolio plan level, will be copied to the Default view of the portfolio plan. Similarly, any customizations made to the Timeline and Kanban views in the free-form roadmap will also be copied to the Default view of the free-form roadmap.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Strategic Planning.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Show or hide features for your portfolio plan](https://www.servicenow.com/docs/access?context=show-or-hide-the-features-for-your-portfolio-plan-spw&family=xanadu&ft:locale=en-US)**

As a portfolio manager, show or hide the features, such as Goals, Scoring, Prioritization, and Roadmap, of your portfolio plan. This capability helps you share only the portfolio plan data that matters to your stakeholders and restrict access to the other data.

-   **[Goal management enhancements](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&family=xanadu&ft:locale=en-US)**
    -   Create daily, weekly, or monthly target breakdowns according to how often you want to update and track the progress of the target. The target breakdowns are created based on the value selected in the **Check-in frequency** field. For example, if you select **Monthly** in the **Check-in frequency** field for a target spanning a year, then 12 monthly target breakdowns are created.
    -   Updating actuals for a target has been simplified with an enhanced UI:
        -   In the Check-in actuals window on the **Progress** tab of the target’s side panel, update the actual value of any time period or breakdown.
        -   In the **Progress** tab of the target’s side panel, view the trend of the target’s progress in a line or bar graph. You can also edit the planned target and view the check-in history of the target actuals.
    -   When creating a target, the **Target breakdown details** section of the Target modal shows the planned target values for each target breakdown in a tabular format, which helps you visualize the final target value spread across the target’s time period.
    -   On the Target form, use the **Baseline reference** field to compare future target performance with the actual value that was achieved in the last year or before the target was created.
    -   Add targets to a new goal using the **Save and add target** option on the Goal modal. Also, you can use the **Save and add new target** option to add more targets for the goal.
    -   Run the **Create Goals Demo Data with Target Breakdowns** scheduled job to create demo data with goals and target breakdowns. For more information on this scheduled job, see [Create goals demo data with target breakdowns](https://www.servicenow.com/docs/access?context=create-goals-demo-data-with-target-breakdowns&family=xanadu&ft:locale=en-US).
    -   Create a copy of a goal or target using the **Duplicate** option from the row context menu icon \(\[Omitted image "image.row-context-menu-icon"\] Alt text: Row context menu icon.\). For more information, see [Create a copy of a goal or target](https://www.servicenow.com/docs/access?context=create-a-copy-of-a-goal-or-target&family=xanadu&ft:locale=en-US).
    -   Activity stream is enabled for the targets and goals in the full details record page.
-   **[Planning enhancements](https://www.servicenow.com/docs/access?context=planning-in-spw&family=xanadu&ft:locale=en-US)**
    -   Filter planning items in the Prioritization page and roadmap bars in the Roadmap page with multi-value fields, such as tags, business applications, and business capabilities.
    -   In the Child items related list of an EAP planning item, view child items associated with the epic in EAP.
    -   When you view a portfolio plan, you can copy a portfolio plan that you don't have edit access to and edit the plan as needed. For more information, see [Copy a portfolio plan](https://www.servicenow.com/docs/access?context=copy-portfolio-plan-in-strategic-planning&family=xanadu&ft:locale=en-US).
-   **[Now Assist in Strategic Planning](https://www.servicenow.com/docs/access?context=now-assist-spm&family=xanadu&ft:locale=en-US)**
    -   Generate a summary of selected text on Docs using the Planning item Gen AI Docs skill. You can summarize, elaborate, and shorten the selected content on Docs.
    -   Summarize a large volume of feedback using the multi feedback summarization skill on the Feedback page.
    -   Create a demand within the Employee Service Management \(ESC\) portal using the Now Assist conversational catalog creation capability.
    -   Summarize the complete content of a document with the Planning item Gen AI Docs skill to help save time on manual content analysis.
-   **[Collaborate using Docs](https://www.servicenow.com/docs/access?context=docs-for-eap-teams-and-planning-items&family=xanadu&ft:locale=en-US)**
    -   Store the information of key artifacts and other details of planning items, such as Epics, Capabilities, and Features, directly from within the workspace.
    -   Manage team-level documentation for Agile team, ART, Solution Train, and Portfolio.
    -   Create multiple rich-text documents at each planning item level or Agile team level.
        -   Help avoid data loss and parallel editing with real-time collaboration.
        -   Tag team members to their action items.
        -   Insert media and URLs.
-   **[Docs for planning items](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&family=xanadu&ft:locale=en-US)**
    -   Store the information of key artifacts and other details of planning items, such as Demands, Projects, and Epics, directly from within the workspace.
    -   Create multiple rich-text documents at each planning item level.
        -   Help avoid data loss and parallel editing with real-time collaboration.
        -   Tag team members to their action items.
        -   Insert media and URLs.
-   **[Migrate from SAFe](https://www.servicenow.com/docs/access?context=migrating-from-safe-to-eap&family=xanadu&ft:locale=en-US)**

Transition from Scaled Agile Framework \(SAFe\) applications, such as Essential SAFe and Portfolio SAFe, to EAP. Use the Guided Setup module in the Strategic Planning application to execute your migration step by step.

This migration is intended to be one-time only. Initiating the migration again later while continuing to use SAFe applications with EAP won't carry any changes made to the SAFe records that are already migrated.

-   **[Override the default planning calendar for Agile Teams](https://www.servicenow.com/docs/access?context=create-planning-calendar-type-in-eap&family=xanadu&ft:locale=en-US)**

For Agile Teams and Agile release trains \(ARTs\), the **Override planning calendar** field enables team members to change their planning calendar. The updated calendar is automatically applied to any child teams and takes effect at the beginning of the next iteration.

-   **[Persistence of personalization settings for the EAP PI planning board](https://www.servicenow.com/docs/access?context=pi-planning-eap&family=xanadu&ft:locale=en-US)**

Personalization of the settings made in the PI planning board for a team type are applied across the workspace according to user, team type, and work item type. For example, settings applied to one ART, such as enabling the Dependencies toggle, Team backlog lane, or compact cards, are applied to all ARTs in the workspace for a user.

-   **[Optimize planning using scenario planning](https://www.servicenow.com/docs/access?context=scenario-planning-in-strategic-planning&family=xanadu&ft:locale=en-US)**
    -   Create scenarios in a simulated environment and adjust the prioritization and timelines of planning items.
    -   Check the alignment of planning items with goals to verify the delivery of strategic outcomes.
    -   Visualize the differences between goal alignment and trade-off decisions between scenarios by comparing scenarios side by side.
    -   Approve the best scenario as the live portfolio plan for execution and making informed decisions.
-   **[Export goals and targets data to Excel or CSV](https://www.servicenow.com/docs/access?context=export-goals-and-targets-to-excel&family=xanadu&ft:locale=en-US)**

Export goals and targets from your portfolio plan into a Microsoft Excel or CSV file to share the data and collaborate with your business stakeholders.

-   **[Export a roadmap or free-form roadmap to PowerPoint](https://www.servicenow.com/docs/access?context=export-a-portfolio-plan-to-powerpoint-strategic-planning&family=xanadu&ft:locale=en-US)**

Export a roadmap or free-form roadmap from a portfolio plan into a Microsoft PowerPoint file to share data and collaborate with your business stakeholders. The predefined template helps you generate reports for your roadmap, including roadmap milestones, item milestones, vertical lines, and horizontal lanes.

You can export a roadmap for the maximum tenure of lanes a year at a time. You can also choose between Compact mode, which exports 25 horizontal lanes per slide, or Default mode, which exports 15 horizontal lanes per slide, when exporting your roadmap.

You can select the data that you want to be exported into the report by editing the predefined templates or creating your own branded template. For more information, see [Create a Microsoft PowerPoint template](https://www.servicenow.com/docs/access?context=create-ppt-template&family=xanadu&ft:locale=en-US).

-   **[Plan at a high level using the Project Program lens](https://www.servicenow.com/docs/access?context=portfolio-plans-in-strategic-planning&family=xanadu&ft:locale=en-US)**

Plan at a high level by building portfolio plans for program \[pm\_program\] items using the Project Program lens. Score and prioritize the programs and track them using roadmaps.

-   **[Feedback enhancements](https://www.servicenow.com/docs/access?context=managing-product-feedback-in-strategic-planning&family=xanadu&ft:locale=en-US)**
    -   Manage the feedback filter card directly from the feedback homepage by sorting, pinning, sharing, updating, or deleting it.
    -   Allow access to specific users or groups when sharing the feedback filter card, and review the users who have access to it.
-   **[Financials in Strategic Planning](https://www.servicenow.com/docs/access?context=using-financials-spw&family=xanadu&ft:locale=en-US)**
    -   Migrate the existing planning items budget from the classic UI to Next Experience using the **Migrate Budget** option.
    -   As a portfolio manager, allocate and manage the budget of your planning items using the Budget vs cost view.
    -   As a project manager, compare a budget to the captured costs of your planning items and reforecast the planned costs to meet the approved budget.
    -   Compare financial baselines to view simple financials and budget.
    -   View the cost plans, expense lines, and financial baselines of sub-projects using the Financial view of a parent project.
    -   Widgets in the Cost view of parent projects display the rolled-up value of the planned costs, expense lines, budget, and variance.
    -   Create custom labor cost types and map them with a unique sys\_id to generate labor costs.

-   **[Capacity Planning in Strategic Planning](https://www.servicenow.com/docs/access?context=using-cap-plan-spw&family=xanadu&ft:locale=en-US)**
    -   Select a primary attribute to auto-select the resource criteria based on the planning items in the portfolio.
    -   Automatically generate resource capacity using a scheduled job at your desired cadence.
    -   View only prioritized planning items in the bottom tray of the Capacity Planning screen.
    -   View the total capacity, estimate, and available efforts of a resource using the heatmap view.

</td></tr><tr><td>

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


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Strategic Planning features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Break down work from a parent work item](https://www.servicenow.com/docs/access?context=breakdown-work-eap-epics-capabilities-child-work&family=xanadu&ft:locale=en-US)**

Create child work items directly from the parent record page.

    -   The **Child items** tab on the work item record page is replaced with the tabs of each associated child item. For example, the full details page of an Epic shows separate tabs for its child work items, capabilities, features, and stories, based on the EAP configuration.
    -   New button is added to each tab to create work items directly from the parent work item record page.
-   **[Enhancements to the PI planning board in EAP](https://www.servicenow.com/docs/access?context=pi-planning-eap&family=xanadu&ft:locale=en-US)**

The PI planning board displays all work assigned to the current Agile structure level as well as its child teams.

-   **[Feedback](https://www.servicenow.com/docs/access?context=product-feedback-landing&family=xanadu&ft:locale=en-US)**

The Product Feedback application name is changed to Feedback.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Changes in planning item forms](https://www.servicenow.com/docs/access?context=epic-form&family=yokohama&ft:locale=en-US)**

The dates in the **Planned start date** and **Planned end date** fields are editable for all planning item types other than Demand and Project planning item types. Also, the **State** field is editable for EAP planning items and its child items.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Strategic Planning features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Strategic Planning features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

</td></tr><tr><td>

Yokohama

</td><td>

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Strategic Planning we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

-   Show or hide the features of your portfolio plan so you share only the most important data with your stakeholders.
-   Update actuals and track the progress of your targets in daily, weekly, monthly, quarterly, or yearly intervals with the enhanced target breakdown feature.
-   Filter the planning items and roadmap bars with multi-value fields, such as tags, business applications, and business capabilities.
-   Create rich-text documents to store and manage artifact information for planning items and Agile teams in EAP.
-   Create scenarios to simulate changes to the portfolio plan, compare scenarios for visualizing trade-off decisions, and approve a scenario to revise the live plan.
-   View the cost plans, expense lines, budget, and financial baselines of sub-projects at the parent project level. View the financial performance of a project using the rolled-up planned and actuals costs in the widgets of parent projects.
-   Select a primary attribute to populate resource criteria automatically from the resource assignments of the prioritized planning items, and view the team's capacity in the Capacity Planning screen.

 See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

