---
title: Create a flow with a Kafka Message trigger
description: Build a flow that processes events from a Kafka stream. Start the flow when an event is available in the specified topic.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create a flow in Workflow Studio, Building flows, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a flow with a Kafka Message trigger

Build a flow that processes events from a Kafka stream. Start the flow when an event is available in the specified topic.

## Before you begin

Role required: flow\_designer or admin

This trigger requires a Stream Connect subscription. For more information, see [https://www.servicenow.com/products/automation-engine.html](https://www.servicenow.com/products/automation-engine.html).

This trigger requires the ServiceNow Stream Connect Installer \[com.glide.hub.stream\_connect.installer\] plugin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Click **New** &gt; **Flow**.

3.  Define the flow properties.

    For more information, see [Create a flow in Workflow Studio](create-flow.md).

4.  In the Trigger section, click **Add a trigger** and select **Application** &gt; **Kafka Message**.

5.  On the Kafka Message form, fill in the fields.

<table id="table_ipn_5qw_frb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Topic

</td><td>

Reference to the topic to monitor for messages.

</td></tr><tr><td>

Serialization format

</td><td>

The serialization format for the message. Select one of the following. -   **Plain Text**: Select this option for any plain-text messages. This is the default format.
-   **Encoded**: Select this option for messages in an Apache Avro format. Converting plain-text messages to an Avro format requires a schema. Select the schema registry in the **Schema registry** field. For information on schemas, see [Schema management in Stream Connect](https://www.servicenow.com/docs/access?context=schema-management&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).


</td></tr><tr><td>

Schema registry

</td><td>

Registry for the selected schema. Select one of the following.

-   **Standalone Schema Registry**
-   **Confluent Schema Registry**
 This field appears only when the **Serialization format** is set to **Encoded**.

 For the Confluent Schema Registry, if the received message's schema ID isn't in the schema table, the system imports the schema dynamically, using the configured REST connection.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced Options

</td></tr><tr><td>

Start processing from

</td><td>

Option to begin processing messages from the beginning or end of the queue, organized by date. Select one of the following. -   **The earliest message in the queue**: Begin processing from the oldest messages in the queue.
-   **The end of the queue**: Begin processing from the newest messages in the queue.


</td></tr><tr><td>

Number of messages to process per run

</td><td>

Option to specify the number of messages processed per run or let the system decide on the number of messages. Select one of the following. -   **Automatically optimize**: The system determines the number of messages to process per run.
-   **Manually override \(advanced\)**: You specify the number of messages to process per run.


</td></tr><tr><td>

Enter the number of messages \(ignored if system-generated value is lower\)

</td><td>

Number of messages to process each run. This field appears only when **Number of messages to process per run** is set to **Manually override \(advanced\)**. -   Type: integer
-   Default value: 100
-   Minimum value: 1
-   Maximum value: 100,000
 If the selected number is greater than the number calculated by the system, the flow runs with the system-calculated number.

 Depending on the size of the messages, the number of messages processed per run might be lower than the number specified.

</td></tr></tbody>
</table>6.  Click **Done**.

7.  Set the **Max concurrency** and **Relative weight** fields.

    The **Max concurrency** field determines the number of partition groups to create and the number of parallel processors to use. The **Relative weight** field enables you to allocate more processing time to the consumer relative to other consumers.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Administration** &gt; **Settings**.

    2.  In the **Flow/SubFlow/Action** field, select the info icon \(![info icon](../../integrationhub/images/info-icon.png)\) for the flow, then select **Open Record**.

    3.  Select the Additional actions icon \(![additional actions icon](../images/context-menu-icon.png)\) and select **View** &gt; **Kafka**.

        The **Max concurrency** field appears on the form.

    4.  To view the **Relative weight** field, select **Advanced**.

    5.  Set the values for **Max concurrency** and **Relative weight**.

<table id="table_bly_1lh_2xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Max concurrency

</td><td>

Maximum number of parallel processors to use to consume messages, and the number of partition groups to create.

 Default value: 1

</td></tr><tr><td>

Relative weight

</td><td>

For each cycle, the maximum amount of time allocated to the consumer for processing messages, relative to other consumers. For example, a consumer with a relative weight that's twice as high as another consumer's gets twice as much time. Consumers that have the same relative weight get the same amount of time.

The minimum value is 5. The maximum value is 2000. The default value is equal to the max concurrency multiplied by the value of the **glide.ih.kafka.consumer.max\_seconds\_per\_partition\_group** property. The **glide.ih.kafka.consumer.max\_seconds\_per\_partition\_group** property specifies the maximum time, in seconds, allocated to each partition group. Its default value is 10.

The system uses the relative weight to calculate the partition group timeout for the subscription. The partition group timeout specifies the maximum time, in milliseconds, allocated to each partition group in a specific subscription.

This field appears only when **Advanced** is selected.

</td></tr></tbody>
</table>    6.  Select **Update**.

    7.  Navigate back to your flow in Workflow Studio.

8.  Add actions, subflows, and flow logic to the flow.

9.  To test the flow, click the **Test** button.

    The **Test** button opens the Test flow dialog, where you can create a message to send to the flow. The system tests the flow with this newly created message, not with messages from the Kafka topic. The flow doesn't start receiving messages from the topic until the flow is activated. For more information, see [Test a flow](flow-test.md).

10. To activate the flow, click the **Activate** button.

    When you activate the flow, the system begins looking for messages in the topic. You must activate the flow to receive messages. For more information, see [Activate a flow](flow-activate.md).


## Result

When there's a message in the Kafka topic, the flow triggers and runs the actions.

**Parent Topic:**[Create a flow in Workflow Studio](create-flow.md)

