---
title: Configure Automations in Smart Assessment template
description: Set up automations to trigger predefined actions whenever assessment templates are published. You can define action set types that determine how and when automated actions execute within the assessment workflow.
locale: en-US
release: zurich
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-02-12"
reading_time_minutes: 2
breadcrumb: [Smart Assessment for Workplace Case and Task, Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configure Automations in Smart Assessment template

Set up automations to trigger predefined actions whenever assessment templates are published. You can define action set types that determine how and when automated actions execute within the assessment workflow.

## Before you begin

Role required: admin

## About this task

You can configure conditional action sets using if-then logic based on assessment responses, or create standalone action sets for unconditional execution to streamline case management workflows.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  From the Assessment templates list, select the published template.

3.  On the Assessment Workspace page, select **New template**.

    The Assessment Workspace page displays where you can specify the template details.

4.  Under the Automations tab, select **Create automation**.

5.  Enter the automation name and provide context.

6.  Select **Create**.

7.  Select **Add conditional action set** to define a group of conditions and actions.

    -   Select **Set condition** in the If section, and select **New condition set**.
    -   In the Set conditions dialog, define evaluation criteria:
        -   **Select field**

            Choose the field to evaluate.Navigate through Response based &gt; Section to access assessment question responses, or select standard case fields.

        -   **Select operator**

            Choose the comparison operator.

        -   **Enter value**

            Specify the value to compare against the selected field.

    -   Use **and** or **or** to add more conditions.
    -   Select **Save** to apply conditions
    -   Under the then section, select **Set action** and configure the action to execute when conditions are met.
    -   Select **+ Set another action** to add multiple actions that execute sequentially.
    -   Configure if nothing matches behavior to define fallback actions when no conditions are satisfied.
8.  Select Add standalone action set to execute actions unconditionally.

    -   Under the then section, select **Set action** and configure the action to execute.
    -   In the Set actions dialog, select Action type and the Workplace case details.
    -   Select **+ Set another action** to add multiple actions that execute sequentially.
9.  Select **Activate** to enable the automation.![](../../workplace-service-delivery/images/automations.png)


## Result

The automation is now active and will execute configured actions when the assessment template is published. Conditional action sets evaluate specified criteria before executing actions, while standalone action sets execute unconditionally.

**Note:**

-   To edit automation, select the automation, and select ![](../../workplace-service-delivery/images/wsd_edit_threedots.png) and select**Edit details**.
-   To delete automation, select the automation, and select ![](../../workplace-service-delivery/images/wsd_edit_threedots.png) and select **Delete automation**.

**Parent Topic:**[Smart Assessment for Workplace Case and Task](smart-assessment-for-workplace-case-and-task.md)

