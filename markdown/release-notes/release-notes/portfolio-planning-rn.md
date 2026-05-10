---
title: Portfolio Planning release notes
description: The ServiceNow Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Portfolio Planning release notes

The ServiceNow® Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Australia release.

## Portfolio Planning highlights for the Australia release

-   Create and manage demands from the Next Experience for Demand Management in Portfolio Planning.
-   Guide demand managers and users through predefined stages and actions for each demand process using Playbook in Next Experience for Demand Management.
-   Link AI systems to a demand using a Playbook activity in Next Experience for Demand Management.
-   Review the financial records of your planning items in both project currency and investment currency when you migrate them from Classic to Next Experience.
-   Create financial baselines with multicurrency to capture, view, and track the financial health of your planning item using project baselines and investment baselines.

See [Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/portfolio-planning-app-landing-page.md) for more information.

**Important:** Portfolio Planning is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[AI-generated insights for portfolio plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/now-assist-for-strategic-portfolio-management-spm/view-portfolio-insights.md)**

    Gain AI-generated insights into planning items within a portfolio plan using the Portfolio insights skill. Identify planning items that are delayed beyond their planned end date, have delayed starts, or have misalignments between planned and approved dates. View AI-generated top root causes and recommended actions for each insight category to help address delays and misalignments effectively.

    Users with the sn\_align\_core.apw\_admin role assigned can configure severity scoring for planning items to control how the Portfolio insights skill classifies insight severity as Critical, Medium, or Low.

-   **[Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/demand-workspace-ppw.md)**

    Manage strategic and operational demands in a unified experience in Portfolio Planning. This Next Experience interface consolidates demand creation, assessment, collaboration, and conversion in one place, eliminating context switching and reducing reliance on the classic Demand Workbench.

-   **[Create and manage demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/managing-demands-ppw.md)**
    -   Create and manage a demand in Next Experience for Demand Management using guided tabs. These tabs help you define alignment, estimate costs, and confirm readiness as you build out the demand.
    -   Collaborate on demands through Docs, which syncs execution and planning.
    -   View, add, and edit cost plans and budgeting details using related lists.
-   **[Use Playbook in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/use-playbooks-in-ppw.md)**

    Help teams manage demands with greater structure and consistency using Playbook in Next Experience for Demand Management.

    Playbooks enable you to define multiple governance processes across the organization using a low‑code/no‑code configuration experience. Create clear stages and guided activities from demand intake to completion by using a default playbook or creating a custom playbook to support your organization’s multiple demand management processes.

-   **[Associate AI systems with demands in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/use-playbooks-in-ppw.md)**

    Use a playbook activity in Next Experience for Demand Management to associate AI systems with a demand. You can link impacted systems and add new ones directly within the demand workflow.

-   **[Portfolio plan enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/work-prioritization-portfolio-planning.md)**
    -   Access the Hierarchy tab directly from the Planning page, located next to the Prioritization tab. This new placement replaces the previous access point within the Prioritization tab, providing a more efficient way to view and manage planning items.
    -   Save filter views specific to the Hierarchy tab without affecting views in the Prioritization tab.
    -   View planning items in the new Hierarchy tab on the Planning page, now sorted using global rank when available. Drag and drop is supported for lowest‑level items, enabling you to rerank them within their groups.
    -   Share a portfolio plan using the Copy link option. This provides access to existing users who have access to the portfolio plan.
    -   Expand or collapse portfolio plan header to maximize screen space while planning.
    -   Edit the default view within a portfolio plan and save changes using the Save view option.
-   **[Financials for planning items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/using-financials-spw.md)**

    View the financial baselines in investment currency and project currency after migrating them from Classic to Next Experience. Migrated financial baselines include actuals, costs, benefits, and budget values from the project currency to the investment currency.

    Using multicurrency, new and existing customers see only investment currency fields in demand and project records. Planned costs, actual costs, planned benefits, actual benefits, and budget fields are included in the financial baselines.

    -   .
        -           -   
## UI changes

-   **[Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/portfolio-planning/demand-workspace-ppw.md)**
    -   The Demands icon ![](../../product/spw-demand/images/demands-icon.png) has been added to the Portfolio Planning L1 menu to open the All Demands home page.
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

## Activation information

Install Portfolio Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/alignment-planner-workspace-landing-page.md)**

    Prioritize, roadmap, and track work when using traditional, agile, or hybrid methodologies with ServiceNow® Strategic Planning. Align strategy to execution by defining and tracking goals across your organization.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

