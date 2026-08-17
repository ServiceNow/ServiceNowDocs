---
title: Portfolio Planning release notes
description: The ServiceNow Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 10
---

# Portfolio Planning release notes

The ServiceNow® Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Australia release.

## Portfolio Planning highlights for the Australia release

-   Identify similar demand records in Next Experience for Demand Management based on contextual similarity in the name, description, and business case content using the identify similar records AI skill.
-   Monitor demand distribution, financials, and data quality at a glance using Dashboard in Next Experience for Demand Management.
-   View and manage cost plans, benefit plans, and expense lines directly from the demand records in the Financials page in Next Experience for Demand Management.
-   Create and manage demands from the Next Experience for Demand Management in Portfolio Planning.
-   Guide demand managers and users through predefined stages and actions for each demand process using Playbook in Next Experience for Demand Management.
-   Link AI systems to a demand using a playbook activity in Next Experience for Demand Management. Generate a concise summary of a demand using the demand summarization skill.
-   Review the financial records of your planning items in both project currency and investment currency when you migrate them from Classic to Next Experience.
-   Create financial baselines with multicurrency to capture, view, and track the financial health of your planning item using project baselines and investment baselines.

See [Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning-app-landing-page.md) for more information.

**Important:** Portfolio Planning is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   **[Financials grid for demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/managing-financials-for-demands-ppw.md)**

    Next Experience for Demand Management includes a Financials grid for demand records. This grid shows the demand's cost plans, benefit plans, and baselines. From this grid, users can:

    -   Add cost plans, benefit plans, and expense lines scoped to the demand.
    -   Create and compare baselines for financial data on the demand.
    -   Filter by time scope and personalize the grid columns.
-   **[Demands Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/c_demand_dashboards_ppw.md)**

    Next Experience for Demand Management includes a Dashboard menu for demand records. The dashboard opens by default and is organized into three tabs:

    -   Overview
    -   Financials
    -   Data Quality
    Filter dashboard data by department, business unit, portfolio, program, or demand manager. Select a widget, or select **View all** on a list widget, to open the underlying records with the same filters applied.

-   **[Identify similar records using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/identify-similar-demand-records-ppw.md)**

    Detect similar existing demand records when creating or editing a demand using the identify similar records skill. This skill compares the Name, Description, and Business Case fields for contextual similarity.

-   **[RIDAC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/explore-ridac-ppw.md)**
    -   Create and associate risks, issues, decisions, actions, and changes \(RIDAC\) with project and demand planning items to track planning uncertainties.
    -   Access a dedicated RIDAC menu in Portfolio Planning Workspace for quick navigation to RIDAC items.
    -   Manage RIDAC items with granular role-based access—assign read-only or full edit access to team members based on their responsibilities.
    -   Run the scheduled job to populate the planning item field on the existing RIDAC records that were created earlier.
    -   Track RIDAC across multiple scopes—view all RIDAC, project-specific RIDAC, portfolio RIDAC, and program RIDAC in a single unified view.
-   **[AI-generated insights for portfolio plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/view-portfolio-insights.md)**

    Gain AI-generated insights into planning items within a portfolio plan using the Portfolio insights skill. Identify planning items that are delayed beyond their planned end date, have delayed starts, or have misalignments between planned and approved dates. Monitor active projects that show early risk indicators but have not yet experienced delays. View AI-generated top root causes and recommended actions for each insight category to help address delays and misalignments effectively.

    The AI Insights window displays a timestamp indicating when insights were last generated. You can regenerate insights and recommendations if required to see the changes based on the latest available data.

    Users with the sn\_align\_core.apw\_admin role can configure severity thresholds and scoring factors for planning items. These settings control how the Portfolio insights skill classifies insight severity as Critical, Medium, or Low.

-   **[Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-workspace-ppw.md)**

    Manage strategic and operational demands in a unified experience in Portfolio Planning. This Next Experience interface consolidates demand creation, assessment, collaboration, and conversion in one place, eliminating context switching and reducing reliance on the classic Demand Workbench.

-   **[Create and manage demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/managing-demands-ppw.md)**
    -   Create and manage a demand in Next Experience for Demand Management using guided tabs. These tabs help you define alignment, estimate costs, and confirm readiness as you build out the demand.
    -   Collaborate on demands through Docs, which syncs execution and planning.
    -   View, add, and edit cost plans and budgeting details using related lists.
-   **[Use Playbook in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/use-playbooks-in-ppw.md)**

    Help teams manage demands with greater structure and consistency using Playbook in Next Experience for Demand Management.

    Playbooks enable you to define multiple governance processes across the organization using a low‑code/no‑code configuration experience. Create clear stages and guided activities from demand intake to completion using a default or custom playbook. Custom playbooks support multiple demand management processes across your organization.

-   **[Associate AI systems with demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/use-playbooks-in-ppw.md)**

    Use a playbook activity in Next Experience for Demand Management to associate AI systems with a demand. You can link impacted systems and add new ones directly within the demand workflow.

-   **[Portfolio plan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/work-prioritization-portfolio-planning.md)**
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
-   **[Plan efficiently with additional pre-defined lenses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/lens-and-portfolio-plans.md)**

    Use the Planning item lens to plan, prioritize, and roadmap work in Strategic Planning Workspace directly with planning items, without configuring organization structure, programs, portfolios, or products. The lens supports all enabled work item types, such as projects and demands, and can be used as a standalone lens or alongside other lenses.

-   **[Financials for planning items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/using-financials-spw.md)**

    View the financial baselines in investment currency and project currency after migrating them from Classic to Next Experience. Migrated financial baselines include actuals, costs, benefits, and budget values from the project currency to the investment currency.

    Using multicurrency, new and existing customers see only investment currency fields in demand and project records. Planned costs, actual costs, planned benefits, actual benefits, and budget fields are included in the financial baselines.


## UI changes

-   **[Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/demand-workspace-ppw.md)**
    -   The Demands icon has been added to the Portfolio Planning L1 menu to open the All Demands home page.
    -   The **State** field on the All Demands home page has been color-coded for each state value.
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

## Changed in this release

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/summarize-demands-in-ppw.md)**

    The demand summary is generated in the **AI Overview** tab instead of the **Details** tab. The skill is set to trigger automatically, that is, the summary is generated on landing in this tab. Auto-generation is on by default and applies to demands in Submitted, Screening, Qualified, or Approved states. You can define the trigger to manually trigger as well, where users must select the **Summarize** button to generate the summary.

-   **[AI skills for Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/ai-skills-in-demands-workspace-ppw.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[Access execution records from Portfolio Plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/access-demands-from-portfolio-planning-views.md)**

    The execution URL is updated on the planning item demand. New planning items demand will automatically use the new execution URL. The execution URLs on existing planning item demands continue to work but doesn't reflect the updated navigation. Run the **Update Demand Planning Item Execution URL** scheduled job to update the execution URL on the existing demands.


## Activation information

Install Portfolio Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/alignment-planner-workspace-landing-page.md)**

    Prioritize, roadmap, and track work when using traditional, agile, or hybrid methodologies with ServiceNow® Strategic Planning. Align strategy to execution by defining and tracking goals across your organization.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-business-management-rn-landing.md)

