---
title: Getting started with flows
description: Create a sample flow with a trigger and base system actions that requires an approval.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Getting started with flows

Create a sample flow with a trigger and base system actions that requires an approval.

Introduction to spokes, setting up an application, granting access, creating a flow, setting up an ATF test, and publishing the flow.

Watch this 3:34-minute video for an introduction to using Workflow Studio.

## Before you begin

Role required: flow\_designer

## About this task

A flow can include these components:

-   Trigger: An activity that initiates the flow, such as a record created in a specified table or a scheduled job.
-   Conditions: Statements that determine when or how an action runs. For example, run an action only if a field is over a certain value.
-   Actions: Operations executed by the system, such as a field value updated, approval requested, or a value logged.

To understand basic flows, create an expense approval flow. This flow:

1.  Runs when an Expenses record is created.
2.  Uses the total amount to determine which action to run.
3.  Approves the request if it is under the specified dollar amount.
4.  Requires manager approval if it is over a specified dollar amount. Another approver can be manually added.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow studio**.

2.  From the Workflow Studio Homepage, select **New** &gt; **Flow**.

3.  Specify a name, description, and optionally specify additional properties for the flow.

4.  Select **Build flow**.

5.  Select **Add a trigger**.

6.  From the list of triggers, select **Application** &gt; **Service catalog**.

    The flow runs whenever a user requests a service catalog item.

7.  Select **Done**.

8.  Select **Add an Action, Flow logic, or Subflow**.

9.  From Action, select **ServiceNow Core** &gt; **Send Email**.

10. Configure the action.

    1.  **Target Record**: On the Data pane, expand **Trigger - Service Catalog** and drag the **Requested Item Record** data pill.

    2.  **To**: Expand the **Requested Item Record** data pill and drag the Email data pill.

    3.  **Subject**: Add a subject for the email notification

    4.  **Body**: Add the email body.

    5.  Select **Done**.


## What to do next

Transform the Ask for Approval action into a reusable action using Workflow Studio. Actions enable flow designers to add complex actions to multiple flows with minimal configuration. See [Getting started with actions](getting-started-action.md).

