---
title: Consume test messages from a Hermes topic using the Kafka client
description: Consume test messages from a Hermes topic by configuring two consumer clients.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Produce and consume messages, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Consume test messages from a Hermes topic using the Kafka client

Consume test messages from a Hermes topic by configuring two consumer clients.

## Before you begin

-   Secure your Kafka topics by generating a ServiceNow® instance-signed certificate and keystore. You must provide truststore and keystore details when you configure the Hermes consumers. See [Set up a secure connection to the Hermes Messaging Service](set-up-secure-connection-to-hermes.md).
-   Download and install Apache Kafka. See [Prepare your Apache Kafka client environment](prepare-kafka-client-environment.md).
-   Create a topic and produce test messages in the Hermes Kafka cluster before you can consume messages. For details, see [Create a test topic in Hermes using the Kafka client](create-hermes-topic.md) and [Produce test messages to a Hermes topic using the Kafka client](produce-messages-hermes.md).

Role required: admin

## About this task

The following steps describe how to configure two consumer clients and receive test messages from the Hermes Kafka cluster. Because Hermes uses a pair of Kafka clusters, you must configure two consumer clients with separate consumer bootstrap addresses. This ensures messages are consumed from both clusters without dropping any messages.

**Important:** You must configure two distinct consumer bootstrap addresses, one for each consumer client.

Refer to these steps when you are ready to consume messages from Hermes for business or production purposes.

## Procedure

1.  Navigate to the `config` directory where you extracted Kafka.

    -   For example, on Unix:

        ```
        cd /home/user/Software/kafka/config
        ```

    -   For example, on Windows:

        ```
        cd C:\Software\kafka\config
        ```

2.  Configure the consumers.

    1.  Open the `consumer.properties` file.

    2.  Configure the following SSL properties:

        ```
        security.protocol=SSL
        
        ssl.truststore.password=<truststore password>
        
        ssl.truststore.location=<path to truststore.p12>
        
        ssl.truststore.type=PKCS12
        
        ssl.keystore.password=<keystore password>
        
        ssl.keystore.location=<path to keystore.p12>
        
        ssl.keystore.type=PKCS12
        
        ssl.key.password=<keystore password>
        ```

        Replace the following placeholder variables:

        -   `<truststore password>` with your truststore password
        -   `<path to truststore.p12>` with the path to your truststore file
        -   `<keystore password>` with your keystore password
        -   `<path to keystore.p12>` with the path to your keystore file
    3.  Save your changes in plain text.

3.  Consume a message using each consumer.

    1.  Run the following command for the first consumer client:

        Unix:

        ```
        ./bin/kafka-console-consumer.sh --consumer.config ./config/consumer.properties --topic snc.<instance_name>.<namespace>.sn_<app_id>.<topic_name> --group snc.<instance_name>.<consumer_group_id> --from-beginning --bootstrap-server <instance_name>.service-now.com:4100,<instance_name>.service-now.com:4101,<instance_name>.service-now.com:4102,<instance_name>.service-now.com:4103
        ```

        Windows:

        ```
        bin\windows\kafka-console-consumer.bat --consumer.config config\consumer.properties --topic snc.<instance_name>.<namespace>.sn_<app_id>.<topic_name> --group snc.<instance_name>.<consumer_group_id> --from-beginning --bootstrap-server <instance_name>.service-now.com:4100,<instance_name>.service-now.com:4101,<instance_name>.service-now.com:4102,<instance_name>.service-now.com:4103
        ```

        Replace the following placeholder variables:

        -   `<instance_name>` with your instance name
        -   `<namespace>` with the namespace of the domain your Kafka topic belongs to \(optional\)
        -   `<app_id>` with the application ID
        -   `<topic_name>` with a test topic name
        -   `<consumer_group_id>` with a label of your choice for the group that the consumer belongs to
        **Note:** Each part of the topic name is case-sensitive.

    2.  Open a new terminal window.

    3.  Navigate to the Kafka directory.

    4.  Run the following command for the second consumer client:

        Unix:

        ```
        ./bin/kafka-console-consumer.sh --consumer.config ./config/consumer.properties --topic snc.<instance_name>.<namespace>.<topic_name> --group snc.<instance_name>.<consumer_group_id> --from-beginning --bootstrap-server <instance_name>.service-now.com:4200,<instance_name>.service-now.com:4201,<instance_name>.service-now.com:4202,<instance_name>.service-now.com:4203
        ```

        Windows:

        ```
        bin\windows\kafka-console-consumer.bat --consumer.config config\consumer.properties --topic snc.<instance_name>.<namespace>.<topic_name> --group snc.<instance_name>.<consumer_group_id> --from-beginning --bootstrap-server <instance_name>.service-now.com:4200,<instance_name>.service-now.com:4201,<instance_name>.service-now.com:4202,<instance_name>.service-now.com:4203
        ```

        Replace the following placeholder variables:

        -   `<instance_name>` with your instance name
        -   `<namespace>` with the namespace of the domain your Kafka topic belongs to \(optional\)
        -   `<topic_name>` with a test topic name
        -   `<consumer_group_id>` with a label of your choice for the group that the consumer belongs to
        **Note:** Each part of the topic name is case-sensitive.


## Result

Test messages are consumed from the Hermes Kafka cluster.

