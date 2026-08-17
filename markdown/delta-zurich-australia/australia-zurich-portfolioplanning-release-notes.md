---
title: Combined Portfolio Planning release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Portfolio Planning from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-portfolioplanning-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 12
breadcrumb: [Products combined by family]
---

# Combined Portfolio Planning release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Portfolio Planning from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Portfolio Planning release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Portfolio Planning to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

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
</table>## New features

Between your current release family and Australia, new features were introduced for Portfolio Planning.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Roadmap enhancements](https://www.servicenow.com/docs/access?context=planning-roadmaps-in-portfolio-planning&family=zurich&ft:locale=en-US)**
    -   Create custom themes for your roadmap bar colors to align with your organization’s standards.
    -   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans.
    -   View the roadmap-level milestone row while scrolling down the Roadmap page.
    -   Use different icons to distinguish item-level milestones.
-   **[Dynamic data linking in Docs](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-ppw&family=zurich&ft:locale=en-US)**

Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Scenario planning enhancements](https://www.servicenow.com/docs/access?context=enable-scenario-planning-in-portfolio-planning&family=zurich&ft:locale=en-US)**

With the sn\_align\_core.apw\_admin role, you can enable or disable the scenario planning feature. The **sn\_align\_ws.is\_scenario\_planning\_disabled** system property allows you to enable or disable the scenario planning feature.

-   **[Quick filters enhancements](https://www.servicenow.com/docs/access?context=quick-fiters-prioitization-roadmap-ppw&family=zurich&ft:locale=en-US)**

Apply filters using string-type and Boolean field values across the Planning page to view the required dataset. These filters are saved as part of your user preferences, enabling you to access the same filtered data when you log back in and continue your planning seamlessly.

-   **[Financial enhancements](https://www.servicenow.com/docs/access?context=using-financials-pp&family=zurich&ft:locale=en-US)**
    -   View only the planned costs of your planning items to track the total cost of projects or demands.
    -   Use **Display mode** to switch between focused views to better plan and track the financials of your planning items.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate and track labor cost for sub-projects, based on the resource assignments of your sub-projects and planning items such as features and capabilities.

</td></tr><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   **[Financials grid for demands in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=managing-financials-for-demands-ppw&family=australia&ft:locale=en-US)**

Next Experience for Demand Management includes a Financials grid for demand records. This grid shows the demand's cost plans, benefit plans, and baselines. From this grid, users can:

    -   Add cost plans, benefit plans, and expense lines scoped to the demand.
    -   Create and compare baselines for financial data on the demand.
    -   Filter by time scope and personalize the grid columns.
-   **[Demands Dashboard](https://www.servicenow.com/docs/access?context=c_demand_dashboards_ppw&family=australia&ft:locale=en-US)**

Next Experience for Demand Management includes a Dashboard menu for demand records. The dashboard opens by default and is organized into three tabs:

    -   Overview
    -   Financials
    -   Data Quality
Filter dashboard data by department, business unit, portfolio, program, or demand manager. Select a widget, or select **View all** on a list widget, to open the underlying records with the same filters applied.

-   **[Identify similar demands using AI](https://www.servicenow.com/docs/access?context=identify-similar-demand-records-ppw&family=australia&ft:locale=en-US)**

Detect similar existing demand records when creating or editing a demand using the identify similar records skill. This skill compares the Name, Description, and Business Case fields for contextual similarity.

-   **[RIDAC](https://www.servicenow.com/docs/access?context=explore-ridac-ppw&family=australia&ft:locale=en-US)**
    -   Create and associate risks, issues, decisions, actions, and changes \(RIDAC\) with project and demand planning items to track planning uncertainties.
    -   Access a dedicated RIDAC menu in Portfolio Planning Workspace for quick navigation to RIDAC items.
    -   Manage RIDAC items with granular role-based access—assign read-only or full edit access to team members based on their responsibilities.
    -   Run the scheduled job to populate the planning item field on the existing RIDAC records that were created earlier.
    -   Track RIDAC across multiple scopes—view all RIDAC, project-specific RIDAC, portfolio RIDAC, and program RIDAC in a single unified view.
-   **[AI-generated insights for portfolio plans](https://www.servicenow.com/docs/access?context=view-portfolio-insights&family=australia&ft:locale=en-US)**

Gain AI-generated insights into planning items within a portfolio plan using the Portfolio insights skill. Identify planning items that are delayed beyond their planned end date, have delayed starts, or have misalignments between planned and approved dates. Monitor active projects that show early risk indicators but have not yet experienced delays. View AI-generated top root causes and recommended actions for each insight category to help address delays and misalignments effectively.

The AI Insights window displays a timestamp indicating when insights were last generated. You can regenerate insights and recommendations if required to see the changes based on the latest available data.

Users with the sn\_align\_core.apw\_admin role can configure severity thresholds and scoring factors for planning items. These settings control how the Portfolio insights skill classifies insight severity as Critical, Medium, or Low.

-   **[Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=demand-workspace-ppw&family=australia&ft:locale=en-US)**

Manage strategic and operational demands in a unified experience in Portfolio Planning. This Next Experience interface consolidates demand creation, assessment, collaboration, and conversion in one place, eliminating context switching and reducing reliance on the classic Demand Workbench.

-   **[Create and manage demands in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=managing-demands-ppw&family=australia&ft:locale=en-US)**
    -   Create and manage a demand in Next Experience for Demand Management using guided tabs. These tabs help you define alignment, estimate costs, and confirm readiness as you build out the demand.
    -   Collaborate on demands through Docs, which syncs execution and planning.
    -   View, add, and edit cost plans and budgeting details using related lists.
-   **[Use Playbook in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-playbooks-in-ppw&family=australia&ft:locale=en-US)**

Help teams manage demands with greater structure and consistency using Playbook in Next Experience for Demand Management.

Playbooks enable you to define multiple governance processes across the organization using a low‑code/no‑code configuration experience. Create clear stages and guided activities from demand intake to completion using a default or custom playbook. Custom playbooks support multiple demand management processes across your organization.

-   **[Associate AI systems with demands in Next Experience for Demand Management](https://www.servicenow.com/docs/access?context=use-playbooks-in-ppw&family=australia&ft:locale=en-US)**

Use a playbook activity in Next Experience for Demand Management to associate AI systems with a demand. You can link impacted systems and add new ones directly within the demand workflow.

-   **[Portfolio plan enhancements](https://www.servicenow.com/docs/access?context=work-prioritization-portfolio-planning&family=australia&ft:locale=en-US)**
    -   Access the Hierarchy tab directly from the Planning page, located next to the Prioritization tab. This new placement replaces the previous access point within the Prioritization tab, providing a more efficient way to view and manage planning items.
    -   Save filter views specific to the Hierarchy tab without affecting views in the Prioritization tab.
    -   View planning items in the new Hierarchy tab on the Planning page, now sorted using global rank when available. Drag and drop is supported for lowest‑level items, enabling you to rerank them within their groups.
    -   Share a portfolio plan using the Copy link option. This provides access to existing users who have access to the portfolio plan.
    -   Make a portfolio plan public and share the copied link with Strategic Planning Workspace users, without inviting them individually or as a group. Note that users accessing a public portfolio plan with the shared link cannot view scenarios within the plan.
    -   Expand or collapse portfolio plan header to maximize screen space while planning.
    -   Edit the default view within a portfolio plan and save changes using the Save view option.
    -   View additional status attributes — cost, resource, schedule, and scope — for planning items in Portfolio Planning Workspace. For project planning items, these attributes are synced automatically from the latest published project status report. For other planning items, these attributes can be set manually. Note that project status report attributes synced from the Project status \(project\_status\) table are read-only in Portfolio Planning Workspace and can't be edited directly.
    -   Set planning item status to **No status** when a status has not been determined, alongside the existing **Green**, **Yellow**, and **Red** values. Planning items are created with **No status** by default.
    -   Display rollup bars at parent levels in the hierarchy view and choose the date type to display — approved, planned, or actual. Use the comparison option to compare date types, such as approved versus planned dates, to identify schedule misalignments.
-   **[Plan efficiently with additional pre-defined lenses](https://www.servicenow.com/docs/access?context=lens-and-portfolio-plans&family=australia&ft:locale=en-US)**

Use the Planning item lens to plan, prioritize, and roadmap work in Strategic Planning Workspace directly with planning items, without configuring organization structure, programs, portfolios, or products. The lens supports all enabled work item types, such as projects and demands, and can be used as a standalone lens or alongside other lenses.

-   **[Financials for planning items](https://www.servicenow.com/docs/access?context=using-financials-spw&family=australia&ft:locale=en-US)**

View the financial baselines in investment currency and project currency after migrating them from Classic to Next Experience. Migrated financial baselines include actuals, costs, benefits, and budget values from the project currency to the investment currency.

Using multicurrency, new and existing customers see only investment currency fields in demand and project records. Planned costs, actual costs, planned benefits, actual benefits, and budget fields are included in the financial baselines.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Portfolio Planning features.

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

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   **[Summarize demands using AI](https://www.servicenow.com/docs/access?context=summarize-demands-in-ppw&family=australia&ft:locale=en-US)**

The demand summary is generated in the **AI Overview** tab instead of the **Details** tab. The skill is set to trigger automatically, that is, the summary is generated on landing in this tab. Auto-generation is on by default and applies to demands in Submitted, Screening, Qualified, or Approved states. You can define the trigger to manually trigger as well, where users must select the **Summarize** button to generate the summary.

-   **[AI skills for Demand Workspace](https://www.servicenow.com/docs/access?context=ai-skills-in-demands-workspace-ppw&family=australia&ft:locale=en-US)**

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[Access execution records from Portfolio Plans](https://www.servicenow.com/docs/access?context=access-demands-from-portfolio-planning-views&family=australia&ft:locale=en-US)**

The execution URL is updated on the planning item demand. New planning items demand will automatically use the new execution URL. The execution URLs on existing planning item demands continue to work but doesn't reflect the updated navigation. Run the **Update Demand Planning Item Execution URL** scheduled job to update the execution URL on the existing demands.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Portfolio Planning features or functionality were removed.

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

Between your current release family and Australia, some Portfolio Planning features or functionality were deprecated.

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
</table>## Activation information

Review information on how to activate Portfolio Planning.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Portfolio Planning by requesting it from the ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install Portfolio Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Portfolio Planning we have noted them here.

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

If any specific browser requirements were introduced or changed for Portfolio Planning we have noted them here.

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

Review details on accessibility information for Portfolio Planning, such as specific requirements or compliance levels.

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

If there are specific localization considerations for Portfolio Planning we have noted them here.

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

If there are specific highlight considerations for Portfolio Planning we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

 See [Portfolio Planning](https://www.servicenow.com/docs/access?context=portfolio-planning-app-landing-page&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Identify similar demand records in Next Experience for Demand Management based on contextual similarity in the name, description, and business case content using the identify similar records AI skill.
-   Monitor demand distribution, financials, and data quality at a glance using Dashboard in Next Experience for Demand Management.
-   View and manage cost plans, benefit plans, and expense lines directly from the demand records in the Financials page in Next Experience for Demand Management.
-   Create and manage demands from the Next Experience for Demand Management in Portfolio Planning.
-   Guide demand managers and users through predefined stages and actions for each demand process using Playbook in Next Experience for Demand Management.
-   Link AI systems to a demand using a playbook activity in Next Experience for Demand Management. Generate a concise summary of a demand using the demand summarization skill.
-   Review the financial records of your planning items in both project currency and investment currency when you migrate them from Classic to Next Experience.
-   Create financial baselines with multicurrency to capture, view, and track the financial health of your planning item using project baselines and investment baselines.

 See [Portfolio Planning](https://www.servicenow.com/docs/access?context=portfolio-planning-app-landing-page&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

