---
title: Project Portfolio Management release notes
description: The ServiceNow Project Portfolio Management application combines innovation, demand, project, program, resource, and portfolio management into a single suite. Teams can plan and execute work using a waterfall, Agile, or hybrid methodology.The Brazil Early Availability release introduces cloning of AI skills and updates to AI skills in Project Portfolio Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/spm-ppm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Project Portfolio Management release notes

The ServiceNow® Project Portfolio Management application combines innovation, demand, project, program, resource, and portfolio management into a single suite. Teams can plan and execute work using a waterfall, Agile, or hybrid methodology.

## About Project Portfolio Management \(PPM\)

-   Gather and evaluate ideas, and promote accepted ideas to a demand, story, epic, or project.
-   Assess, approve, and promote demands to strategic and operational work.
-   Manage projects, programs, and portfolios, along with their resources and financials, from a single suite of applications.
-   Execute work using a traditional waterfall methodology, an Agile approach, or a hybrid of the two.

See [Project Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/c_ProjectPortfolioSuite.md) for more information.

## Activation and other requirements

-   **Activation information**

    Activate the PPM Standard plugin \(com.snc.financial\_planning\_pmo\) if you have the admin role. This plugin installs the Project Portfolio Management applications, along with their user roles and tables. For more information, see [Activate PPM Standard \(Project Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/t_ActivateProjectPortfolioSuiteWithFinancials.md).

-   **Upgrade information**

    Users who already have Project Portfolio Management can upgrade to PPM Standard. New users must purchase PPM Standard. For more information, see [Activate PPM Standard \(Project Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/t_ActivateProjectPortfolioSuiteWithFinancials.md).


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Brazil Early Availability

The Brazil Early Availability release introduces cloning of AI skills and updates to AI skills in Project Portfolio Management.

### What's new

-   **Budget Overrun insight card**

    Identify portfolio plans at risk of exceeding their approved budget with the new Budget Overrun insight card in Portfolio Insights. The card compares each planning item's current fiscal year forecast against its approved budget and flags items where the forecast is higher. Flagged items include a root cause analysis — grouped by cost type and driven by factors such as rate changes, effort overruns, or foreign exchange impact — along with recommended actions like re-forecasting with finance or initiating change control.

-   **Cost Variance insight card**

    Identify cost plans whose actual spend is running over or under plan for the current fiscal period with the new Cost Variance insight card in Portfolio Insights. The card flags cost plans where the variance between actual and planned costs exceeds a configurable threshold, in either direction, and groups the root causes by driver — such as rate-driven, effort or hours overrun, or actuals below plan — along with recommended next steps for each.

-   **[Copy and customize the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/clone-customize-the-demand-summarization-skill-ppm.md)**

    Tailor demand summaries to your organization's process by copying the base demand summarization skill and customizing it with your own input fields, related entities, and prompt. When you activate a copy of the demand summarization skill, the previously active skill, either the base skill or an earlier copy, is automatically deactivated. Only one version of the skill can be active at a time.

-   **[Work with demands in Employee Slate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/my-demands-widget-ppm.md)**

    Create and track demands without leaving the conversation-first Employee Slate workspace. Describe the demand in a conversation to have matching catalog items identified and relevant fields prepopulated from your message, then track its status, activity, and progress using the new My Demands widget on your canvas or the standard Requests widget. Demands appear in Employee Slate only when both Project Workspace and Employee Slate Core apps are installed.


### What's changed

-   **Portfolio Insights card order**

    The AI Insights panel now displays insight cards in a fixed order based on prominence and impact: Projects at risk, Budget Overrun, Cost Variance, Items past planned end date, Delayed start, and Planned versus approved misalignment. Review the most critical financial and schedule risks first.

-   **Insight explanations in Portfolio Insights**

    Each card in Portfolio Insights now includes an info icon. Select the icon to open a popover with a plain-language explanation of what the insight measures and how it's calculated, so you can interpret the insight without leaving the panel.

-   **[Navigation to Project Workspace in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/t_CreateAProject.md#steps_cmz_5wd_tw)**

    View and access Project Workspace in Next Experience when you access project workspace from the All navigation menu.

-   **[Summarize demands with the demand summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/demand-summary-demand-classic.md)**

    The default trigger is not set to **Automatic** for demands in any state. You can select how you want the skill to be triggered for any state.


### What's deprecated or removed

-   **[Planning console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/c_TheProjectPlanningConsole.md)**

    Starting Brazil release, Planning console is deprecated and is no longer supported. Project managers can [access Project Workspace using Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/access-new-project-workspace.md) to work on project planning.

-   **Process Mining**

    Starting Brazil release, Process Mining Content Pack for SPM \(`com.snc.itbm_po`\) will be migrated to Process Mining Content Pack store application. Upgrade your instance to Brazil or higher releases. For more information, see [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining.md) documentation.

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


