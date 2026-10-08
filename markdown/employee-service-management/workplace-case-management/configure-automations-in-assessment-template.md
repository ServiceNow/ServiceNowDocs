---
title: Configure automations in a Smart Assessment template
description: Set up automations that run predefined actions when an assessment template is published, using conditional or standalone action sets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/employee-service-management/workplace-case-management/configure-automations-in-assessment-template.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Smart Assessment for workplace cases and tasks, Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Configure automations in a Smart Assessment template

Set up automations that run predefined actions when an assessment template is published, using conditional or standalone action sets.

## Before you begin

Role required: admin

## About this task

You can configure conditional action sets that use if-then logic based on assessment responses, or create standalone action sets that run unconditionally.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  From the Assessment templates list, select the published template.

3.  On the Assessment Workspace page, select **New template**.

    The Assessment Workspace page opens, where you can specify the template details.

4.  On the **Automations** tab, select **Create automation**.

5.  Enter the automation name and provide context.

6.  Select **Create**.

7.  Select **Add conditional action set** to define a group of conditions and actions.

    -   Select **Set condition** in the If section, and select **New condition set**.
    -   In the Set conditions dialog box, define the evaluation criteria:
        -   **Select field**

            Field to evaluate. To access assessment question responses, navigate to **Response based** &gt; **Section**, or select a standard case field.

        -   **Select operator**

            Comparison operator to apply to the selected field.

        -   **Enter value**

            Value to compare against the selected field.

    -   Use **and** or **or** to add more conditions.
    -   Select **Save** to apply the conditions.
    -   In the Then section, select **Set action** and configure the action to execute when conditions are met.
    -   Select **+ Set another action** to add multiple actions that execute sequentially.
    -   Configure the **If nothing matches** behavior to define fallback actions when no conditions are met.
8.  Select **Add standalone action set** to execute actions unconditionally.

    -   In the Then section, select **Set action** and configure the action to execute.
    -   In the Set actions dialog box, select the **Action type** and the Workplace case details.
    -   Select **+ Set another action** to add multiple actions that execute sequentially.
9.  Select **Activate** to enable the automation.\[Omitted image "automations.png"\] Alt text:


## Result

The automation is active and runs the configured actions when the assessment template is published. Conditional action sets evaluate specified criteria before executing actions, while standalone action sets execute unconditionally.

**Note:**

-   To edit an automation, select the automation, select \[Omitted image "wsd\_edit\_threedots.png"\] Alt text:, and then select **Edit details**.
-   To delete an automation, select the automation, select \[Omitted image "wsd\_edit\_threedots.png"\] Alt text:, and then select **Delete automation**.

**Parent Topic:**[Smart Assessment for workplace cases and tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/employee-service-management/workplace-case-management/smart-assessment-for-workplace-case-and-task.md)

