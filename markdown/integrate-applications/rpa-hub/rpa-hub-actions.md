---
title: RPA Hub actions and subflow
description: Two-way integration of actions and subflows in Workflow Studio and RPA Hub for a seamless robot execution.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [RPA Hub reference, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# RPA Hub actions and subflow

Two-way integration of actions and subflows in Workflow Studio and RPA Hub for a seamless robot execution.

## Flows and actions overview

The flows and actions are built using ServiceNow Workflow Studio, so make sure you’re familiar with the [Building actions in Workflow Studio](https://www.servicenow.com/docs/access?context=actions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) and [Building subflows in Workflow Studio](https://www.servicenow.com/docs/access?context=subflows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) basics.

## Invoke flows or subflow

Invoke the flow or subflow via RPA Desktop Design Studio, Unattended Robot, or Attended Robot. For more information, see the topics listed in [Flow Designer components](../../rpa-studio/concept/flow-designer-components.md).

## Enable the client callable option for a flow or subflow

Enable a client script to trigger an RPA Hub flow or subflow. For more information, see [Enable the client callable option on an RPA Hub flow or subflow](../../rpa-studio/task/enable-client-flow-rpa.md).

## RPA Hub actions

The following table shows the detailed descriptions, action inputs, and action outputs of RPA Hub actions.

<table id="table_efr_qkt_tsb"><thead><tr><th>

Action

</th><th>

Description

</th><th>

Action inputs

</th><th>

Action outputs

</th></tr></thead><tbody><tr><td>

Add WorkItem to Queue Action

</td><td>

Adds WorkItem in a specified queue in the RPA Hub application and returns the WorkItem ID.

</td><td>

-   **Queue Name**: Record
-   **Name**: String
-   **Content**: String
-   **Type**: String
-   **Priority**: String.Choice
-   **Stage**: String
-   **SLA**: Date/Time

 The maximum limit for **Content** field \(Request Content and Response Content\) is 8000 characters.

 If the **Is Work Item Name Sensitive** check box on the associated work queue form is selected, the data in the **Request Content** field is encrypted. Sensitive data with encryption is stored in the work item, so that it can be passed to the RPA Desktop Design Studio or robots.

</td><td>

-   **Action Status**: Object
-   **WorkItemID**: GUID
-   **IsNameExists**: Boolean
-   **status**: String
-   **message**: String

</td></tr><tr><td>

Assign User to Attended Automation Process Action

</td><td>

Assigns a user to the attended automation process.

</td><td>

-   **Process Name**: Record
-   **Username**: Record

</td><td>

-   **Action Status**: Object
-   **status**: String
-   **Message**: String

</td></tr><tr><td>

Assign User to Attended Robot Action

</td><td>

Assigns a user to the attended robot.

</td><td>

**Username**: Record

</td><td>

-   **Action Status**: Object
-   **status**: String
-   **Message**: String

</td></tr><tr><td>

Change Life Cycle Stage Status of a Bot Process Action

</td><td>

Changes the life cycle stage status of a bot process that is not retired.If a bot process is in **Build** life cycle stage status, if you have the required role, you can update it to **Published** state, but you cannot update it to **In Maintenance**.

If a bot process is in **Published** life cycle stage status, if you have the required role, you can update it to **In Maintenance** state, and vice versa.

</td><td>

-   **Process name**: Record
-   **Life cycle stage status**: Choice

</td><td>

-   **result**: String
-   **message**: String
-   **Action Status**: Object

</td></tr><tr><td>

Fetch Created Jobs Action

</td><td>

Fetches the process jobs in RPA Hub.

</td><td>

-   **Process Number**: String
-   **Robots**: Array\[String\]

</td><td>

-   **Action Status**: Object
-   **Result**: String
-   **Jobs**: Array\[String\]
-   **startedRobots**: Array\[String\]
-   **pendingRobots**: Array\[String\]

</td></tr><tr><td>

Fetch Execution Status Action

</td><td>

Fetches the execution status of a specific process job in RPA Hub.

</td><td>

**Process Job Number**: String

</td><td>

-   **Action Status**: Object
-   **ProcessJob**: Object
    -   **Process Name**: String
    -   **Robot Name**: String
    -   **State**: String
    -   **Started At**: Date/Time
    -   **Completed At**: Date/Time
    -   **Message**: String
-   **status**: String
-   **message**: String

</td></tr><tr><td>

Fetch Work Item Status Action

</td><td>

Fetches the status of specific work queue items, asynchronously.

</td><td>

**Work Queue Item ID**: GUID

</td><td>

-   **Action Status**: Object
    -   **Code**: Integer
    -   **Message**: String
-   **WorkItem**: Object
    -   **sysId**: String
    -   **name**: String
    -   **type**: String
    -   **priority**: String
    -   **status**: String
    -   **lockedBy**: String
    -   **additionalComments**: String
    -   **requestContent**: String
    -   **responseContent**: String
    -   **deferredTill**: Date/Time
    -   **sla**: Date/Time
    -   **created**: Date/Time
    -   **startedOn**: Date/Time
    -   **completedOn**: Date/Time
    -   **lastStartedTime**: Date/Time
-   **status**: String
-   **message**: String

</td></tr><tr><td>

Start Process Action

</td><td>

Triggers a specific bot process in RPA Hub and returns the status.

</td><td>

-   **Process Name**: Record
-   **Robots**: Array\[String\]

Ignore an entry in this field if a robot pool is assigned to the bot process.

When invoking the **Start Process** Workflow Studio action, the robots that are in the **In Maintenance** life-cycle stage status are treated as failed robots.


</td><td>

-   **Action Status**: Object
-   **Result**: String
-   **Robots**: Array\[String\]
-   **Process**: String
-   **Failed Robots**: Array\[Object\]

</td></tr><tr><td>

Stop Process Action

</td><td>

Stops a bot process. If Graceful Stop is enabled, this action gracefully stops the bot process.

</td><td>

-   **Process Name**: Record
-   **Robots**: Array\[String\]
-   **Wait For Graceful Stop**: True/False

If this check box is selected, then bot process must stop gracefully.

For more information about stopping a bot process, see [Stop an unattended bot process in RPA Hub](../task/stop-bot-process.md).

For more information about Graceful stop, see [Using Graceful Stop functionality in RPA Hub](../concept/graceful-stop-rpa.md).

For more information about Robot Pool, see [Robot pool in RPA Hub](../concept/robot-pool-rpa.md).


</td><td>

-   **Result**: String
-   **Action Status**: Object
-   **Robots**: Array\[String\]
-   **Process**: String
-   **Failed Robots**: Array\[Object\]

</td></tr><tr><td>

Unassign User from Attended Automation Process Action

</td><td>

Unassigns the user from the attended automation process.

</td><td>

-   **Process Name**: Record
-   **Username**: Record

</td><td>

-   **status**: String
-   **message**: String
-   **Action Status**: Object

</td></tr><tr><td>

Unassign User from Attended Robot Action

</td><td>

Unassigns the user from the attended robot and retires the attended robot.

</td><td>

**Username**: Record

</td><td>

-   **Action Status**: Object
-   **Status**: String
-   **Message**: String

</td></tr><tr><td>

Update Process Parameter Action

</td><td>

Updates the **Value** field for the process parameter.

</td><td>

-   **Process**: Record
-   **Parameter Name**: String
-   **Value**: String

</td><td>

-   **status**: String
-   **Action Status**: Object
-   **message**: String

</td></tr><tr><td>

Update WorkItem Action

</td><td>

Updates work queue items.

</td><td>

-   **Queue Name**: Record
-   **WorkItemID**: String
-   **Stage**: String
-   **DefferedTill**: Date/Time
-   **Name**: String
-   **Priority**: Choice
-   **Status**: Choice
-   **Request Content**: String
-   **Type**: String
-   **Remarks**: String
-   **SLA**: Date/Time
-   **Response Content**: String

 The maximum limit for **Request Content** and **Response Content** fields is 8000 characters.

 If the **Is Work Item Name Sensitive** check box on the associated work queue form is selected, the data in the **Request Content** field is encrypted. Sensitive data with encryption is stored in the work item, so that it can be passed to the RPA Desktop Design Studio or robots.

</td><td>

-   **IsNameExist**: True/False
-   **Status**: String
-   **Message**: String
-   **Action Status**: Object

</td></tr><tr><td>

Verify HashCode of a Package Version

</td><td>

Verifies the HashCode of a package version in RPA Hub to validate the HashCode of the manually uploaded automation zip file with the associated package version record.For more information about verifying the HashCode of a package version, see [Verify the HashCode of a package version in RPA Hub](../task/view-hash-code.md).

</td><td>

**Package Version**: Record

</td><td>

-   **Action Status**: Object
-   **Message**: String
-   **isAttachmentValid**: True/False

</td></tr></tbody>
</table>## RPA Hub subflow

The following table shows the detailed description, action input, and action output of RPA Hub subflow.

<table id="id_f1t_skt_tsb"><thead><tr><th>

Subflow

</th><th>

Description

</th><th>

Subflow inputs

</th><th>

Subflow outputs

</th></tr></thead><tbody><tr><td>

Import Package Version Attachment Subflow

</td><td>

Imports the package version attachments automatically for a package version. To automatically migrate the package attachment \(automation zip file\) from a lower \(non-production\) to a higher \(production\) environment.For more information about importing a package version attachment in RPA Hub, see [Import a package version attachment in RPA Hub](../task/import-attachment-package-version.md).

</td><td>

-   **Email**: Email
-   **Package Version**: Record

</td><td>

After the attachment is uploaded successfully or if an error occurs while uploading the attachment, an email notification \(if email is provided as an input\) is sent to the user who performs this import attachment action.

</td></tr><tr><td>

Start Process Subflow

</td><td>

Triggers a specific bot process in RPA Hub. Returns process job details.

</td><td>

-   **Process Name**: Record
-   **Robots**: Array\[String\]

Ignore an entry in this field if a robot pool is assigned to the bot process.

If a process job is not in the **Running** status, the robot that is associated with the process job is treated as **Failed** in the **Start Process** subflow output.


</td><td>

-   **Failed Robots**: Array\[Object\]
-   **Stopped Robots**: Array\[String\]
-   **Pending Robots**: Array\[String\]
-   **Process Jobs**: Array\[String\]
-   **Result**: String
-   **Message**: String

</td></tr><tr><td>

Stop Process Subflow

</td><td>

Triggers a specific bot process to stop in RPA Hub. Returns robots details and process job status. If Graceful Stop is enabled, this subflow gracefully stops the bot process.

</td><td>

-   **Graceful Stop**: True/False
-   **Process Name**: Record
-   **Robots**: Array\[String\]

</td><td>

-   **Failed Robots**: Array\[Object\]
-   **Stopped Robots**: Array\[String\]
-   **Pending Robots**: Array\[String\]
-   **Process Jobs**: Array\[String\]
-   **Message**: String
-   **Result**: String

</td></tr></tbody>
</table>**Parent Topic:**[RPA Hub reference](rpa-hub-reference.md)

