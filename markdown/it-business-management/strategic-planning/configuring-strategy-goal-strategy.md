---
title: Configuring Strategy and Goals
description: Strategy and Goals in Strategic Planning Workspace requires no mandatory configuration to get started.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-planning/configuring-strategy-goal-strategy.html
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 3
breadcrumb: [Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Configuring Strategy and Goals

Strategy and Goals in Strategic Planning Workspace requires no mandatory configuration to get started.

Unlike portfolio plan goals, you can create and manage goals on a board without prerequisites or limitations. For example, portfolio plan goals do not display if they are not created at the lens entity level or if the assigned entity fields are empty. In Strategy and Goals, all goals that match the applied filter criteria or selected entity are visible on the board. For details, see [Managing boards in Strategic Planning Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/managing-boards-strategy.md) and [Managing strategy and goals using boards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/managing-strategic-goals-strategy.md).

## Optional configuration for Strategy and Goals

Although no mandatory configuration is required, you can perform the following administrative tasks based on your organization's needs.

-   **Migrate legacy goals data**

    If your organization uses the legacy goal and strategy tables \(Goal, Enterprise Strategy, Business Unit Strategy, and Strategic Objective\), you can migrate the existing data to the new tables by running a scheduled job. After migration, you can create boards and manage your existing goals and strategic priories. For details, see [Migrate existing goals data to Goal Framework tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/migrate-existing-goals-data-apw.md).

-   **Set display limit for goals**

    By default, 250 goals are displayed in the Goals page. To modify this limit, configure the value in the **sn\_align\_ws.goal\_hierarchy.max\_records** system property. For details, see [Set display limit for goals and targets in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/set-display-limits-for-goals-and-targets-spw.md).

-   **Customize goal and target labels**

    You can customize the labels for the Goal \[sn\_gf\_goal\] and Target \[sn\_gf\_goal\_target\] tables to match your organization's terminology. For example, you can rename Goal to Objective and Target to Key Result. For details, see [Customize label for Goal and Target tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/customize-labels-for-goal-and-target-tables.md).

-   **Configure assigned entities**

    You can define goals at any level in your organization without assigning them to a specific entity. Using advanced filter criteria when creating a board, you can manage a specific set of goals based on any goal field value. For example, you can create a board to manage goals that belong to the Chatbot team.

    \[Omitted image "board-goal-filter-team.png"\] Alt text: Creating goal-based board with Team filter.

    You can also create boards for your goals based on assigned entities. The default assigned entities are Business Unit \[business\_unit\], Department \[cmn\_department\], Company \[core\_company\], Product Model \[cmdb\_model\], Value Stream \[cmn\_value\_stream\], Initiative \[sn\_align\_core\_initiative\], and Strategic Program \[sn\_align\_core\_program\].

    To create boards based on assigned entities other than the defaults, create an entry in the assigned entity configuration. For details, see [Configure a table for an assigned entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/configure-assigned-entity-egm.md).

-   **Configure goal preferences**

    Configure goal preferences including the calendar type for goal setting, weighted average calculation for goal progress, and deletion settings for goals and targets. For details, see [Configure goal preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/configure-goal-preferences-apw.md).

-   **Configure reminders for target actuals**

    Configure reminders to automatically notify target owners and contributors to update actuals for their targets before the due date, based on the check-in frequency defined for each target. For details, see [Configure reminders for target actuals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/configure-reminders-for-target-actuals-strategy.md).

-   **Configure Goal insights generation**

    Activate the Goal insights generation scheduled job and configure the filter criteria to automatically generate AI-driven insights for a defined set of goals at a scheduled frequency. For details, see [Goal insights generation job](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-planning/configure-goal-insights-generation-job.md).


