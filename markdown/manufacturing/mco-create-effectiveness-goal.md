---
title: Create an effectiveness goal
description: Create an effectiveness goal from a remediation action or remediation action plan to track the outcome of a fix instead of closing the action without measuring its result.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-create-effectiveness-goal.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [create, effectiveness goal, remediation action, supporting goal, target]
breadcrumb: [Create a product quality investigation, Product quality investigation, MCO workspace, Use, Manufacturing Commercial Operations]
---

# Create an effectiveness goal

Create an effectiveness goal from a remediation action or remediation action plan to track the outcome of a fix instead of closing the action without measuring its result.

## Before you begin

Role required: admin or sn\_mfg\_qm.product\_quality\_investigation\_member or sn\_mfg\_qm.product\_non\_conformance\_case\_resolver

## About this task

You can create an effectiveness goal from a remediation action, such as a containment, correction, corrective, or preventive action, or from a remediation action plan.

## Procedure

1.  Navigate to **Workspaces** &gt; **CRM Workspace** &gt; **List** &gt; **Product Quality Investigation**.

2.  Open the remediation action or remediation action plan record that you want to measure.

    -   On a remediation action plan: visible while the plan is Draft, Pending review, Approved, Rejected, or In progress.
    -   On a remediation action: visible while the action is New, In progress, In review, or Review complete.
3.  Select **Create effectiveness goal**.

    **Note:** It is visible only while the source record is in a non-closed state.

    The system creates an effectiveness goal record that extends the Goals framework table.

4.  On the effectiveness goal form, fill in the [Effectiveness goal form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-effectiveness-goal-form.md) fields.

5.  To add a sub-goal, select **New** under the **Supporting Goal** related list.

    The parent goal field auto-populates with the effectiveness goal you're working from.

6.  Select **Qualitative Targets** and add qualitative targets.

    The unit of measure you select on a target determines whether the target displays under the qualitative.

7.  Select **Quantitative Targets** and add quantitative targets.

    The unit of measure you select on a target determines whether the target displays under the quantitative.

8.  Select **Save**.

    The effectiveness goal can be linked to additional remediation actions. Multiple actions can share a single effectiveness goal through the many-to-many relationship between actions and effectiveness goals.


-   **[Create a qualitative target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-qualitative-targets.md)**  
Create a qualitative target for an effectiveness record to define and track non-numeric success criteria for a product quality investigation.
-   **[Create a quantitative target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-quantitative-targets.md)**  
Create a quantitative target to define measurable numeric criteria for an effectiveness goal in a product quality investigation.
-   **[Supporting goals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-supporting-goals.md)**  


**Parent Topic:**[Create a product quality investigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/manufacturing/mco-create-product-quality-investigation.md)

