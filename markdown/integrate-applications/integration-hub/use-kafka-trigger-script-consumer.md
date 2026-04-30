---
title: Use the Kafka Message trigger and Script consumer to consume messages
description: Retrieve messages from Hermes with the Kafka Message trigger in Workflow Studio and the Script consumer.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Stream Connect quick start guide, Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Data and Automation]
---

# Use the Kafka Message trigger and Script consumer to consume messages

Retrieve messages from Hermes with the Kafka Message trigger in Workflow Studio and the Script consumer.

## Before you begin

-   Role required: integration\_hub\_admin
-   This page is part of the [Stream Connect quick start guide](../concept/stream-connect-quick-start.md).
-   This document shows you how to consume messages through your connection to Hermes. To set up and test your connection, see [Set up a secure connection to the Hermes Messaging Service](set-up-connection-hermes.md) and [Testing the connection to Hermes through the ADCv2 gateway](test-connection-hermes.md).
-   The first part of this page shows you how to use the Kafka Message trigger in Workflow Studio to consume messages. For more information about the trigger, see [Create a flow with a Kafka Message trigger](https://www.servicenow.com/docs/access?context=create-flow-kafka&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US). For more information about Workflow Studio and configuring flows, see [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).
-   The second part of this page shows you how to use the Script consumer to consume messages. For more information, see [Configure a script consumer](configure-script-consumer.md).

## Procedure

1.  Create a topic to consume messages.

    1.  Use the following command to create a topic in Hermes.

        ```
        bin/kafka-topics.sh --create --command-config config/bootcamp.properties  --bootstrap-server <instance name>.service-now.com:4000,<instance name>.service-now.com:4001,<instance name>.service-now.com:4002, <instance name>.service-now.com:4003 --topic snc.<instance name>.topic1
        ```

        Be sure to replace `<instance name>` with the name of your instance.

    2.  To view the topic, log in to the instance and navigate to **All** &gt; **IntegrationHub** &gt; **Stream Connect** &gt; **Topics**.

        **Note:** It takes approximately 10 minutes to create a topic.

2.  Create a flow trigger to consume messages from the topic.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Select **Create new** &gt; **Flow**.

    3.  On the Flow properties form, enter a name for your flow, then enter **Submit**.

        This example uses the name `Topic1 Consumer`.

    4.  In the trigger section, select **Add a trigger**, then select **Kafka Message** as the trigger type.

        ![Kafka Message is the trigger type for the flow.](../images/select-kafka-trigger.png)

    5.  Select the Topic1 topic.

        ![Select topic1 for the Topic field.](../images/select-kafka-topic.png)

        You can use the magnifying glass icon to see the list of available topics.

    6.  In the Actions section of the flow, navigate to **Add an Action, Flow Logic, or Subflow** &gt; **Flow Logic** &gt; **For Each**.

    7.  Drag the **Messages** data pill to the **Items** field, then select **Done**.

    8.  In the Actions section of the flow, navigate to **Add an Action, Flow Logic, or Subflow** &gt; **Action** &gt; **ServiceNow Core** &gt; **Log**.

    9.  Drag the **Payload** data pill to the **Message** field, then select **Done**.

        ![Topic1 Consumer flow trigger.](../images/add-log-action.png)

    10. **Save** the flow trigger.

    11. Go to the Settings \[sys\_flow\_execution\_setting\] table to enable reporting for this flow.

    12. Create a new entry and enable reporting to the flow created above.

        ![Creating a new Setting record to enable reporting for the flow.](../images/enable-flow-reporting.png)

    13. Navigate back to your flow and select **Activate**.

    14. To view your topic subscription, navigate to **All** &gt; **Integration Hub** &gt; **Stream Connect** &gt; **Subscriptions**.

        ![The subscription for the topic1 topic.](../images/topic1-subscription.png)

3.  Publish messages to the topic using the Kafka command-line tool.

    1.  Run the following command to publish messages to the topic.

        ```
        bin/kafka-console-producer.sh --topic snc.<instance name>.topic1  --producer.config  config/bootcamp.properties  --bootstrap-server <instance name>.service-now.com:4000,<instance name>.service-now.com:4001,<instance name>.service-now.com:4002,<instance name>.service-now.com:4003
        ```

        Be sure to replace `<instance name>` with the name of your instance.

        This command prompts you for messages. Add a few sample messages. This example uses the following messages.

        -   Test message1
        -   Test message2
        -   Test message3
        You should receive the messages in about a minute.

    2.  Navigate back to the flow and select **Executions**.

        ![Select Executions to navigate to the flow execution view.](../images/kafka-flow-executions.png)

    3.  Open the flow execution.

        ![Execution details for the flow.](../images/kafka-flow-details.png)

    4.  To view the statistics for this subscription, navigate to **All** &gt; **Integration Hub** &gt; **Stream Connect** &gt; **Subscriptions**, open the subscription, and go to the statistics view.

        ![The Kafka statistics for the subscription.](../images/kafka-flow-statistics.png)

4.  Create a Script consumer to consume messages from the topic.

    1.  Navigate to **IntegrationHub** &gt; **Consumers** &gt; **Script Consumers**.

    2.  Select **New**.

    3.  In the **Name** field, enter a name for your script consumer.

        This example uses `Topic1 Consumer`.

    4.  Set the script to log the message by adding the following logic in the script box.

        ```
        for (var i = 0; i < messages.length; i++) {
              gs.info('Received message ' + JSON.stringify(messages[i].message));
         }
        
        ```

        ![Kafka script consumer showing the script in the Event consumer field.](../images/kafka-script-example.png)

    5.  Save the form.

    6.  In the Related Links section, select **New** to add a Kafka stream to consume the messages.

    7.  On the Kafka Stream form, set the following field values.

        -   **Name** to `Topic1 Stream`.
        -   **Topic** to the topic created earlier, topic1.
        -   **Max concurrency** to `1`.
        -   **Start Consuming** to **All the messages stored in the topic**. This option enables you to read the messages already published to this topic.
        -   **Message handling** to **Automatically optimize**.
        ![The Kafka Stream record.](../images/kafka-stream-example.png)

    8.  Select the **Activate** link under Related Links.

        You should be able to see the activated subscription.

    9.  To view the messages, navigate to **All** &gt; **System logs** &gt; **System log** and filter messages that start with Received message.

        ![List of the received messages.](../images/received-messages-example.png)

    10. You should see all the messages after 1 minute.


## What to do next

[Use the ETL and Transform Map consumers to import data](use-etl-transform-map-consumers.md).

