---
title: Use the Kafka Message trigger and Script consumer to consume messages
description: Retrieve messages from Hermes with the Kafka Message trigger in Workflow Studio and the Script consumer.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/integrate-applications/integration-hub/use-kafka-trigger-script-consumer.html
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Stream Connect quick start guide, Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Use the Kafka Message trigger and Script consumer to consume messages

Retrieve messages from Hermes with the Kafka Message trigger in Workflow Studio and the Script consumer.

## Before you begin

-   Role required: integration\_hub\_admin
-   This page is part of the [Stream Connect quick start guide](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/integration-hub/stream-connect-quick-start.md).
-   This document shows you how to consume messages through your connection to Hermes. To set up and test your connection, see  and [Testing the connection to Hermes through the ADCv2 gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/integration-hub/test-connection-hermes.md).
-   The first part of this page shows you how to use the Kafka Message trigger in Workflow Studio to consume messages. For more information about the trigger, see . For more information about Workflow Studio and configuring flows, see .
-   The second part of this page shows you how to use the Script consumer to consume messages. For more information, see [Configure a script consumer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/integration-hub/configure-script-consumer.md).

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

        \[Omitted image "select-kafka-trigger.png"\] Alt text: Kafka Message is the trigger type for the flow.

    5.  Select the Topic1 topic.

        \[Omitted image "select-kafka-topic.png"\] Alt text: Select topic1 for the Topic field.

        You can use the magnifying glass icon to see the list of available topics.

    6.  In the Actions section of the flow, navigate to **Add an Action, Flow Logic, or Subflow** &gt; **Flow Logic** &gt; **For Each**.

    7.  Drag the **Messages** data pill to the **Items** field, then select **Done**.

    8.  In the Actions section of the flow, navigate to **Add an Action, Flow Logic, or Subflow** &gt; **Action** &gt; **ServiceNow Core** &gt; **Log**.

    9.  Drag the **Payload** data pill to the **Message** field, then select **Done**.

        \[Omitted image "add-log-action.png"\] Alt text:

    10. **Save** the flow trigger.

    11. Go to the Settings \[sys\_flow\_execution\_setting\] table to enable reporting for this flow.

    12. Create a new entry and enable reporting to the flow created above.

        \[Omitted image "enable-flow-reporting.png"\] Alt text: Creating a new Setting record to enable reporting for the flow.

    13. Navigate back to your flow and select **Activate**.

    14. To view your topic subscription, navigate to **All** &gt; **Integration Hub** &gt; **Stream Connect** &gt; **Subscriptions**.

        \[Omitted image "topic1-subscription.png"\] Alt text: The subscription for the topic1 topic.

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

        \[Omitted image "kafka-flow-executions.png"\] Alt text: Select Executions to navigate to the flow execution view.

    3.  Open the flow execution.

        \[Omitted image "kafka-flow-details.png"\] Alt text: Execution details for the flow.

    4.  To view the statistics for this subscription, navigate to **All** &gt; **Integration Hub** &gt; **Stream Connect** &gt; **Subscriptions**, open the subscription, and go to the statistics view.

        \[Omitted image "kafka-flow-statistics.png"\] Alt text: The Kafka statistics for the subscription.

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

        \[Omitted image "kafka-script-example.png"\] Alt text: Kafka script consumer showing the script in the Event consumer field.

    5.  Save the form.

    6.  In the Related Links section, select **New** to add a Kafka stream to consume the messages.

    7.  On the Kafka Stream form, set the following field values.

        -   **Name** to `Topic1 Stream`.
        -   **Topic** to the topic created earlier, topic1.
        -   **Max concurrency** to `1`.
        -   **Start Consuming** to **All the messages stored in the topic**. This option enables you to read the messages already published to this topic.
        -   **Message handling** to **Automatically optimize**.
        \[Omitted image "kafka-stream-example.png"\] Alt text: The Kafka Stream record.

    8.  Select the **Activate** link under Related Links.

        You should be able to see the activated subscription.

    9.  To view the messages, navigate to **All** &gt; **System logs** &gt; **System log** and filter messages that start with Received message.

        \[Omitted image "received-messages-example.png"\] Alt text: List of the received messages.

    10. You should see all the messages after 1 minute.


## What to do next

[Use the ETL and Transform Map consumers to import data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/integrate-applications/integration-hub/use-etl-transform-map-consumers.md).

