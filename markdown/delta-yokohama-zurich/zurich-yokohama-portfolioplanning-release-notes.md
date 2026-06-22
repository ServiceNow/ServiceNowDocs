---
title: Combined Portfolio Planning release notes for upgrades from Yokohama to Zurich
description: Consolidated page of all release notes for Portfolio Planning from Yokohama to Zurich.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/delta-yokohama-zurich/zurich-yokohama-portfolioplanning-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined Portfolio Planning release notes for upgrades from Yokohama to Zurich

Consolidated page of all release notes for Portfolio Planning from Yokohama to Zurich.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Portfolio Planning release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Zurich.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Portfolio Planning to Zurich

Before you upgrade to Zurich, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

After upgrading to Portfolio Planning v8.8.0, the custom view settings previously saved under user preferences will be cleared. You must reapply these changes and create views as needed. For instructions, see [Create a portfolio plan view in Portfolio Planning](https://servicenow-staging.fluidtopics.net/access?context=create-portfolio-plan-view-ppw&family=yokohama&ft:locale=en-US) and [Create a free-form roadmap view in Portfolio Planning](https://servicenow-staging.fluidtopics.net/access?context=create-free-form-roadmap-view-ppw&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Zurich, new features were introduced for Portfolio Planning.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[View financial data of your planning items at the portfolio level](https://servicenow-staging.fluidtopics.net/access?context=using-portfolio-financials-ppw&family=yokohama&ft:locale=en-US)**
    -   View the rolled-up financial costs and benefits data of your planning items Epics, Demands, and Projects at the portfolio level for different time scales and ranges.
    -   View the financial values such as the Budget, Planned cost, Variance, Actuals, and Remaining Estimates of your planning items by expense type or cost type.
    -   View the Forecasts, Actuals, and Variance of your planning items for monetary benefits.
    -   View the financial data of the planning items while creating multiple prioritization scenarios to promote efficient use of budget and to help increase ROI.
-   **[Create and manage financial scenarios of planning items](https://servicenow-staging.fluidtopics.net/access?context=optimizing-scenarios-in-strategic-planning&family=yokohama&ft:locale=en-US)**
    -   Optimize your portfolio by creating financial scenarios to validate and arrive at a profitable outcome.
    -   Plan and manage the budget of the planning items in a simulation mode for efficient financial planning and to help prevent overspending.
    -   Manage prioritization and budget allocation of the planning items to meet business priorities.
    -   Compare financial scenarios and automatically allocate the planned budget from approved scenarios to planning items.
    -   Enable a budget allocation property to analyze finances in scenario planning and take effective decisions using data-driven insights.
-   **[Dashboards for data analysis and decision-making](https://servicenow-staging.fluidtopics.net/access?context=using-dashboards-in-ppw&family=yokohama&ft:locale=en-US)**

Consolidate key data and metrics from multiple sources onto dashboards, enabling you to monitor performance, track progress, and make informed decisions related to planning and execution.

You can create, edit, and copy a dashboard, customizing as needed. Add widgets to a dashboard to display key data, metrics, and visualizations. You can also share dashboards to collaborate with the business stakeholders who have access to the portfolio plan.

-   **[Create and share views for portfolio plans and free-form roadmaps](https://servicenow-staging.fluidtopics.net/access?context=managing-portfolio-plan-views-ppw&family=yokohama&ft:locale=en-US)**

Create, edit, and switch views in portfolio plans and free-form roadmaps using display preferences. You can create personal views that are private to you or public views that can be shared with stakeholders who have access.

Portfolio plan display preferences include column selection, grouping and filtering. Free-form roadmap preferences include grouping, milestones selection, dependencies selection, and tracking mode. The portfolio plan view saves your display preferences across the Prioritization, Roadmap, Capacity, and Financials tabs.

**Note:** Portfolio plan views are available only for the Planning module and are supported in live mode, but not in scenario mode.

-   **[Real-time collaboration for Planning item Docs](https://servicenow-staging.fluidtopics.net/access?context=docs-for-planning-items-in-ppw&family=yokohama&ft:locale=en-US)**

Edit a doc page concurrently with multiple other editors. Colored cursors denote the current location of editors on the page. You can choose to show or hide these indicators.

**Note:** To use the full functionality of Docs v6.6.0 within Portfolio Planning Workspace, upgrade to Portfolio Planning Workspace v8.5.0. For more information, see the [Incompatibility After Upgrading Docs to Version 6.0.0 \[KB2017926\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926) article in the Now Support Knowledge Base.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Roadmap enhancements](https://servicenow-staging.fluidtopics.net/access?context=planning-roadmaps-in-portfolio-planning&family=zurich&ft:locale=en-US)**
    -   Create custom themes for your roadmap bar colors to align with your organization’s standards.
    -   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans.
    -   View the roadmap-level milestone row while scrolling down the Roadmap page.
    -   Use different icons to distinguish item-level milestones.
-   **[Dynamic data linking in Docs](https://servicenow-staging.fluidtopics.net/access?context=docs-for-planning-items-in-ppw&family=zurich&ft:locale=en-US)**

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Scenario planning enhancements](https://servicenow-staging.fluidtopics.net/access?context=enable-scenario-planning-in-portfolio-planning&family=zurich&ft:locale=en-US)**

With the sn\_align\_core.apw\_admin role, you can enable or disable the scenario planning feature. The **sn\_align\_ws.is\_scenario\_planning\_disabled** system property allows you to enable or disable the scenario planning feature.

-   **[Quick filters enhancements](https://servicenow-staging.fluidtopics.net/access?context=quick-fiters-prioitization-roadmap-ppw&family=zurich&ft:locale=en-US)**

Apply filters using string-type and Boolean field values across the Planning page to view the required dataset. These filters are saved as part of your user preferences, enabling you to access the same filtered data when you log back in and continue your planning seamlessly.

-   **[Financial enhancements](https://servicenow-staging.fluidtopics.net/access?context=using-financials-pp&family=zurich&ft:locale=en-US)**
    -   View only the planned costs of your planning items to track the total cost of projects or demands.
    -   Use **Display mode** to switch between focused views to better plan and track the financials of your planning items.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate and track labor cost for sub-projects, based on the resource assignments of your sub-projects and planning items such as features and capabilities.

</td></tr></tbody>
</table>## Changes

Between your current release family and Zurich, some changes were made to existing Portfolio Planning features.

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

</td></tr></tbody>
</table>## Removed

Between your current release family and Zurich, some Portfolio Planning features or functionality were removed.

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

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Zurich, some Portfolio Planning features or functionality were deprecated.

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

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Portfolio Planning.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

Install Portfolio Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://servicenow-staging.fluidtopics.net/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

</td></tr><tr><td>

Zurich

</td><td>

Install Portfolio Planning by requesting it from the ServiceNow Store. 

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Portfolio Planning we have noted them here.

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

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Portfolio Planning we have noted them here.

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

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Portfolio Planning, such as specific requirements or compliance levels.

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

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Portfolio Planning we have noted them here.

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

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Portfolio Planning we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   View the rolled-up financial costs and benefits data of your planning items in the new **Financials** tab in the Planning page.
-   View the financial data of planning items while creating multiple prioritization scenarios to promote efficient use of budget and help increase the return on investment \(ROI\).
-   Monitor performance, track progress, and make informed decisions related to planning and execution using dashboards.
-   Create, edit, and switch views in portfolio plans and free-form roadmaps with display preferences.

 See [Portfolio Planning](https://servicenow-staging.fluidtopics.net/access?context=portfolio-planning-app-landing-page&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   View the planned costs of your planning items for the past fiscal periods.
-   Use **Display mode** to switch between different views of the financials record page.
-   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans. View the roadmap-level milestone row while scrolling down the Roadmap page. Use different icons to distinguish item-level milestones.
-   Apply filters using string-type and Boolean field values to view the desired data.
-   Customize and apply a theme to your roadmap to match your organization’s standards.
-   Create and manage monetary benefit plans to capture and track projected and actual benefits.
-   Manage and run projects in various global currencies besides the functional currency using multicurrency.
-   Generate labor cost on sub-projects based on the resource assignments.

 See [Portfolio Planning](https://servicenow-staging.fluidtopics.net/access?context=portfolio-planning-app-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/delta-yokohama-zurich/rn-combined-intro.md)

