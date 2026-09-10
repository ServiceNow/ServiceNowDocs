---
title: Combined Strategic Planning release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Strategic Planning from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-strategicplanning-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 19
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

-   **Upgrade information**

After upgrading to Strategic Planning v4.7.0, the following changes apply to user preferences:

    -   Custom view settings previously saved under user preferences will be cleared. You must reapply these changes and create views as needed. For instructions, see [Create a portfolio plan view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-portfolio-plan-view-spw&family=yokohama&ft:locale=en-US) and [Create a free-form roadmap view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-free-form-roadmap-view-spw&family=yokohama&ft:locale=en-US).
    -   Customizations made to the Timeline and Kanban views in the **Roadmap** tab, and the Kanban view in the **Prioritization** tab at the portfolio plan level, will be copied to the Default view of the portfolio plan. Similarly, any customizations made to the Timeline and Kanban views in the free-form roadmap will also be copied to the Default view of the free-form roadmap.

</td></tr><tr><td>

Zurich

</td><td>

-   **Upgrade information**

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
-   **[Cycle time report for Agile teams in EAP dashboards](https://www.servicenow.com/docs/access?context=eap-agile-team-dashboard&family=yokohama&ft:locale=en-US)**

Analyze how long the stories take for your Agile team to move from an in-progress state to completion. Each bubble on the chart represents a story and the chart shows stories completed in the past 30 days. You can compare the cycle times of stories that have different story points and review the trend in the time taken by the team to complete them.

Using this data, identify the stories that took longer to complete and analyze the reasons so that you can draft an action plan to optimize the team's cycle time in the future.

-   **[Kanban configuration for EAP teams](https://www.servicenow.com/docs/access?context=agile-configurations-in-eap&family=yokohama&ft:locale=en-US)**

Use the Kanban configuration for teams that don't prefer to work in an iteration-based schedule. You can activate the predefined Kanban configuration and add teams to your Agile structure or you can modify an existing configuration by setting the **Planning calendar** field to **None**.

-   **[Column filters in EAP Backlog](https://www.servicenow.com/docs/access?context=using-eap&family=yokohama&ft:locale=en-US)**

Quickly find the work items that you need by using column-level filters for the data on your EAP Backlog. You can filter on any column that is displayed on the **Backlog** tab.

-   **[Generate stories from epics and features using Now Assist for EAP](https://www.servicenow.com/docs/access?context=generate-stories-from-epics-now-assist-eap&family=yokohama&ft:locale=en-US)**

Break down epics and features into stories using the Now Assist Agile story generation skill in the EAP workspace. Using the available details such as name, description, docs content, and any existing stories, Now Assist provides story recommendations for your epic or feature. You can let Now Assist generate stories using its initial recommendations or you can choose to split or combine the story recommendations before prompting Now Assist to create the stories.

-   **[Create a manage financial scenarios of planning items](https://www.servicenow.com/docs/access?context=optimizing-scenarios-in-strategic-planning&family=yokohama&ft:locale=en-US)**
    -   Optimize your portfolio by creating financial scenarios to validate and arrive at a profitable outcome.
    -   Plan and manage the budget of planning items in simulation mode for efficient financial planning and to help prevent overspending.
    -   Manage prioritization and budget allocation of the planning items to meet business priorities.
    -   Compare scenarios financially and automatically allocate the planned budget to planning items from approved scenarios.
    -   Enable the **new budget allocation** property \(**sn\_invst\_pln.enable\_budget\_allocation\_v2**\) to perform financial analysis in scenario planning and take effective decisions by data-driven insights.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Strategic Planning and AI Control Tower](https://www.servicenow.com/docs/access?context=better-together-with-other-apps-spw&family=zurich&ft:locale=en-US)**

Categorize your strategic priorities, goals, planning items, and execution items—projects and demands as Artificial Intelligence to track and monitor strategy progress from the AI Control Tower workspace.

Use the **Type** field for strategic priorities, the **Category** field for goals, the **Investment type** field for planning items - to classify them as Artificial Intelligence and monitor their progress in the AI Control Tower workspace.

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

-   **[Admin role enhancements in Feedback](https://www.servicenow.com/docs/access?context=components-installed-with-product-feedback&family=australia&ft:locale=en-US)**

The read role sn\_align\_core.pf\_read and write role sn\_align\_core.apw\_admin are added to the following system properties in Feedback and Product idea:

    -   sn\_apw\_advanced.product\_feedback\_allowed\_non\_planning\_items\_for\_link\_item
    -   sn\_apw\_advanced.product\_feedback\_product\_idea\_filters
    -   sn\_apw\_advanced.product\_feedback\_feedback\_filters
    -   sn\_apw\_advanced.feedback.idea\_feedback\_queue\_address

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

-   **[Skill name updates](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&family=yokohama&ft:locale=en-US)**
    -   Renamed the Planning item Gen AI Docs to the Planning item doc summarization skill in Strategic Planning.
    -   Renamed the EAP Teams Gen AI Docs to the EAP doc summarization skill in Enterprise Agile Planning.
    -   Added the Write planning items skill in Strategic Planning.
-   **[Capacity Planning name updates](https://www.servicenow.com/docs/access?context=using-cap-plan-spw&family=yokohama&ft:locale=en-US)**

Change in the name of the **Capacity Planning** tab to **Capacity** in the planning view.


</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Financials UI changes](https://www.servicenow.com/docs/access?context=using-financials-spw&family=zurich&ft:locale=en-US)**
    -   New Display mode in the Financials record page to select and view forecast, compare planned vs actual costs, planned costs, or allocate budget.
    -   Select and view forecasts, compare planned vs. actual costs, and view planned costs or the allocated budget through a new display mode on the Financials record page.
    -   Renamed **Cost** tab as **Costs and benefits** to manage cost plans and benefit plans in one view.
    -   Renamed **Baselines** as **Baseline comparison** to create and compare financial baselines.
    -   Renamed **Time scope** as **Filter time scope** to adjust the time scope to view a focused and customized financial snapshot.
    -   New **Generate labor costs** button to generate labor costs based on the resource assignments.
    -   New **Currency** list option to switch between functional and investment currency.
    -   New **Edit investment currency** option to define investment currency for your projects.
    -   **New monetary benefit plan** option to create new forecast benefit plans.
    -   New **Planned Benefits** widget displays the total forecasted benefits.
    -   New **Total Return** widget displays the total actual benefits form the projects.
    -   New **Record type** column to classify the financial records between benefits and costs.
    -   Renamed **Estimate At Completion** widget to **EAC Cost**.
    -   Renamed **Actual Cost To Date** to **Actuals \(Incl. current fiscal period\)**.

 -   **[Investment type and Investment class fields](https://www.servicenow.com/docs/access?context=planning-item-form&family=zurich&ft:locale=en-US)**

The **Investment type** and **Investment class** fields have been deprecated from the Project and Demand planning item tables. These fields are now created at the parent level in the Planning item \[sn\_align\_core\_planning\_item\] table.

-   **[Goal management](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&family=zurich&ft:locale=en-US)**

By default, only active goals—those goals with the **Active** field set to **true**—are displayed across the workspace. This change applies to the **Dashboards** and **Goals and targets** tabs on the Goals page, the **Goal**/**Parent goal** reference fields in all applicable tables, and all relevant dashboards.

-   **[Default related list view changes for Stories](https://www.servicenow.com/docs/access?context=create-single-or-multiple-child-items-for-epic-in-eap&family=zurich&ft:locale=en-US)**

In the Stories list for an Epic, Feature, or Capability in the Enterprise Agile Planning workspace, the Assignment group and Sprint columns in the default related list view are replaced with the EAP team and Iteration columns.


</td></tr><tr><td>

Australia

</td><td>

-   **[Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=demand-workspace&family=australia&ft:locale=en-US)**
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
    -   [Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)The **Financials** grid is added to the navigation menu of a demand. It has options to create cost plans, monetary benefits plans, expense lines, and create and compare baselines.
    -   The **Dashboards** menu item is added for demands, providing **Overview**, **Financials**, and **Data Quality** tabs.
    -   The following items have been added to the demand form and are available if you have the identify similar records AI skill activated:
        -   The **Identify similar demands** button, which identifies and displays similar demands.
        -   The **Similar Demands** tab in **Details**, which displays the list of similar demand records identified by AI.
    -   The **AI Overview** tab is added to the navigation menu of a demand. It generates a demand summary on landing if the skill trigger is set to automatic. If the trigger is set to manual, a **Summarize** button is available to generate the summary.
-   **[Changes to Target form](https://www.servicenow.com/docs/access?context=target-form-egm&family=australia&ft:locale=en-US)**

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
-   **[Changes to Strategic Priority form](https://www.servicenow.com/docs/access?context=strategic-priority-form&family=australia&ft:locale=en-US)**

The **Status** field has been added to the Strategic Priority form, enabling you to set the status of a strategic priority as **None**, **Green**, **Yellow**, or **Red**.

-   **[Hierarchy and List views in Prioritization](https://www.servicenow.com/docs/access?context=managing-backlog-alignment-planner-workspace&family=australia&ft:locale=en-US)**

The **Kanban** and **Hierarchy** views have been removed from the Prioritization page and are now available as separate tabs in the Planning page. This change improves navigation by consolidating all planning-related views in one place.


 -   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


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

-   **Activation information**

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

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

-   Identify similar demand records in Next Experience for Demand Management based on contextual similarity in the name, description, and business case content using the identify similar records AI skill.
-   View and manage cost plans, benefit plans, and expense lines directly from the demand records in the Financials page in Next Experience for Demand Management.
-   Monitor demand distribution, financials, and data quality at a glance using Dashboard in Next Experience for Demand Management.
-   Create and manage demands from the Next Experience for Demand Management in Strategic Planning. Guide demand managers and users through predefined stages and actions for each demand process using Playbooks in Next Experience for Demand Management.
-   Link AI systems to a demand using a playbook activity in Next Experience for Demand Management. Generate a concise summary of a demand using the demand summarization skill.
-   Use boards in Strategy and Goals to group and manage strategic priorities and objectives for your organization. Use the goal insights skill to generate insights for goals to gain predictive, actionable visibility into goal health.
-   Send notifications to target owners or contributors to ensure timely updates of target actuals. Define targets across multiple organizational levels with the Assigned entity field in the target form.
-   Consistent financial reporting across all baselines by support of investment currency on migrated financial baselines.
-   Simplified user experience and focus on investment level financials view on investment currency fields for new customers. Complete and accurate currency data in all financial baselines for existing customers are now upgraded to include investment currency values.

 See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

