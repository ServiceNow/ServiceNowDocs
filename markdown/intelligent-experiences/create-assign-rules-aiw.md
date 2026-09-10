---
title: Create assignment rules for an AI specialist
description: Route work to an AI specialist using assignment rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/create-assign-rules-aiw.html
release: australia
topic_type: task
last_updated: "2026-04-08"
reading_time_minutes: 1
breadcrumb: [Configure, Autonomous Workforce, Enable AI experiences]
---

# Create assignment rules for an AI specialist

Route work to an AI specialist using assignment rules.

## Before you begin

Role required: assignment\_rule\_admin or admin

## About this task

An AI specialist can't assign itself tasks. You must assign tickets to the AI specialist like any other user. If you want to automate assignment, you can either create assignment rules or you can configure Advanced Work Assignment. The following procedure outlines the steps for creating an assignment rule for your AI specialist. To learn more about assignment rules, see [Create an assignment rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AssignmentModuleRule.md) on the documentation site. For more information about using AWA, see the [documentation for Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/awa-application-landing-page.md).

## Procedure

1.  Navigate to **All** &gt; **System Policy** &gt; **Rules** &gt; **Assignment**.

2.  Select **New**.

3.  In the **Name** field, enter a name for your assignment rule, such as "AI L1 Service Desk."

4.  In the **Applies to** tab, select the table and filter conditions for which tasks you want the AI Specialist to handle.

5.  In the **Assign to** tab, enter the name of the AI specialist in the **User** field.

6.  Select **Submit** to create the assignment rule.


## Result

Your AI specialist is now automatically routed cases that match the filter conditions you set.

## What to do next

After your AI specialist receives work, you can track its activity or performance.

-   [Track AI specialist activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-aiw-activity.md)
-   [View AI specialist performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/view-aiw-performance.md)

