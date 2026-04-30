---
title: Getting started with flows
description: Create a sample flow with a trigger and base system actions that requires an approval.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-08-07"
reading_time_minutes: 3
breadcrumb: [Flows, Explore, Workflow Studio, Build workflows]
---

# Getting started with flows

Create a sample flow with a trigger and base system actions that requires an approval.

Video explaining how to create a sample flow to ask for approval.

Watch this 3:34-minute video for an introduction to creating a flow in Workflow Studio.

## Before you begin

Role required: flow\_designer

## About this task

A flow can include these components:

-   Trigger: An activity that initiates the flow, such as a record created in a specified table or a scheduled job.
-   Conditions: Statements that determine when or how an action runs. For example, run an action only if a field is over a certain value.
-   Actions: Operations executed by the system, such as a field value updated, approval requested, or a value logged.

To understand basic flows, create an catalog item approval flow. This flow:

1.  Runs when a catalog item is requested.
2.  Sends an email to notify the requester.
3.  Initiates manager approval if it is over a specified dollar amount.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow studio**.

2.  On the Workflow Studio Homepage, select **New** &gt; **Flow**.

3.  Specify a name, description, and optionally specify additional properties for the flow.

4.  Select **Build flow**.

5.  After the flow is built, add a trigger to start the flow.

    1.  Select **Add a trigger**.

    2.  From the list of triggers, select **Application** &gt; **Service catalog**.

    3.  Select **Done**.

    The flow runs whenever a user requests a service catalog item.

6.  Select **Add an Action, Flow logic, or Subflow**.

    First, we will add a Send Email action that sends an email when a catalog item is requested, followed by an IF flow logic and an Ask for approval action that will initiate approval if the item cost is more than 1000 USD.

7.  Add a Send Email action to send an email to the requester when a catalog item is requested.

    1.  From **Action**, select **ServiceNow Core** &gt; **Send Email**.

    2.  Configure the action.

        |Field|Action|
        |-----|------|
        |**Target Record**|On the Data pane, expand **Trigger - Service Catalog** and drag the **Requested Item Record** data pill.|
        |**To**|Expand the **Requested Item Record** data pill and drag the Email data pill.|
        |**Subject**|Add a subject for the email notification.|
        |**Body**|Add the email body.|

8.  Add an IF flow logic and an Ask for approval action so that we can initiate the approval if the item cost is more than 1000 USD.

    1.  Select **Add an Action, Flow logic, or Subflow** &gt; **Flow logic** &gt; **If**.

    2.  In **Condition 1**, dot-walk or drag the **Requested Item Record** &gt; **Price** data pill.

    3.  Select **greater than**.

    4.  Enter `1000`.

    5.  Select **Done**.

    6.  Select **Action** &gt; **Ask For Approval**.

    7.  In **Record**, dot-walk or drag the **Requested Item Record** data pill.

    8.  Specify the **Rules** as **Approve** when **Anyone approves** and dot-walk or drag the **Requested Item Record** &gt; **Opened by** &gt; **Manager** data pill.

    9.  Select **Done**.

9.  **Test** and **Activate** the flow.


## What to do next

Transform the Ask for Approval action into a reusable action using Workflow Studio. Actions enable flow designers to add complex actions to multiple flows with minimal configuration. See [Getting started with actions](getting-started-action.md).

-   **[Build your first flow in Workflow Studio](build-your-first-flow.md)**  
Step through an example of how to build, test, and activate a sample flow in Workflow Studio.
-   **[Build a flow from a template in App Engine Studio](build-flow-from-template.md)**  
Step through an example of how to build, test, and activate a flow using a flow template in App Engine Studio.
-   **[Use the Workflow Studio help panel](use-flow-designer-help-panel.md)**  
Browse topics in the side help panel to learn more about building flows and actions, working with data and spokes, and stepping through guided tours in Workflow Studio.

**Parent Topic:**[Exploring flows](../../workflow-studio/concept/exploring-flows.md)

