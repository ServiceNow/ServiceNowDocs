---
title: Collaborative Work Management \(CWM\) release notes
description: The ServiceNow Collaborative Work Management application centralizes tasks, documentation, and planning in a single workspace so teams can manage work without switching between applications. See the following sections for release notes by version.The September 2026 release of Collaborative Work Management \(CWM\) includes new features and updates to improve team collaboration and work management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/spm-cwm-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Strategic Portfolio Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Collaborative Work Management \(CWM\) release notes

The ServiceNow® Collaborative Work Management application centralizes tasks, documentation, and planning in a single workspace so teams can manage work without switching between applications. See the following sections for release notes by version.

## About Collaborative Work Management \(CWM\)

-   Centralize tasks, documentation, and planning in a single workspace organized around Spaces, so teams stop losing context switching between tools.
-   Configure your own workflow and Boards without admin involvement, using custom fields, work item types, and Dashboard, List, Gantt, or Kanban views.
-   Run sprints end-to-end with built-in Agile capabilities, including sprint planning, scrum tasks, and cross-team dependency tracking.
-   Reduce manual overhead with generative AI features that assist with task creation, formula building, and content generation.

See [Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/cwm-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install the Collaborative Work Management application \(sn\_cwm\) from the ServiceNow Store. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed. Role required: admin. For more information, see [Install Collaborative Work Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/install-cwm.md).


**Parent Topic:**[Strategic Portfolio Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-business-management-rn-landing.md)

## Version 11.0.1

The September 2026 release of Collaborative Work Management \(CWM\) includes new features and updates to improve team collaboration and work management.

### What's new

-   **[Create CWM tasks or stories from files or open prompts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/generate-tasks-cwm-boards.md)**

    Generate a batch of actionable tasks or stories for a Board by describing the work in an open prompt or uploading a reference file, such as meeting notes, brainstorming planning docs, or epic PRDs. AI analyzes the input, maps the results to your Board columns, and lets you review and select which items to add.

-   **[Create child tasks from CWM task types in List view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/generate-subtasks-for-cwm-tasks.md)**

    Break down a large or complex task into clear, assignable child tasks without manual work breakdown. AI analyzes the task's short description and description and generates the child tasks inline from the List view. This capability is available for CWM tasks and CWM custom task types.

-   **[Manage lists in CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/cwm-lists.md)**

    Access ready-made default lists of Agile and connected work records, or build and save your own custom lists from any table, without leaving the CWM workspace. The Lists panel under the Quick access section includes the **Default lists** and **My lists** tabs. You can filter, sort, group, and export records, or create and edit records directly from a list.

-   **[Manage work with Board dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/cwm-board-dashboards.md)**

    Every Board now includes a Dashboard tab, alongside List, Gantt, Kanban, and Sprint planning, with two predefined shared dashboards added automatically: Team progress for waterfall work and Team sprint tracker for agile work. Space owners and editors can also create additional dashboards, add predefined or custom widgets bound to any Board column, and rename, duplicate, or delete them. Every dashboard is shared with everyone with access to the Board and can be shared with a direct link.

-   **[Enable sprint data collection for burnup and burndown widgets in a dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/cwm-activate-daily-sprint-data-collection-job.md)**

    Activate the **CWM Daily Sprint Data Collection** scheduled job to populate the Sprint burnup and Sprint burndown widgets in the Board dashboards. Once the job is active, data for active sprints is collected daily, and chart data appears starting the day after the job first runs.


### What's changed

-   **[Import tasks entry point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/import-tasks-cwm-board.md)**

    The **Import tasks** option moved from a standalone button on the Board header into the **Create with Otto** menu, alongside the **Generate tasks** option. From the Board header, select **Create with Otto**, and then select **Import tasks** to start the import wizard.

-   **[Sprint sync between EAP and CWM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/cwm-integration-with-eap.md)**

    Sprint name, state, capacity, and dates sync automatically from Enterprise Agile Planning to Collaborative Work Management for Agile teams that use non-calendar-based iterations, in addition to calendar-based teams.


### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


