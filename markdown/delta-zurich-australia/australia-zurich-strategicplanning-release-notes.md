---
title: Combined Strategic Planning release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Strategic Planning from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-strategicplanning-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 13
breadcrumb: [Products combined by family]
---

# Combined Strategic Planning release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Strategic Planning from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Strategic Planning release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Strategic Planning to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

