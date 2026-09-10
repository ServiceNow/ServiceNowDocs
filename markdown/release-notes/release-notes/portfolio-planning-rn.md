---
title: Portfolio Planning release notes
description: The ServiceNow Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Zurich release.The ServiceNow Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Zurich release.The ServiceNow Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Portfolio Planning release notes

The ServiceNow® Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Zurich release.

## About Portfolio Planning

-   View the planned costs of your planning items for the past fiscal periods.
-   Use **Display mode** to switch between different views of the financials record page.
-   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans. View the roadmap-level milestone row while scrolling down the Roadmap page. Use different icons to distinguish item-level milestones.
-   Apply filters using string-type and Boolean field values to view the desired data.
-   Customize and apply a theme to your roadmap to match your organization’s standards.
-   Create and manage monetary benefit plans to capture and track projected and actual benefits.
-   Manage and run projects in various global currencies besides the functional currency using multicurrency.
-   Generate labor cost on sub-projects based on the resource assignments.

See [Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/portfolio-planning-app-landing-page.md) for more information.

## Activation and other requirements

**Important:** Portfolio Planning is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Portfolio Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-business-management-rn-landing.md)

## December 2025

The ServiceNow® Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Zurich release.

### What's new

-   **[Dynamic data linking in Docs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/docs-for-planning-items-in-ppw.md)**

    Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

    You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Scenario planning enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/enable-scenario-planning-in-portfolio-planning.md)**

    With the sn\_align\_core.apw\_admin role, you can enable or disable the scenario planning feature. The **sn\_align\_ws.is\_scenario\_planning\_disabled** system property allows you to enable or disable the scenario planning feature.


## Zurich

The ServiceNow® Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. Portfolio Planning was enhanced and updated in the Zurich release.

### What's new

-   **[Roadmap enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/planning-roadmaps-in-portfolio-planning.md)**
    -   Create custom themes for your roadmap bar colors to align with your organization’s standards.
    -   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans.
    -   View the roadmap-level milestone row while scrolling down the Roadmap page.
    -   Use different icons to distinguish item-level milestones.
-   **[Quick filters enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/quick-fiters-prioitization-roadmap-ppw.md)**

    Apply filters using string-type and Boolean field values across the Planning page to view the required dataset. These filters are saved as part of your user preferences, enabling you to access the same filtered data when you log back in and continue your planning seamlessly.

-   **[Financial enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/using-financials-pp.md)**
    -   View only the planned costs of your planning items to track the total cost of projects or demands.
    -   Use **Display mode** to switch between focused views to better plan and track the financials of your planning items.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate and track labor cost for sub-projects, based on the resource assignments of your sub-projects and planning items such as features and capabilities.

### What's changed

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Financials in Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/using-financials-pp.md)**
    -   Use the new **Display mode** in the Financials record page to select and view forecast, compare planned vs actual costs, planned costs, or allocate budget.
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

