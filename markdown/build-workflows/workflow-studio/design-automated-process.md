---
title: Create a sample playbook
description: Create a sample playbook to standardize and automate how Service Desk agents handle chat interactions with VIP users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/design-automated-process.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-06-12"
reading_time_minutes: 6
breadcrumb: [Building your first playbook, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Create a sample playbook

Create a sample playbook to standardize and automate how Service Desk agents handle chat interactions with VIP users.

## Before you begin

-   Role required: admin or playbook.admin

## About this task

In the following procedure, you can step through an example of how to digitize a manual business process on the ServiceNow AI Platform using Playbooks in Workflow Studio to standardize and automate how Service Desk agents handle chat interactions with VIP users.

The manual business process for this example consists of the following stages:

1.  **Identify and Log**: A Service Desk agent learns of an issue that a VIP user is facing while chatting with the user in a messaging application. The Service Desk agent creates an interaction record to track this issue.
2.  **Classify and Diagnose**: The Service Desk agent associates an incident record with the interaction and sets the incident's priority to High. The agent then enters the Assigned To user for the incident.
3.  **Communicate Work in Progress**: The assignee updates the incident record's state to Work in Progress and emails the VIP user when progress is made on the incident.
4.  **Resolve**: When the incident is resolved, the assignee emails the resolution information to the VIP user.

## Procedure

1.  Create a playbook named **Handle Interactions with VIPs**.

    1.  Navigate to **All** &gt; **Workflow Studio** &gt; **Playbooks**.

        The Workflow Studio landing page opens with the Playbooks list displayed by default.

    2.  In the upper-right corner, select **New** &gt; **Playbook**.

    3.  Fill in the following fields.

        |Field|Inputs|
        |-----|------|
        |**Playbook name**|`Handle Interactions with VIPs`|
        |**Application**|`Global`|
        |**Description**|`This process defines how Service Desk agents can handle interaction records that are created for VIP users.`|

    4.  Select **Build playbook**.

        The builder displays in **Diagram view** by default, but you can select **Board view** to switch between views anytime as you build your playbook.

        \[Omitted image "board-view.png"\] Alt text: Diagram and Board view toggle

    The Playbooks design environment appears.

2.  Specify the table.

    1.  Select the **Start** node.

        The Playbook properties side panel opens.

    2.  In the **Parent table** field, enter and select `Interaction`.

    3.  Select **Save and close**.

3.  Create the trigger.

    \[Omitted image "sample-playbook-trigger.png"\] Alt text: Sample playbook trigger defition.

    1.  Open the trigger panel \[Omitted image "triggers-icon.png"\].

    2.  Select **Add trigger** &gt; **When record is created**.

        The trigger definition panel opens.

    3.  Under **Conditions**, use the condition builder to add the following condition.

        **\[Opened for-&gt;VIP\]** **\[is\]** **\[True\]**.

    4.  Select **Save and close**.

4.  Add a stage for each phase of your process.

    \[Omitted image "sample-playbook-add-stage.png"\] Alt text: Adding the first stage in the sample playbook.

    1.  Select **+** &gt; **Add a stage**.

        Repeat this step to add three stages.

    2.  Enter the **Label** and **Description** for each stage.

        |Stage|Label|Description|
        |-----|-----|-----------|
        |1|`Classify and Diagnose`|`Associate an incident with the interaction`|
        |2|`Communicate Work in Progress`|`Notify VIP of work in progress`|
        |3|`Resolve`|`Resolve incident and share resolution details`|

    3.  Select **Save and close**.

5.  Add the **Create incident from interaction** activity to the **Classify and Diagnose** stage.

    \[Omitted image "sample-playbook-add-activity.png"\] Alt text: Add activity to stage.

    1.  Under the **Classify and Diagnose** stage, select **+** &gt; **Add an activity**.

    2.  In the activity picker, select **Common Activities** &gt; **Non-Interactive** &gt; **Create New Record**.

    3.  On the **Automation** tab, in the **Table Name** list, select **Incident \[incident\]**.

    4.  From the **Fields** list, select **Assigned To**.

    5.  Next to the **Assigned To** field, select the data pill picker icon \(\[Omitted image "data-pill-picker-icon.png"\] Alt text: Data pill picker icon\).

    6.  Dot-walk to **Context** &gt; **Parent Record - interaction** &gt; **Assigned To**.

    7.  Select **Add Field** and add the following four fields.

        |Field|Values to enter|
        |-----|---------------|
        |**Impact**|`2 - Moderate`|
        |**Urgency**|`1 - High`|
        |**Short Description**|Dot-walk to **Context** &gt; **Parent Record - interaction** &gt; **Short Description**|
        |**Caller**|Dot-walk to **Context** &gt; **Parent Record - interaction** &gt; **Opened for**|

    8.  Select **Save and close**.

    The **Create incident from interaction** activity automatically maps the Assigned To and Short Description fields from the interaction record to the incident record when your process runs.

6.  Add the **Wait for assignee to update** activity to the **Communicate Work in Progress** stage.

    1.  Under the **Communicate Work in Progress** stage, select **+** &gt; **Add an activity**.

    2.  In the activity picker, select **Common Activities** &gt; **Interactive** &gt; **Wait For Condition**.

    3.  In the activity properties panel's **Label** field, enter `Wait for assignee to update`.

    4.  On the **Automation** tab, in the **Table** list, select `Incident`.

    5.  Next to the **Record** field, select the data pill picker icon \(\[Omitted image "data-pill-picker-icon.png"\] Alt text: Data pill picker icon\).

    6.  Dot-walk to **1.1 Create incident from interaction** &gt; **Incident records**.

    7.  Use the condition builder to add the following condition to your activity:

        **\[Updated by\]** **\[is\]** **\[Activities** &gt; **1.1 Create incident from interactions** &gt; **Incident record** &gt; **Assigned to\]**.

    8.  Select **Save and close**.

    The **Wait for assignee to update** activity pauses the process until the Assigned To user for the Incident record updates the record.

7.  Add the **Send update to VIP** activity to the **Communicate Work in Progress** stage.

    1.  Under the **Communicate Work in Progress** stage, select **+** &gt; **Add an activity**.

    2.  In the activity picker, select **Common Activities** &gt; **Interactive** &gt; **Instruction**.

    3.  In the activity properties panel's **Label** field, enter `Send update to VIP`.

    4.  In the **When to start** field, leave **After Previous** selected, and then select **Save**.

    5.  Click the **Send update to VIP** activity card.

    6.  Select the **Automation** tab.

    7.  In the **Message** field, enter `Notify the VIP user that work on their issue is in progress`.

    8.  Leave the **Wait for user input** field's value as **Yes**.

    9.  Select **Save and close**.

    The **Send update to VIP** activity prompts the agent to send an email to the VIP user when the assignee for the incident record makes an update.

8.  Add the **Wait for incident resolution** activity to the **Resolve** stage.

    1.  Under the **Resolve** stage, select **+** &gt; **Add an activity**.

    2.  In the activity picker, select **Common Activities** &gt; **Interactive** &gt; **Wait For Condition**.

    3.  In the activity properties panel's **Label** field, enter `Wait for incident resolution`.

    4.  Select the **Automation** tab.

    5.  In the **Table** field, select **Incident**.

    6.  Next to the **Record** field, select the data pill picker icon \(\[Omitted image "data-pill-picker-icon.png"\] Alt text: Data pill picker icon\).

    7.  Dot-walk to **Activities** &gt; **1.1 Create incident from interaction** &gt; **Incident record**.

    8.  Use the condition builder to add the following condition to your activity:

        **\[State\]** **\[is\]** **\[Resolved\]**.

    9.  Select **Save and close**.

    The **Wait for incident resolution** activity pauses the process until the Incident's state becomes **\[Resolved\]**.

9.  Add the **Share resolution details with VIP** activity to the **Resolve** stage.

    1.  Under the **Resolve** stage, select **+** &gt; **Add an activity**.

    2.  In the activity picker, select **Common Activities** &gt; **Interactive** &gt; **Instruction**.

    3.  In the activity properties panel's **Label** field, enter `Share resolution details with VIP`.

    4.  Select the **Automation** tab.

    5.  In the **Message** field, enter `Provide the Resolution Notes from the Incident record in an email to the VIP user`.

    6.  Leave the **Wait for user input** field's value as **Yes**.

    7.  Select **Save and close**.

    The **Share resolution details with VIP** activity prompts the agent to send the issue resolution details to the VIP user.

10. In the main header, select **Activate** so that your process runs when triggered.


## Result

Your process appears in as a playbook. Here, agents and fulfillers can get a task-oriented view of the automated business process. Agents can step through the activities that you set up to see where the record is in the overall process.

## What to do next

Customize the Playbook layout for deployment. To learn more, see [Customizing the Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-customize-playbook.md)

**Parent Topic:**[Building your first playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/getting-started-processes.md)

