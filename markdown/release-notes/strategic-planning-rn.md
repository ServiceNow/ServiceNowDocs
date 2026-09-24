---
title: Strategic Planning release notes
description: The ServiceNow Strategic Planning application helps you accomplish end-to-end planning using a single workspace. See the following sections for release notes by version.The version 4.18.0 delivers dedicated RIDAC pages within portfolio plans to consolidate portfolio governance \(risks, issues, decisions, actions, requested changes\) in one interface. Programs enhanced experience provides automatic dedicated planning views for every program with zero setup required. Additional enhancements include automated cost recalculation, scenario approval notifications, automatic target status calculation, and Scrum configuration options in Enterprise Agile Planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/strategic-planning-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Strategic Planning release notes

The ServiceNow® Strategic Planning application helps you accomplish end-to-end planning using a single workspace. See the following sections for release notes by version.

## About Strategic Planning

-   Define and manage strategic plans, goals, and targets while aligning planning items across portfolio plans, enterprise agile iterations, and organizational hierarchies to drive business outcomes.
-   Prioritize, roadmap, and score work items using predefined or custom lenses, with support for capacity planning, financial planning, and scenario planning to optimize portfolio decisions.
-   Capture and assess customer feedback and demands through configurable playbooks, using AI to summarize, identify similar items, and accelerate prioritization before converting them into work items.
-   Track risks, issues, decisions, actions, and changes \(RIDAC\) across planning items, iterations, and goals, and gain actionable insights through dashboards covering strategy, planning, feedback, and execution.

See [Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/alignment-planner-workspace-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Strategic Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Version 4.18.0

The version 4.18.0 delivers dedicated RIDAC pages within portfolio plans to consolidate portfolio governance \(risks, issues, decisions, actions, requested changes\) in one interface. Programs enhanced experience provides automatic dedicated planning views for every program with zero setup required. Additional enhancements include automated cost recalculation, scenario approval notifications, automatic target status calculation, and Scrum configuration options in Enterprise Agile Planning.

### What's new

-   **[RIDAC for portfolio plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-plan-ridac-spw.md)**

    Access portfolio risks, issues, decisions, actions, and requested changes \(RIDAC\) directly from the portfolio plan using the dedicated RIDAC page within the portfolio plan. View all portfolio governance items in a single, integrated interface without navigating to the separate RIDAC menu. The RIDAC page reduces context-switching and improves portfolio visibility by consolidating governance data. The portfolio plan RIDAC displays the RIDAC items that match the portfolio plan's criteria or belong to the planning items of that portfolio plan.

-   **[Show or hide RIDAC page of a portfolio plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/show-or-hide-the-features-for-your-portfolio-plan-spw.md)**

    As a portfolio manager, show or hide the RIDAC page of your portfolio plan. This capability helps you share only the portfolio plan data that matters to your stakeholders and restrict access to the other data.

-   **[Programs enhanced experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-spw.md)**

    Access dedicated program planning views automatically created with zero setup. Navigate to the new Programs menu and click any program to open its dedicated plan with Prioritization, Roadmap, Kanban, and Financials views. New programs get plans instantly; existing programs receive them through an automatic one-time backfill \(500 at a time, newest first\). Role-based access ensures users with the sn\_align\_core.ap\_read\_only role can read, users with the sn\_align\_core.apw\_user role can manage items, and program managers are automatic plan owners.

-   **[Program-scoped data with fiscal calendar support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-spw.md)**

    View and manage program-scoped planning data in a focused, streamlined interface. Program plans display only that program's planning items. The Financials tab defaults to your fiscal calendar; if the fiscal calendar doesn't span the program dates, the system gracefully falls back to Gregorian with an explanatory message. Making the portfolio plan public and scenario planning for these program portfolio plans are hidden.

-   **[Automated email notification for scenario approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/approve-a-scenario-in-strategic-planning.md)**

    Receive email notification when a scenario is approved. The system sends the notification to the scenario approver and portfolio owner. During the approval process, the portfolio plan becomes read-only to prevent unintended modifications and maintain data integrity.

-   **[Automatic status calculation for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/automatic-status-calculation-targets-spw.md)**

    Automatically determine target status based on actual achievement percentages. When you enter actual values for a target period, the system compares the achievement percentage against predefined thresholds and automatically assigns a status \(Green, Yellow, or Red\). This eliminates manual status selection, reducing data entry errors and improving organizational governance.

    Status is calculated and updated when you enter actual values using the formula: \(\(Actual Value - Start Value\) / \(Planned Target - Start Value\)\) x 100. Target owners can override automatically calculated status values at any time. If you update the actual value after a manual override, the system recalculates the status automatically.

-   **[Configure automatic status calculation thresholds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-automatic-status-calculation-spw.md)**

    Enable administrators to customize automatic status calculation thresholds and enable or disable the feature based on organizational requirements. By default, automatic status calculation is enabled with system-defined thresholds of Green \(≥90%\), Yellow \(75-89%\), and Red \(&lt;75%\).

    Administrators can adjust threshold percentages using the system property **sn\_gfa.target.auto\_status.thresholds**. To disable automatic status calculation and revert to manual status selection, set the system property to `false`.

-   **[Scrum Configuration in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/agile-configurations-in-eap.md)**

    Set up teams that run Sprints without a Planning Interval above them by using the Scrum Configuration in Enterprise Agile Planning. It defines a single team level of the type Agile Team and allows the Epic and Story work item types. Story is the default work item type for that level and is mapped to the new **Scrum Sprint** planning calendar. The **Epic methodology** field is set to **Scrum**. Like the other default configurations, the Scrum Configuration is inactive until you activate it.

-   **[Unique iteration cadence for each team in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/simplified-iteration-creation-in-eap.md)**

    Let each team set its own iteration dates by selecting **Allow unique cadence for each team** on an Enterprise Agile Planning configuration. If the configuration has planning calendars at more than one team level, each top-level team receives its own calendar. If the configuration has a single level of iterations, such as Sprints only, the iterations carry their own start and end dates instead of following a planning calendar entry. Teams that you add after you select this option receive a unique calendar, and teams that already exist continue to use the default calendar of the configuration.

-   **[Spillover and New scope fields on iterations in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/start-or-complete-iteration-in-eap.md)**

    See how the scope of a Sprint moved during its run by using the **Spillover** and **New scope** fields on the Enterprise agile iteration \[sn\_apw\_advanced\_eap\_iteration\] record. Spillover is the sum of the story points of the committed stories that are no longer in the iteration when it completes. New scope is the sum of the story points of the stories that were added after the iteration started. Both fields are read-only and are calculated when you complete the iteration. Select a value to open the stories that it counts.

-   **[Copy and customize the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/clone-customize-demand-summarization-skill.md)**

    Tailor demand summaries to your organization's process by copying the base demand summarization skill and customizing it with your own input fields, related entities, and prompt. When you activate a copy of the demand summarization skill, the previously active skill, either the base skill or an earlier copy, is automatically deactivated. Only one version of the skill can be active at a time.

-   **[Work with demands in Employee Slate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/my-demands-widget.md)**

    Create and track demands without leaving the conversation-first Employee Slate workspace. Describe the demand in a conversation to have matching catalog items identified and relevant fields prepopulated from your message, then track its status, activity, and progress using the new My Demands widget on your canvas or the standard Requests widget. Demands appear in Employee Slate only when both Project Workspace and Employee Slate Core apps are installed.


### What's changed

-   **Financials**

    Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.

-   **[Enterprise Agile Planning configuration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/create-eap-configuration.md)**
    -   The **Have unique calendars** option is renamed to **Allow unique cadence for each team**.
    -   An EAP admin can now clear the **Allow unique cadence for each team** option after selecting it. Selecting the option doesn't change the calendars or the iterations that already exist.
    -   The **Scrum Sprint** planning calendar type is available by default, alongside **Planning Interval** and **Sprint**.
-   **[Iteration dates in Enterprise Agile Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/edit-pi-sprint-iteration-details-in-eap.md)**
    -   The **Enterprise agile calendar entry** field on the Enterprise agile iteration \[sn\_apw\_advanced\_eap\_iteration\] table is no longer mandatory, which supports iterations that carry their own start and end dates. A fix script makes the field optional when you upgrade.
    -   Users with the `sn_apw_advanced.eap_user` role can set the start date and the end date while they create an iteration. They can change those dates afterward on an iteration that doesn't follow a planning calendar entry. However, changing the dates on an iteration that follows a planning calendar entry still requires the `sn_apw_advanced.eap_scrum_master` role.
-   **[Sprint sync with Agile Development 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/sync-eap-and-agile-2.md)**
    -   Sprints that don't follow a planning calendar entry now sync to Agile Development 2.0 by using the start date and the end date on the iteration.
    -   Changing the start date or the end date of an iteration now updates the dates on the corresponding Sprint in Agile Development 2.0.
-   **[Program planning updates and enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-spw.md)**
    -   **Programs menu addition** — A new Programs menu has been added to the workspace as L2 menu, positioned below Portfolio Plan. This menu lists every program in your portfolio and provides single-click navigation to each program's enhanced planning view.
    -   **Role-based access for program planning** — Users with the sn\_align\_core.ap\_read\_only role have read access to program plans \(where they already have program-level read access\). Users with the sn\_align\_core.apw\_admin and program manager roles receive full access to create, update, and manage planning items within program plans
-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/summarize-demand-in-demand-workspace.md)**

    The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **Process Mining**

    Starting Brazil release, Process Mining Content Pack for SPM \(`com.snc.itbm_po`\) will be migrated to Process Mining Content Pack store application. Upgrade your instance to Brazil or higher releases. For more information, see [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining.md) documentation.


