---
title: Project Workspace release notes
description: The ServiceNow Project Workspace application provides an interactive UI to enable project managers to define, plan, track, and monitor projects from a single location.Keep project tasks and their resource assignments in sync by preventing task dates from moving earlier than logged actuals.Organize and access your work more efficiently with the new Lists view, which provides quick navigation to projects, RIDAC items, programs, and portfolios with customizable list options.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/spm-project-workspace-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Project Workspace, project management, planning console, resource management, Project Workspace, date validation, task actuals, related list, HTML, resource assignment, planning, project types, module visibility, Enterprise-Wide Deployment, Lists view, navigation, custom lists, RIDAC]
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Project Workspace release notes

The ServiceNow® Project Workspace application provides an interactive UI to enable project managers to define, plan, track, and monitor projects from a single location.

## About Project Workspace

-   Define, plan, track, and monitor projects from a single interactive workspace with an intuitive UI.
-   Manage project tasks, dependencies, and timelines using an integrated planning console with grid and Gantt views.
-   Allocate and track resources with the resource assignment pane, including allocation heatmaps and effort tracking.
-   Create and compare schedule and financial baselines to monitor project performance against original plans.
-   Collaborate with stakeholders through activity streams, attachments, and status reporting capabilities.

See [Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-workspace-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    The Project Workspace plugin \(com.snc.project\_workspace\) is available on ServiceNow® Store. Install the plugin to activate the application.


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Version 7.7.3

Keep project tasks and their resource assignments in sync by preventing task dates from moving earlier than logged actuals.

### What's new

-   **[Project type module visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/configure-project-type-pw.md)**

    Show only the modules that are relevant to each project type in Project Workspace. In the **Show modules** section of the project type form, select the modules to display for projects of that type: **Playbook**, **Planning**, **Details**, **Financials**, **RIDAC**, **Resource**, **Analytics**, **Docs**, and **Status Report**. All modules are selected by default, and projects without a project type display all modules. Role-based access to each module continues to apply.


-   **Tour guides**

    Introduced guided tours for Ask Otto button in planning view and Accept button in the AI Identified Risk page.


### What's changed

-   **[Managing projects with Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/use-projects-pw.md)**

    On project tasks with logged actuals, you can't change the Planned start or move the end date earlier than the last logged actual, whether you edit dates directly or a dependency recalculates them. When the Actual start and end dates are present, the restriction applies to them. This keeps the tasks and assignments in sync.

-   **[Preview attachments and manage excel files with dedicated prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/generate-project-using-ai-pw.md)**

    When you generate a project plan, a preview of the attachment now appears before you proceed. This matches the existing behavior of [generating tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/generate-tasks-using-ai-pw.md). Excel attachments are now processed with a dedicated prompt tailored to tabular data, separate from word, pdf, and powerpoint attachments. This applies when generating a project plan or inserting tasks.


## Version 7.6.2

Organize and access your work more efficiently with the new Lists view, which provides quick navigation to projects, RIDAC items, programs, and portfolios with customizable list options.

### What's new

-   **[List view for centralized navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/use-projects-pw.md#section_oz3_352_kkc)**

    Centralized location for accessing all project-related entities such as My projects, All projects, Project templates, and RIDAC categories \(Risks, Issues, Decisions, Actions, Request changes\), streamlining navigation and improving productivity. Create and save custom lists in the My lists tab to organize your work according to your preferences.

-   **[Recalculate planned costs for projects](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/fin-recalculate-costs-pws.md)**

    Recalculate the cost plans, benefit plans, and their rolled-up investment-level values directly from the Financials view using the **Recalculate costs** option.

-   **[Create dynamic docs template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/create-a-status-report-template-project-workspace.md)**

    Customize the docs based on your organization and project requirements using the dynamic docs template in Project Workspace.


### What's changed

-   **UI options for RIDAC**

    RIDAC section is expanded by default to view AI-Identified Risks and RIDAC.

-   **UI options for Financials**
    -   Added in-context help \(hover info icons\) on the Financials page widgets, explaining how the key fields like Budget, EAC, Planned Cost, Actuals, Return, ROI, and NPV are calculated.
    -   Added **Recalculate costs** option to recalculate the planned costs and planned benefit when labor rates or budget reference rates change.
-   **UI options for Project Workspace**
    -   Added **Export status report** in the more options menu in the Details page.
    -   Added **Save as new template** and **Project Diagnostics** in the more options menu in the Planning page.

### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


