---
title: Configuring Strategy and Goals
description: Strategy and Goals in Strategic Planning Workspace requires no mandatory configuration to get started.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Strategy and Goals, Strategic Planning, Strategic Portfolio Management]
---

# Configuring Strategy and Goals

Strategy and Goals in Strategic Planning Workspace requires no mandatory configuration to get started.

Unlike portfolio plan goals, you can create and manage goals on a board without prerequisites or limitations. For example, portfolio plan goals do not display if they are not created at the lens entity level or if the assigned entity fields are empty. In Strategy and Goals, all goals that match the applied filter criteria or selected entity are visible on the board. For details, see [Managing boards in Strategic Planning Workspace](managing-boards-strategy.md) and [Managing strategy and goals using boards](managing-strategic-goals-strategy.md).

## Optional configuration for Strategy and Goals

Although no mandatory configuration is required, you can perform the following administrative tasks based on your organization's needs.

-   **Migrate legacy goals data**

    If your organization uses the legacy goal and strategy tables \(Goal, Enterprise Strategy, Business Unit Strategy, and Strategic Objective\), you can migrate the existing data to the new tables by running a scheduled job. After migration, you can create boards and manage your existing goals and strategic priories. For details, see [Migrate existing goals data to Goal Framework tables](../../spw-goals/task/migrate-existing-goals-data-apw.md).

-   **Set display limit for goals**

    By default, 250 goals are displayed in the Goals page. To modify this limit, configure the value in the **sn\_align\_ws.goal\_hierarchy.max\_records** system property. For details, see [Set display limit for goals and targets in Strategic Planning](../../spw-goals/task/set-display-limits-for-goals-and-targets-spw.md).

-   **Customize goal and target labels**

    You can customize the labels for the Goal \[sn\_gf\_goal\] and Target \[sn\_gf\_goal\_target\] tables to match your organization's terminology. For example, you can rename Goal to Objective and Target to Key Result. For details, see [Customize label for Goal and Target tables](../../spw-goals/task/customize-labels-for-goal-and-target-tables.md).

-   **Configure assigned entities**

    You can define goals at any level in your organization without assigning them to a specific entity. Using advanced filter criteria when creating a board, you can manage a specific set of goals based on any goal field value. For example, you can create a board to manage goals that belong to the Chatbot team.

    ![Creating goal-based board with Team filter.](../image/board-goal-filter-team.png)

    You can also create boards for your goals based on assigned entities. The default assigned entities are Business Unit \[business\_unit\], Department \[cmn\_department\], Company \[core\_company\], Product Model \[cmdb\_model\], Value Stream \[cmn\_value\_stream\], Initiative \[sn\_align\_core\_initiative\], and Strategic Program \[sn\_align\_core\_program\].

    To create boards based on assigned entities other than the defaults, create an entry in the assigned entity configuration. For details, see [Configure a table for an assigned entity](../../spw-goals/task/configure-assigned-entity-egm.md).

-   **Configure goal preferences**

    Configure goal preferences including the calendar type for goal setting, weighted average calculation for goal progress, and deletion settings for goals and targets. For details, see [Configure goal preferences](../../spw-goals/task/configure-goal-preferences-apw.md).

-   **Configure reminders for target actuals**

    Configure reminders to automatically notify target owners and contributors to update actuals for their targets before the due date, based on the check-in frequency defined for each target. For details, see [Configure reminders for target actuals](../task/configure-reminders-for-target-actuals-strategy.md).


