---
title: Use the ETL and Transform Map consumers to import data
description: Use ETL definitions and transform maps to process Kafka events. ETL definitions and transform maps specify the transformation logic to use when pulling data through scheduled imports. You can use the same ETL definitions and transform maps to transform the events received through Kafka.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Stream Connect quick start guide, Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Use the ETL and Transform Map consumers to import data

Use ETL definitions and transform maps to process Kafka events. ETL definitions and transform maps specify the transformation logic to use when pulling data through scheduled imports. You can use the same ETL definitions and transform maps to transform the events received through Kafka.

## Before you begin

-   Role required: integration\_hub\_admin
-   This page is part of the [Stream Connect quick start guide](../concept/stream-connect-quick-start.md).
-   This document shows you how to consume messages through your connection to Hermes. To set up and test your connection, see [Set up a secure connection to the Hermes Messaging Service](https://www.servicenow.com/docs/access?context=set-up-secure-connection-to-hermes&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) and [Testing the connection to Hermes through the ADCv2 gateway](test-connection-hermes.md).
-   The first part of this page shows you how to use the ETL Consumer to consume messages. To use the ETL consumer, you need a [robust import set transformer](../../import-sets/concept/robust-import-set-transformers.md).
-   The second part of this page shows you how to use a Transform Map consumer to consume messages. To use the Transform Map Consumer, you need a [transform map](../../../script/server-scripting/concept/c_CreatingNewTransformMaps.md).

## Procedure

1.  Create a topic to consume ETL and transform map consumer messages.

    1.  Use the following command to create a topic in Hermes.

        In this example, the topic name is topic2.

        ```
        bin/kafka-topics.sh --create --command-config config/bootcamp.properties  --bootstrap-server <instance name>.service-now.com:4000,<instance name>.service-now.com:4001,<instance name>.service-now.com:4002, <instance name>.service-now.com:4003 --topic snc.<instance name>.topic2
        ```

        Be sure to replace `<instance name>` with the name of your instance.

    2.  To view the topic, log in to the instance and navigate to **All** &gt; **IntegrationHub** &gt; **Stream Connect** &gt; **Topics**.

        **Note:** It takes approximately 10 minutes to create a topic.

2.  Create an ETL Consumer to consume data from the topic.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Consumers** &gt; **ETL Consumer**.

    2.  Select **New**.

    3.  On the Kafka Consumer form, enter a name in the **Name** field.

        This example uses the name Member Import.

    4.  For the **Robust import set transformer** filed, select an existing Robust import set transformer.

        For the robust import set transformer, select one that is not using the option to store data in a single column. To be able to see the messages, make sure the robust import set transformer has the **Verbose** option enabled.

    5.  Deselect the **Data in single column** option.

        This option should only be selected for import set tables with data in a single column.

    6.  Set the **Column mapping** to **Label**.

        This means the input message's JSON keys are mapped to the column labels of the Import Set table.

        ![The Kafka ETL Consumer form.](../images/kafka-consumer-example.png)

    7.  Save the form.

    8.  [Create a Kafka stream](create-kafka-stream.md) for the consumer.

    9.  On the Kafka Stream form, set the following field values.

        -   **Name** to `Topic2 Stream`.
        -   **Topic** to the topic created earlier, topic2.
        -   **Max concurrency** to `1`.
        -   **Start Consuming** to **Messages received after the first activation**.
        -   **Message handling** to **Automatically optimize**.
    10. Select the **Activate** link under Related Links.

        You should be able to see the activated subscription.

        ![Example Kafka Stream form for topic2.](../images/kafka-stream-topic2.png)

3.  Publish messages to topic2.

    1.  Run the following command to publish messages to topic2.

        ```
        bin/kafka-console-producer.sh --topic snc.<instance name>.topic2  --producer.config  config/bootcamp.properties  --bootstrap-server <instance name>.service-now.com:4000,<instance name>.service-now.com:4001,<instance name>.service-now.com:4002,<instance name>.service-now.com:4003
        ```

        Be sure to replace `<instance name>` with the name of your instance.

        This command prompts you for messages.

    2.  Send the following JSON message.

        ```
        {"city":"San Diego","name":"Jhon","id":"SN001","state":"California"}
        ```

        You can send this message with any values, but the JSON message key should match the Import Set table labels.

    3.  Navigate back to the ETL Consumer you created.

        After about one minute, the data should have been imported through the import set.

        ![The Kafka Consumer form with the Import sets tab filled in.](../images/kafka-consumer-import.png)

    4.  To view detailed information about the import set, select the import set number.

        ![Detailed view of the import set.](../images/kafka-import-set.png)

    5.  To view detailed information about an import set row, select the import set row number.

        ![Detailed view of the import set row](../images/kafka-import-row.png)

4.  Create a Transform Map Consumer to consume data.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Consumers** &gt; **Transform Map Consumer**.

    2.  Select **New**.

    3.  On the Kafka Transform Map Consumer form, enter a name in the **Name** field.

    4.  For the **Transform Map** field, select an existing transform map.

        ![The Transform Map Consumer form.](../images/transform-map-consumer.png)

    5.  Save the form.

    6.  [Create a Kafka stream](create-kafka-stream.md) for the consumer.

    7.  On the Kafka Stream form, set the following field values.

        -   **Name** to `Transform Map Stream`.
        -   **Topic** to the topic created earlier, topic2.
        -   **Max concurrency** to `1`.
        -   **Start Consuming** to **Messages received after the first activation**.
        -   **Message handling** to **Automatically optimize**.
    8.  Select the **Activate** link under Related Links.

        You should be able to see the activated subscription.

        ![Kafka Stream form for the Transform Map Consumer with subscription information.](../images/transform-map-stream.png)

5.  Publish messages to topic2.

    1.  Run the following command to publish messages to topic2.

        ```
        bin/kafka-console-producer.sh --topic snc.<instance name>.topic2  --producer.config  config/bootcamp.properties  --bootstrap-server <instance name>.service-now.com:4000,<instance name>.service-now.com:4001,<instance name>.service-now.com:4002,<instance name>.service-now.com:4003
        ```

        Be sure to replace `<instance name>` with the name of your instance.

        This command prompts you for messages.

    2.  Send the following JSON message.

        ```
        {"city":"San Diego","name":"Jhon","id":"SN001","state":"California"}
        ```

        You can send this message with any values, but the JSON message key should match the Import Set table labels.

    3.  Go to the Transform Map Consumer you created.

        After about one minute, the data should have been imported through the import set.

    4.  To view detailed information about the import set, select the import set number as in step 3d above.


## What to do next

[Use the Kafka Producer step and the ProducerV2 API to publish messages](publish-messages-instance-hermes.md).

