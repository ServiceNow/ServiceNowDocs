---
title: Strategic Planning release notes
description: The ServiceNow Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
---

# Strategic Planning release notes

The ServiceNow® Strategic Planning application helps you accomplish end-to-end planning using a single workspace. Strategic Planning was enhanced and updated in the Yokohama release.

## Strategic Planning highlights for the Yokohama release

-   Reduce time and effort by using story recommendations from Now Assist to break down your epics and features in Enterprise Agile Planning \(EAP\).
-   Collaborate in real time on docs with multiple editors.
-   View the rolled-up financial costs and benefits data of your planning items on the new **Financials** tab in the Planning page.
-   View the financial data of planning items while creating multiple prioritization scenarios for efficient use of budget and to get better ROI.
-   Use dashboards to monitor performance, track progress, and make informed decisions related to ideas, feedback, planning, and execution.
-   Create, edit, and switch between views with display preferences for portfolio plans and free-form roadmaps.
-   Enhance the quality of planning item descriptions by enabling AI assistance.

See [Strategic Planning](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

**Important:** Strategic Planning is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Strategic Planning to Yokohama

After upgrading to Strategic Planning v4.7.0, the following changes apply to user preferences:

-   Custom view settings previously saved under user preferences will be cleared. You must reapply these changes and create views as needed. For instructions, see [Create a portfolio plan view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-portfolio-plan-view-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) and [Create a free-form roadmap view in Strategic Planning](https://www.servicenow.com/docs/access?context=create-free-form-roadmap-view-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).
-   Customizations made to the Timeline and Kanban views in the **Roadmap** tab, and the Kanban view in the **Prioritization** tab at the portfolio plan level, will be copied to the Default view of the portfolio plan. Similarly, any customizations made to the Timeline and Kanban views in the free-form roadmap will also be copied to the Default view of the free-form roadmap.

## New in the Yokohama release

-   **[Dashboards for data analysis and decision-making](https://www.servicenow.com/docs/access?context=dashboards-in-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Use dashboards to view key data and metrics, enabling you to monitor performance, track progress, and make informed decisions related to ideas, feedback, planning, and execution. Dashboards consolidate data from multiple sources into a single, easily digestible format. Each widget within a dashboard displays key data and metrics and may include visualizations. The default dashboards include the Product Idea Dashboard, Feedback Dashboard, Strategy Execution Dashboard, and Execution Dashboard.

    You can create or edit dashboards, copy an existing dashboard and customize it as needed, and share dashboards to collaborate with business stakeholders who have access to the portfolio plan.

-   **[Create and share views for portfolio plans and free-form roadmaps](https://www.servicenow.com/docs/access?context=managing-portfolio-plan-views-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    For portfolio plans - Create, edit, and switch between views with display preferences such as column selection, grouping, and filtering for portfolio plans. You can create personal views that are private to you, or public views that can be shared with stakeholders who have access to the portfolio plan. The portfolio plan view saves your display preferences across the **Prioritization**, **Roadmap**, **Capacity**, and **Financials** tabs.

    **Note:** Views are available only for the Planning module and are supported in live mode, but not in scenario mode.

    For free-form roadmaps - Create, edit, and switch between views with display preferences such as grouping, milestones selection, dependencies selection, and tracking mode for free-form roadmaps. You can create personal views that are private to you, or public views that can be shared with stakeholders who have access to the free-form roadmap.

-   **[Write planning item skill](https://www.servicenow.com/docs/access?context=refine-text-with-write-planning-item-skill&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Improve record quality and user satisfaction by enabling AI assistance in the **Description** field across all Strategic Planning Workspace forms, including product idea, demand, epic, project, capability, feature, and story.
    -   Enable text refinement with the **Elaborate** and **Shorten** options on planning items to support product managers and agile team members in creating and editing content more effectively.
-   **[Plan efficiently with additional pre-defined lenses](https://www.servicenow.com/docs/access?context=lens-alignment-planner-workspace&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Using the Digital Product lens, portfolio managers can plan, prioritize, and roadmap the work in the Strategic Planning Workspace based on the digital products by aligning with the business strategy.

    The lens is supported with the work items, epic, and product idea. With the Digital Product lens, you can also do high-level planning using the Product Enhancement entity. By default, the Product Enhancement entity is enabled for high-level planning.

-   **[Cycle time report for Agile teams in EAP dashboards](https://www.servicenow.com/docs/access?context=eap-agile-team-dashboard&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Analyze how long the stories take for your Agile team to move from an in-progress state to completion. Each bubble on the chart represents a story and the chart shows stories completed in the past 30 days. You can compare the cycle times of stories that have different story points and review the trend in the time taken by the team to complete them.

    Using this data, identify the stories that took longer to complete and analyze the reasons so that you can draft an action plan to optimize the team's cycle time in the future.

-   **[Kanban configuration for EAP teams](https://www.servicenow.com/docs/access?context=agile-configurations-in-eap&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Use the Kanban configuration for teams that don't prefer to work in an iteration-based schedule. You can activate the predefined Kanban configuration and add teams to your Agile structure or you can modify an existing configuration by setting the **Planning calendar** field to **None**.

-   **[Column filters in EAP Backlog](https://www.servicenow.com/docs/access?context=using-eap&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Quickly find the work items that you need by using column-level filters for the data on your EAP Backlog. You can filter on any column that is displayed on the **Backlog** tab.

-   **[Generate stories from epics and features using Now Assist for EAP](https://www.servicenow.com/docs/access?context=generate-stories-from-epics-now-assist-eap&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Break down epics and features into stories using the Now Assist Agile story generation skill in the EAP workspace. Using the available details such as name, description, docs content, and any existing stories, Now Assist provides story recommendations for your epic or feature. You can let Now Assist generate stories using its initial recommendations or you can choose to split or combine the story recommendations before prompting Now Assist to create the stories.

-   **[View financial data of your planning items at portfolio level](https://www.servicenow.com/docs/access?context=using-portfolio-financials-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   View the rolled-up financial costs and benefits data of your planning items such as Epics, Demands, and Projects at the portfolio level for different time scales and ranges.
    -   View the Budget, Planned, Variance, Actuals, and Remaining Estimates of the financials costs by expense type or cost type.
    -   View the Forecasts, Actuals, and Variance of monetary benefits.
-   **[Create a manage financial scenarios of planning items](https://www.servicenow.com/docs/access?context=optimizing-scenarios-in-strategic-planning&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Optimize your portfolio by creating financial scenarios to validate and arrive at a profitable outcome.
    -   Plan and manage the budget of planning items in simulation mode for efficient financial planning and to help prevent overspending.
    -   Manage prioritization and budget allocation of the planning items to meet business priorities.
    -   Compare scenarios financially and automatically allocate the planned budget to planning items from approved scenarios.
    -   Enable the **new budget allocation** property \(**sn\_invst\_pln.enable\_budget\_allocation\_v2**\) to perform financial analysis in scenario planning and take effective decisions by data-driven insights.
-   **[Real-time collaboration for EAP Docs](https://www.servicenow.com/docs/access?context=docs-for-eap-teams-and-planning-items&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Edit a doc page concurrently with multiple other editors. Colored cursors denote the current location of editors on the page. You can choose to show or hide these indicators.

    The real-time collaboration feature for docs is also available for planning items in the Strategic Planning Workspace. See [Docs for planning items in Strategic Planning](https://www.servicenow.com/docs/access?context=docs-for-planning-items-in-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US).

    **Note:** To use the full functionality of Docs v6.6.0 within Strategic Planning Workspace, ensure that you upgrade Strategic Planning Workspace to v4.5.0. For more information, see [KB2017926](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2017926).


## UI changes

-   **[Financials UI changes](https://www.servicenow.com/docs/access?context=using-portfolio-financials-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   New **Financials** tab in the Planning page.
    -   The name of the **ETC** field is changed to **Remaining Estimates**.
    -   The name of the **EAC** field is changed to **Forecast**.
    -   The name of the **Actuals to date** field is changed to **Actuals**.
    -   New Financials view in scenario planning.
    -   New financial widgets in the compare scenario page.
-   **[Skill name updates](https://www.servicenow.com/docs/access?context=alignment-planner-workspace-landing-page&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Renamed the Planning item Gen AI Docs to the Planning item doc summarization skill in Strategic Planning.
    -   Renamed the EAP Teams Gen AI Docs to the EAP doc summarization skill in Enterprise Agile Planning.
    -   Added the Write planning items skill in Strategic Planning.
-   **[Capacity Planning name updates](https://www.servicenow.com/docs/access?context=using-cap-plan-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Change in the name of the **Capacity Planning** tab to **Capacity** in the planning view.


## Changed in this release

-   **[Changes in planning item forms](https://www.servicenow.com/docs/access?context=epic-form&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    The dates in the **Planned start date** and **Planned end date** fields are editable for all planning item types other than Demand and Project planning item types. Also, the **State** field is editable for EAP planning items and its child items.


## Activation information

Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Now Assist lets you use generative AI skills in multiple SPM apps. With Now Assist for SPM, summarize product feedback, create stories for epics, generate concise project summaries, rephrase content for docs, create demands through a conversational experience, and quickly gain insights into projects.

-   **[Digital Product Release Workspace](https://www.servicenow.com/docs/access?context=dpr-workspace&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    ServiceNow Digital Product Release Workspace helps product managers track the planning items associated with the product enhancements that are defined in the Strategic Planning Workspace using the Digital Product lens.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

