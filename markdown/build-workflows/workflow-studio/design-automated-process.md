---
title: Design an automated process
description: Transform an example manual business process into a well-designed, automated process that runs on the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Getting started with Playbooks, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Design an automated process

Transform an example manual business process into a well-designed, automated process that runs on the ServiceNow AI Platform®.

## Before you begin

-   Enable the **Process Automation Designer for App Engine \[com.glide.pad.license\]** plugin with a subscription to the ServiceNow AI Platform App Engine. For more information, see [Activate playbooks](../concept/activate-process-automation-designer.md#).
-   Follow the steps to Configure a Playbook user experience.
-   Ensure that your current application is set to **Global**. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).
-   Role required: admin or playbook.admin

## About this task

In the following procedure, you can step through an example of how to digitize a manual business process on the ServiceNow AI Platform using Playbooks in Workflow Studio. In this example, you can use Playbooks to standardize and automate how Service Desk agents handle chat interactions with VIP users.

The manual business process for this example consists of the following stages:

1.  **Identify and Log**: A Service Desk agent learns of an issue that a VIP user is facing while chatting with the user in a messaging application. The Service Desk agent creates an interaction record to track this issue.
2.  **Classify and Diagnose**: The Service Desk agent associates an incident record with the interaction and sets the incident's priority to High. The agent then enters the Assigned To user for the incident.
3.  **Communicate Work in Progress**: The assignee updates the incident record's state to Work in Progress and emails the VIP user when progress is made on the incident.
4.  **Resolve**: When the incident is resolved, the assignee emails the resolution information to the VIP user.

## Procedure

1.  Create a playbook named **Handle Interactions with VIPs**.

    1.  Navigate to **Process Automation** &gt; **Workflow Studio** &gt; **Playbooks**.

    2.  In the main header, click **Create a new process**.

    3.  On the form, fill in the fields.

        |Field|Action|
        |-----|------|
        |Label|Enter `Handle Interactions with VIPs`.|
        |Description|Enter `This process defines how Service Desk agents can handle interaction records that are created for VIP users.`|
        |Application|Select **Global**.|

    4.  Click **Select a trigger**.

    5.  Click the **Define your own trigger conditions for when your process runs** option.

    6.  From the list of trigger options, select **Record Create**.

    7.  Click **Set your trigger conditions**.

    8.  In the Table list, select **Interaction \[interaction\]**.

    9.  Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) to add the following condition to your trigger:

        **\[Opened for-&gt;VIP\]** **\[is\]** **\[True\]**.

    10. Click **Go to Designer**.

    The Playbooks design environment appears.

2.  Add a stage for each stage in your process.

    1.  Click **+ Add stage** to add the first stage to your process.

    2.  In the stage properties panel's **Label** field, enter `Classify and Diagnose`.

        **Note:** Because the **Identify and Log** stage triggers this process, don't add it as a stage.

    3.  In the **Description** field, enter `Associate an incident with the interaction`.

    4.  In the **When to start** field, leave **Immediately** selected, and then click **Save**.

    5.  Click **+ Add stage** to add another stage to your process.

    6.  In the stage side panel's **Label** field, enter `Communicate Work in Progress`.

    7.  In the **Description** field, enter `Notify VIP of work in progress`.

    8.  In the **When to start** field, leave **After Previous** selected, and then click **Save**.

    9.  Click **+ Add stage** to add the final stage to your process.

    10. In the stage side panel's **Label** field, enter `Resolve`.

    11. In the **Description** field, enter `Resolve incident and share resolution details`.

    12. In the **When to start** field, leave **After Previous** selected, and then click **Save**.

3.  Add the **Create incident from interaction** activity to the **Classify and Diagnose** stage.

    1.  Under the **Classify and Diagnose** stage, click **+ Add an activity**.

    2.  In the activity picker, select **Common Activities**, and then select **Automated Create Record** under Non-Interactive.

    3.  In the activity properties panel's **Label** field, enter `Create incident from interaction`.

    4.  In the **When to start** field, leave **Immediately** selected, and then click **Save**.

    5.  Click the **Create incident from interaction** activity card.

    6.  In the activity properties panel, click **Configure activity**.

    7.  On the Configure your activity screen, locate the Variables section under Inputs.

    8.  In the Table Name list, select **Incident \[incident\]**.

    9.  From the Fields list, select **Assigned To**.

    10. Next to the **Assigned To** field, select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker-icon.png)\).

    11. Dot-walk to the Interaction record's **Assigned To** field by selecting **Context** &gt; **Input Record - interaction** &gt; **Assigned To**.

    12. In the Fields list, select **Impact** and then select **2 - Moderate**.

    13. Under **Fields**, select **Urgency** and then select **1 - High**.

    14. In the Fields list, select **Short Description**.

    15. Dot-walk to the Interaction record's **Short description** field by selecting **Context** &gt; **Input Record - interaction** &gt; **Short Description**.

    16. In the Fields list, select **Caller**.

    17. Dot-walk to the Interaction record's **Opened for** field by selecting **Context** &gt; **Input Record - interaction** &gt; **Opened for**.

    18. In the **Wait for user input** field, leave **No** selected.

    19. In the **Fields to show after creation** field, enter `priority`.

    20. Click **Update** to finish updating the inputs for the activity.

    The **Create incident from interaction** activity automatically maps the Assigned To and Short Description fields from the interaction record to the incident record when your process runs.

4.  Add the **Wait for assignee to update** activity to the **Communicate Work in Progress** stage.

    1.  Under the **Communicate Work in Progress** stage, click **+ Add activity**.

    2.  In the activity picker, select **Common Activities**, and then select **Wait For Condition** under Interactive.

    3.  In the activity properties panel's **Label** field, enter `Wait for assignee to update`.

    4.  In the **When to start** field, leave **Immediately** selected, and then click **Save**.

    5.  Click the **Wait for assignee to update** activity card.

    6.  In the activity properties panel, click **Configure activity**.

    7.  On the Configure your activity screen, locate the Variables section under Inputs.

    8.  Next to the **Record** field, select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker-icon.png)\).

    9.  Dot-walk to the **Create incident from interaction** activity's **record** output by selecting **Activities** &gt; **1:1 - automated\_create\_record** &gt; **Outputs** &gt; **record**.

    10. In the Table list, select **Incident \[incident\]**.

    11. Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) to add the following condition to your activity:

        **\[Updated by\]** **\[is\]** **\[Activities** &gt; **1:1 - automated\_create\_record** &gt; **Outputs** &gt; **record** &gt; **Assigned to\]**.

    12. Click **Update** to finish updating the inputs for the activity.

    The **Wait for assignee to update** activity pauses the process until the Assigned To user for the Incident record updates the record.

5.  Add the **Send update to VIP** activity to the **Communicate Work in Progress** stage.

    1.  Under the **Communicate Work in Progress** stage, select **+ Add activity**.

    2.  In the activity picker, select **Common Activities**, and then select **Instruction** under Default.

    3.  In the activity properties panel's **Label** field, enter `Send update to VIP`.

    4.  In the **When to start** field, leave **After Previous** selected, and then select **Save**.

    5.  Click the **Send update to VIP** activity card.

    6.  In the activity properties panel, select **Configure activity**.

    7.  On the Configure your activity screen, locate the Variables section under Inputs.

    8.  In the **Message** field, enter `Notify the VIP user that work on their issue is in progress`.

    9.  Leave the **Wait for user input** field's value as **Yes**.

    10. Click **Update** to finish updating the inputs for the activity.

    The **Send update to VIP** activity prompts the agent to send an email to the VIP user when the assignee for the incident record makes an update.

6.  Add the **Wait for incident resolution** activity to the **Resolve** stage.

    1.  Under the **Resolve** stage, select **+ Add activity**.

    2.  In the activity picker, select **Common Activities**, and then select **Wait For Condition** under Interactive.

    3.  In the activity properties panel's **Label** field, enter `Wait for incident resolution`.

    4.  In the **When to start** field, leave **Immediately** selected, and then click **Save**.

    5.  Click the **Wait for incident resolution** activity card.

    6.  In the activity properties panel, click **Configure activity**.

    7.  On the Configure your activity screen, locate the Variables section under Inputs.

    8.  Next to the **Record** field, select the data pill picker icon \(![Data pill picker icon](../images/data-pill-picker-icon.png)\).

    9.  Dot-walk to the **Create incident from interaction** activity's **record** output by selecting **Activities** &gt; **1:1 - automated\_create\_record** &gt; **Outputs** &gt; **record**.

    10. In the **Table** field, select **Incident \[incident\]**.

    11. Use the [condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) to add the following condition to your activity:

        **\[State\]** **\[is\]** **\[Resolved\]**.

    12. Select **Update** to finish updating the inputs for the activity.

    The **Wait for incident resolution** activity pauses the process until the Incident's state becomes **\[Resolved\]**.

7.  Add the **Share resolution details with VIP** activity to the **Resolve** stage.

    1.  Under the **Resolve** stage, select **+ Add an activity**.

    2.  In the activity picker, select **Common Activities**, and then select **Instruction** under Default.

    3.  In the activity properties panel's **Label** field, enter `Share resolution details with VIP`.

    4.  In the **When to start** field, leave **After Previous** selected, and then click **Save**.

    5.  Click the **Share resolution details with VIP** activity card.

    6.  In the activity properties panel, click **Configure activity**.

    7.  On the Configure your activity screen, locate the Variables section under Inputs.

    8.  In the **Message** field, enter `Provide the Resolution Notes from the Incident record in an email to the VIP user`.

    9.  Leave the **Wait for user input** field's value as **Yes**.

    10. Click **Update** to finish updating the inputs for the activity.

    The **Share resolution details with VIP** activity prompts the agent to send the issue resolution details to the VIP user.

8.  In the main header, click **Activate** so that your process runs when triggered.

9.  View your activated process as a playbook.

    1.  Close the Playbooks tab and navigate to **Playbook Experience**.

    2.  In the side menu, click the lists icon \(![Lists icon](../images/workspace-lists-icon.png)\).

    3.  In the **Lists** tab under Interactions, click **My Interactions**.

    4.  In the form header, click **New**.

    5.  On the form, fill in the fields:

        |Field|Action|
        |-----|------|
        |Type|Select **Chat**.|
        |Opened for|Select a VIP user.|
        |Assigned to|Select a user that can make updates to Incident records.|
        |Short description|Enter `Testing out the Handle Interactions with VIPs playbook`.|

    6.  In the form header, click **Save**.

    7.  In the Contextual side panel, click the playbook icon \(![Playbook icon](../images/workspace-playbook-icon.png)\).


## Result

Your process appears in as a playbook. Here, agents and fulfillers can get a task-oriented view of the automated business process. Agents can step through the activities that you set up to see where the record is in the overall process.

**Parent Topic:**[Getting started with Playbooks](../concept/getting-started-processes.md)

