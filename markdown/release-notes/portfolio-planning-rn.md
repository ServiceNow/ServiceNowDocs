---
title: Portfolio Planning release notes
description: The ServiceNow Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. See the following sections for release notes by version.The version 8.18.0 release consolidates governance in dedicated RIDAC pages within portfolio plans to reduce context-switching and improve portfolio visibility. Programs enhanced experience provides automatic dedicated planning views for every program with zero setup required. Additional enhancements include scenario approval email notifications, automated cost recalculation with exchange rate detection, and in-context financial field explanations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/portfolio-planning-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Portfolio Planning release notes

The ServiceNow® Portfolio Planning application helps you enhance traditional product and portfolio management by visualizing the alignment of work with organizational objectives. See the following sections for release notes by version.

## About Portfolio Planning

-   Prioritize, roadmap, and score planning items using portfolio plans with support for multiple lenses, private or shared views, and free-form roadmaps to align work with organizational strategy.
-   Plan and manage portfolio financials with rolled-up cost and benefit data, financial baselines, budget approvals, and scenario planning to optimize portfolio decisions and drive cost-effective outcomes.
-   Capture, assess, and prioritize demands through configurable playbooks, using AI to summarize and identify similar items, before converting them into work items with full financial tracking.
-   Track Risks, Issues, Decisions, Actions, and Changes \(RIDAC\), monitor capacity, and gain actionable insights through dashboards to maintain portfolio health and keep stakeholders informed.

See [Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-planning-app-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Portfolio Planning by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Version 8.18.0

The version 8.18.0 release consolidates governance in dedicated RIDAC pages within portfolio plans to reduce context-switching and improve portfolio visibility. Programs enhanced experience provides automatic dedicated planning views for every program with zero setup required. Additional enhancements include scenario approval email notifications, automated cost recalculation with exchange rate detection, and in-context financial field explanations.

### What's new

-   **[RIDAC for portfolio plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/portfolio-plan-ridac-ppw.md)**

    Access portfolio risks, issues, decisions, actions, and requested changes \(RIDAC\) directly from the portfolio plan using the dedicated RIDAC page within the portfolio plan. View all portfolio governance items in a single, integrated interface without navigating to the separate RIDAC menu. The RIDAC page reduces context-switching and improves portfolio visibility by consolidating governance data. The portfolio plan RIDAC displays the RIDAC items that match the portfolio plan's criteria or belong to the planning items of that portfolio plan.

-   **[Show or hide RIDAC page of a portfolio plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/show-or-hide-the-features-for-your-portfolio-plan-ppw.md)**

    As a portfolio manager, show or hide the RIDAC page of your portfolio plan. This capability helps you share only the portfolio plan data that matters to your stakeholders and restrict access to the other data.

-   **[Programs enhanced experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-ppw.md)**

    Access dedicated program planning views automatically created with zero setup. Navigate to the new Programs menu and click any program to open its dedicated plan with Prioritization, Roadmap, and Financials views. New programs get plans instantly; existing programs receive them through an automatic one-time backfill \(500 at a time, newest first\). Role-based access ensures users with the sn\_align\_core.ap\_read\_only role can read, users with the sn\_align\_core.apw\_user role can manage items, and program managers are automatic plan owners.

-   **[Program-scoped data with fiscal calendar support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-ppw.md)**

    View and manage program-scoped planning data in a focused, streamlined interface. Program plans display only that program's planning items. The Financials tab defaults to your fiscal calendar; if the fiscal calendar doesn't span the program dates, the system gracefully falls back to Gregorian with an explanatory message. Making the portfolio plan public and scenario planning for these program portfolio plans are hidden.

-   **[Automated email notification for scenario approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/approve-a-scenario-in-portfolio-planning.md)**

    Receive email notification when a scenario is approved. The system sends the notification to the scenario approver and portfolio owner. During the approval process, the portfolio plan becomes read-only to prevent unintended modifications and maintain data integrity.

-   **[Copy and customize the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/clone-customize-demand-summarization-skill-ppw.md)**

    Tailor demand summaries to your organization's process by copying the base demand summarization skill and customizing it with your own input fields, related entities, and prompt. When you activate a copy of the demand summarization skill, the previously active skill, either the base skill or an earlier copy, is automatically deactivated. Only one version of the skill can be active at a time.

-   **[Work with demands in Employee Slate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/my-demands-widget-ppw.md)**

    Create and track demands without leaving the conversation-first Employee Slate workspace. Describe the demand in a conversation to have matching catalog items identified and relevant fields prepopulated from your message, then track its status, activity, and progress using the new My Demands widget on your canvas or the standard Requests widget. Demands appear in Employee Slate only when both Project Workspace and Employee Slate Core apps are installed.


### What's changed

-   **Financials**

    Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.

-   **[Program planning updates and enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/program-portfolio-plan-ppw.md)**
    -   **Programs menu addition** — A new Programs menu has been added to the workspace as L2 menu, positioned below Portfolio Plan. This menu lists every program in your portfolio and provides single-click navigation to each program's enhanced planning view.
    -   **Role-based access for program planning** — Users with the sn\_align\_core.ap\_read\_only role have read access to program plans \(where they already have program-level read access\). Users with the sn\_align\_core.apw\_admin and program manager roles receive full access to create, update, and manage planning items within program plans.
-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/summarize-demands-in-ppw.md)**

    The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.

-   **Process Mining**

    Starting Brazil release, Process Mining Content Pack for SPM \(`com.snc.itbm_po`\) will be migrated to Process Mining Content Pack store application. Upgrade your instance to Brazil or higher releases. For more information, see [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining.md) documentation.


