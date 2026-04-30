---
title: Use the Kafka Producer step and the ProducerV2 API to publish messages
description: Push data from ServiceNow to Hermes so that the Kafka consumers can read them.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Stream Connect quick start guide, Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Use the Kafka Producer step and the ProducerV2 API to publish messages

Push data from ServiceNow to Hermes so that the Kafka consumers can read them.

## Before you begin

-   Role required: integration\_hub\_admin
-   This page is part of the [Stream Connect quick start guide](../concept/stream-connect-quick-start.md).
-   This document shows you how to publish messages through your connection to Hermes. To set up and test your connection, see [Set up a secure connection to the Hermes Messaging Service](https://www.servicenow.com/docs/access?context=set-up-secure-connection-to-hermes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) and [Testing the connection to Hermes through the ADCv2 gateway](test-connection-hermes.md).
-   The first part of this page shows you how to use the Kafka Producer step in Workflow Studio to publish messages to Hermes. For more information about the step, see [Kafka Producer step](https://www.servicenow.com/docs/access?context=kafka-producer-action-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
-   The second part of this page shows you how to use the ProducerV2 API to publish messages. For more information, see [ProducerV2 API](https://www.servicenow.com/docs/access?context=ProducerV2ScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).
-   To receive all the messages, you need to run two consumers for different datacenters. See [Consume test messages from a Hermes topic using the Kafka client](https://www.servicenow.com/docs/access?context=consume-messages-hermes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for details.

## Procedure

1.  Start two consumers to receive messages.

    1.  Run the following commands from the command line to receive the messages.

        ```
        bin/kafka-console-consumer.sh --consumer.config config/bootcamp.properties --topic snc.<instance name>.topic1 --group snc.<instance name>.consumer_group1 --from-beginning --bootstrap-server <instance name>.service-now.com:4100,<instance name>.service-now.com:4101,<instance name>.service-now.com:4102,<instance name>.service-now.com:4103
        ```

        ```
        bin/kafka-console-consumer.sh --consumer.config config/bootcamp.properties --topic snc.<instance name>.topic1 --group snc.<instance name>.consumer_group1 --from-beginning --bootstrap-server <instance name>.service-now.com:4200, <instance name>.service-now.com:4201, <instance name>.service-now.com:4202, <instance name>.service-now.com:4203
        ```

        Be sure to replace `<instance name>` with the name of your instance.

2.  Publish messages from the instance using a flow step.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

    2.  Create a new action by selecting **Create new** &gt; **Action**.

    3.  In the Action properties form, give your action a name, then select **Submit**.

        This example uses the name Message Publisher.

    4.  Add a **Kafka Producer** step to the action.

        To add an action step, select the plus sign between the **Inputs** and **Error Evaluation** in the Action Outline.

        ![](../images/add-kafka-producer-step.png) ![Add the Kafka Producer step to the action.]()

    5.  In the step, set the **Topic** field to `topic1`.

    6.  In the **Message** field, enter a message.

        You don't need to change any other fields.

        ![Fill in the fields for the Kafka Producer step.](../images/kafka-producer-step-fields.png)

    7.  Select **Save** to save the action.

    8.  Select the **Test** button to test the action.

        Testing the action publishes the message to the topic.

    9.  To view the message, go to the command-line consoles created in step 1.

        The message should be present in one of the terminals.

3.  Publish messages from the instance using a script.

    1.  Run the following script using the scripts background to publish messages to this topic from the instance.

        ```
        var producer = new sn_ih_kafka.ProducerV2();
        producer.send('<sys id of the topic record>', gs.generateGUID(), 'Test message from ServiceNow', false, null);
        
        ```

        Be sure to replace `<sys id of the topic record>` with the sys\_id of the topic record.

    2.  To view the message, go to the command-line consoles created in step 1.

        The message should be present in one of the terminals.


