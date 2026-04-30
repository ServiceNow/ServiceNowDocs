---
title: Strategic Planning release notes
description: The ServiceNow Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
---

# Strategic Planning release notes

The ServiceNow® Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Zurich release.

## Strategic Planning highlights for the Zurich release

-   Categorize your strategic priorities, goals, planning items, and execution items—projects and demands as Artificial Intelligence to track and monitor their progress from the AI Control Tower workspace.
-   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans. View the roadmap-level milestone row while scrolling down the Roadmap page. Use different icons to distinguish item-level milestones.
-   Apply filters using string-type and boolean field values to view the desired data on the Planning and Scoring pages.
-   Work on financial planning for various planning items such as Capabilities, Features, and so on.
-   View the planned costs of your planning items for the past fiscal periods.
-   Use Display mode to switch between different views of the financials record page.
-   Create and manage monetary benefit plans to capture and track projected and actual benefits.
-   Manage and run projects in various global currencies besides the functional currency using multicurrency.
-   Generate labor cost on sub-projects based on the resource assignments.

See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US) for more information.

**Important:** Strategic Planning is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Strategic Planning to Zurich

After upgrading to Strategic Planning v4.8.0, the existing **Investment type** and **Investment class** fields will appear as **Investment type \(Deprecated\)** and **Investment class \(Deprecated\)** respectively across the Planning page including in the Prioritization and Roadmap views and in the Scenario Planning page. The values from these deprecated fields will be automatically copied to the new **Investment type** and **Investment class** fields.

If you previously applied filters or personalized your view using the deprecated fields, you must update those configurations to use the new **Investment type** and **Investment class** fields across the workspace—including in the Prioritization and Roadmap views on the Planning page, as well as in the Scenario Planning page.

## New in the Zurich release

-   **[Strategic Planning and AI Control Tower](https://www.servicenow.com/docs/access?context=better-together-with-other-apps-spw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Categorize your strategic priorities, goals, planning items, and execution items—projects and demands as Artificial Intelligence to track and monitor strategy progress from the AI Control Tower workspace.

    Use the **Type** field for strategic priorities, the **Category** field for goals, the **Investment type** field for planning items - to classify them as Artificial Intelligence and monitor their progress in the AI Control Tower workspace.

-   **[Integrate Enterprise Agile Planning \(EAP\) with Atlassian Jira](https://www.servicenow.com/docs/access?context=spw-jira-landing&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Facilitate execution of the work planned in EAP and executed in Jira. With this integration, enable seamless tracking of work across tools with bidirectional sync between Jira and EAP. Key updates made in one system, such as a status change or field update for Epics and Stories, will automatically reflect in the other. This integration ensures your team can collaborate and track development efforts without switching contexts, reducing manual effort and improving visibility across platforms.

-   **[Enterprise Agile Planning \(EAP\) integration with CWM](https://www.servicenow.com/docs/access?context=agile-sprint-planning-in-cwm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Enhance visibility, planning, and execution for your teams with seamless integration between EAP and CWM.

    For Agile teams managing non-agile work items such as incidents and change tasks, this integration bridges the gap by automatically creating a dedicated Space and Board in CWM. Agile work is seamlessly brought over via Connected Work, while EAP sprints are reflected directly in CWM’s Sprint planning view, thus enabling unified planning across work types. Teams can plan work for their sprints and update work status directly from the CWM Board, with performance reports in EAP dynamically reflecting these changes. This integration enables teams to manage their full scope of work from a single, connected workspace.

-   **[Dynamic data linking in Docs](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Keep record information in your documentation always current and reduce manual effort with the Dynamic data linking feature in Docs. You can now reference any ServiceNow application record and Docs will automatically reflect the latest updates from those records. For example, if you add a reference to a Project record, the reference will show the latest field information of the project in Docs without requiring manual edits. Clicking the project reference opens up the project form so that you can view the full details of the project record and make any necessary changes. Dynamic linking also enables adding references to a particular field of a record, such as Assigned to of an Incident record.

    You can add references from any ServiceNow table you have access to, with no setup or configuration needed, thereby eliminate the hassle of switching between applications to copy and paste data from various records into Docs.

-   **[Portfolio plan enhancements](https://www.servicenow.com/docs/access?context=create-portfolio-plans-in-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Create portfolio plans for AI-related items by applying a filter on the planning item tables, setting the **Investment type** field value to **Artificial Intelligence** during portfolio plan creation. This allows you to focus exclusively on AI-related items.
    -   With the sn\_align\_core.apw\_admin role, you can update the following system properties:
        -   **sn\_align\_core.planning\_item\_types\_allow\_list** - Defines the planning item types that can be configured and allowed for a portfolio plan.
        -   **glide.ui.sn\_align\_core\_dependency\_activity.fields** - Enables activity stream for the dependency formatter fields.
        -   **sn\_align\_ws.gantt\_show\_higher\_planning\_upper\_entities** - Enables display of entire hierarchy of lens structure from top to bottom in prioritization hierarchy view for high-level portfolio plans.
        -   **sn\_align\_ws.portfolio\_plan\_items\_limit** - Defines the number of planning items to be loaded on the planning page.
-   **[Roadmap enhancements](https://www.servicenow.com/docs/access?context=roadmaps-in-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Create custom themes for your roadmap bar colors to align with your organization’s standards.
    -   Experience consistent roadmap bar colors for choice list attribute values across all portfolio plans.
    -   View the roadmap-level milestone row while scrolling down the Roadmap page.
    -   Use different icons to distinguish item-level milestones.
    -   Match milestone colors with their status labels across the roadmap, milestone popover, and side panel. For example, a missed milestone displays the same color in all locations.
    -   With the sn\_align\_core.apw\_admin role, you can define the number of milestone items to be loaded in the Roadmap tab. The **sn\_align\_ws.item\_milestone\_limit** system property allows you to define the number of milestone items to be loaded in the Roadmap tab.
    -   With the sn\_align\_core.apw\_admin role, you can define the list of planning item types that can be created in a free-form roadmap. The **sn\_align\_ws.freeform\_planning\_items\_creation\_list** system property allows you to define the list of planning item types that can be created in a free-form roadmap.
-   **[Scenario planning enhancements](https://www.servicenow.com/docs/access?context=enable-scenario-planning-in-strategic-planning&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    With the sn\_align\_core.apw\_admin role, you can enable or disable the scenario planning feature. The **sn\_align\_ws.is\_scenario\_planning\_disabled** system property allows you to enable or disable the scenario planning feature.

-   **[Quick filters enhancements](https://www.servicenow.com/docs/access?context=managing-backlog-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Apply filters using string-type and boolean field values across the Planning page and Scoring page to view the required dataset. These filters are saved as part of your user preferences, enabling you to access the same filtered data when you log back in and continue your planning seamlessly.

-   **[Investment type and Investment class fields on the Planning item table](https://www.servicenow.com/docs/access?context=planning-item-form&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    The **Investment type** and **Investment class** fields have been added to the Planning item \[sn\_align\_core\_planning\_item\] table to enable these attributes to be defined at the parent planning item level.

    A new value, **Artificial Intelligence**, has also been added to the **Investment type** field to categorize a planning item as an Artificial Intelligence initiative.

-   **[Goal management enhancements](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   With the sn\_gf\_goal\_admin role, you can update goal-specific system properties:
        -   **sn\_align\_ws.goal\_hierarchy.max\_records** - Defines the number of targets to load on the Hierarchy tab in the Targets view. The default value is 250.
        -   **glide.ui.sn\_gf\_goal\_activity.fields** - Enables activity stream for fields of the goals.
    -   Experience faster loading of goals data, even when large volumes of data are present.
    -   With the sn\_gf.goal\_admin role, you can edit any goal and target as needed, even when you aren’t the owner or contributor of a goal or target.
    -   With both the sn\_gf\_goal\_admin and sn\_apw\_advanced.spw\_goal\_user roles, you can edit target breakdowns as needed.
-   **[Financial enhancements](https://www.servicenow.com/docs/access?context=using-financials-spw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   View only the planned costs of your planning items to track the total cost of your planning items.
    -   Use Display mode to switch between focused views to better plan and track the financials of your planning items.
    -   Manage the planned and actual monetary benefit plans for your projects to identify the financial performance of your project using the Cost and benefits screen.
    -   Use multicurrency to view and manage financial records of the project in Investment currency, which can be different from your functional currency. Manage multiple financial records such as planned and actual expenses, planned and actual benefits, and so on.
    -   Generate and track labor cost for sub-projects, based on the resource assignments of your sub-projects and planning items such as features and capabilities.

## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Financials UI changes](https://www.servicenow.com/docs/access?context=using-financials-spw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
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

## Changed in this release

-   **[Investment type and Investment class fields](https://www.servicenow.com/docs/access?context=planning-item-form&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    The **Investment type** and **Investment class** fields have been deprecated from the Project and Demand planning item tables. These fields are now created at the parent level in the Planning item \[sn\_align\_core\_planning\_item\] table.

-   **[Goal management](https://www.servicenow.com/docs/access?context=managing-goals-in-alignment-planner-workspace&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    By default, only active goals—those goals with the **Active** field set to **true**—are displayed across the workspace. This change applies to the **Dashboards** and **Goals and targets** tabs on the Goals page, the **Goal**/**Parent goal** reference fields in all applicable tables, and all relevant dashboards.

-   **[Default related list view changes for Stories](https://www.servicenow.com/docs/access?context=create-single-or-multiple-child-items-for-epic-in-eap&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    In the Stories list for an Epic, Feature, or Capability in the Enterprise Agile Planning workspace, the Assignment group and Sprint columns in the default related list view are replaced with the EAP team and Iteration columns.

-   **[Enhancements to tables in Docs](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**
    -   Resize the column width of a table per your preference.
    -   Add color to single or multiple table cells.

## Deprecations

The **Investment class** and **Investment type** fields have been deprecated from the Project \[sn\_align\_core\_project\] and Demand \[sn\_align\_core\_demand\] tables.

## Activation information

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[AI Control Tower](https://www.servicenow.com/docs/access?context=ai-control-tower-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    ServiceNow AI Control Tower allows you to track and monitor all your strategic priorities, goals, targets, planning items, and execution items—projects and demands categorized as Artificial Intelligence in the Strategic Planning Workspace.

-   **[Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)**

    Now Assist enables you to use generative AI skills in multiple SPM apps. With Now Assist for SPM, summarize product feedback, create stories for epics, generate concise project summaries, rephrase content for docs, create demands through a conversational experience, and quickly gain insights into projects.

-   **[Digital Product Release Workspace](https://www.servicenow.com/docs/access?context=dpr-workspace&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)**

    ServiceNow Digital Product Release Workspace helps product managers track the planning items associated with the product enhancements that are defined in the Strategic Planning Workspace using the Digital Product lens.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

