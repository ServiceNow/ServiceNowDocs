---
title: Kafka Producer step
description: Create an action that publishes events to a topic in your Kafka environment.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Workflow Studio steps, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Kafka Producer step

Create an action that publishes events to a topic in your Kafka environment.

## Roles and availability

The Kafka Producer step is an Workflow Studio action step. Users with the action\_designer role can create a custom action with one or more action steps.

This step is requires a Stream Connect subscription. For more information, see [https://www.servicenow.com/products/automation-engine.html](https://www.servicenow.com/products/automation-engine.html).

This step requires the ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin.

## Fields

<table id="table_sxk_5bp_frb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Topic

</td><td>

Name of the topic to publish the message to. A topic stores messages of the same type. For example, a topic named Payments might store messages about recent payments.

 Select a topic from the drop-down list.

</td></tr><tr><td>

Message

</td><td>

Text of the message.

</td></tr><tr><td>

Key

</td><td>

Name of the key for a specific partition. Topics can be partitioned. Messages with the same key are stored in the same partition. For example, payment messages with a key of June would all be stored in the same partition of the Payments topic.

</td></tr><tr><td>

Headers

</td><td>

Headers for the message, in name-value pairs. For both the **Name** and **Value** fields, you can enter a value or use a data pill.

</td></tr><tr><td>

Wait For Completion

</td><td>

Option to require the flow to wait for the step to complete before continuing.

</td></tr><tr><td>

Schema

</td><td>

Reference to a schema table. Select a schema from the list. For information on schemas, see [Schema management in Stream Connect](https://www.servicenow.com/docs/access?context=schema-management&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).**Note:** The message you're sending in the **Message** field must adhere to the structure of the selected schema.

</td></tr><tr><td>

If this step fails

</td><td>

Option to go to error evaluation or continue running the next step. This option has no effect on the Step Status. Select one of the following. -   **Stop the action and go to error evaluation**: Stop running the action at the current step and go to error evaluation. The Step Status object contains the error information returned by the step.
-   **Don't stop the action and go to the next step**: Ignore the failure and continue running the action from the next step. The Step Status object contains the error information returned by the step. Action error evaluation runs regardless of whether the action continues running.

</td></tr></tbody>
</table>## Example

In this example, the step sends a message recording the creation of an incident. The message includes an incident identifier, a description, and a message header. The message is sent to the incidents topic, and stored in the partition with the name of the incident identifier.

![Example Kafka Producer step.](../images/kafka-producer-action-designer.png)

## Outputs

|Field|Description|Data Type|
|-----|-----------|---------|
|Step Status|Object data pill containing runtime details about the step. Each step in an action returns a Step Status.|Object|
|Step Status &gt; Code|Integer data pill indicating whether the step produced an error. By default, a value of 1 indicates that the step produced an error. A value of 0 indicates that the step ran successfully. You can't customize these codes.|Integer|
|Step Status &gt; Message|String data pill containing the error message produced by the step or system operation. You can't customize this message.|String|

**Parent Topic:**[Workflow Studio steps](../concept/steps.md)

