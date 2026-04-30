---
title: Produce test messages to a Hermes topic using the Kafka client
description: Produce test messages to a Hermes topic by configuring a producer client.
locale: en-US
release: yokohama
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Produce and consume messages, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Produce test messages to a Hermes topic using the Kafka client

Produce test messages to a Hermes topic by configuring a producer client.

## Before you begin

-   Secure your Kafka topics by generating a ServiceNow® instance-signed certificate and keystore. You must provide truststore and keystore details when you configure the Hermes producer. See [Set up a secure connection to the Hermes Messaging Service](set-up-secure-connection-to-hermes.md).
-   Download and install Apache Kafka. See [Prepare your Apache Kafka client environment](prepare-kafka-client-environment.md).
-   Create a test topic to store the test messages that you produce. For details, see [Create a test topic in Hermes using the Kafka client](create-hermes-topic.md).

Role required: admin

## About this task

The following steps describe how to configure a producer client and send test messages to the Hermes Kafka cluster. Refer to these steps when you're ready to produce messages to Hermes for business or production purposes.

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

2.  Configure a producer.

    1.  Open the `producer.properties` file.

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

3.  Produce a test topic.

    1.  Navigate to the Kafka directory.

    2.  Run the following command:

        Unix:

        ```
        ./bin/kafka-console-producer.sh --topic snc.<instance_name>.<namespace>.sn_<app_id>.<topic_name> --producer.config ./config/producer.properties --bootstrap-server <instance_name>.service-now.com:4000,<instance_name>.service-now.com:4001,<instance_name>.service-now.com:4002,<instance_name>.service-now.com:4003
        ```

        Windows:

        ```
        bin\windows\kafka-console-producer.bat --topic snc.<instance_name>.<namespace>.sn_<app_id>.<topic_name> --producer.config config\producer.properties --bootstrap-server <instance_name>.service-now.com:4000,<instance_name>.service-now.com:4001,<instance_name>.service-now.com:4002,<instance_name>.service-now.com:4003
        ```

        Replace the following placeholder variables:

        -   `<instance_name>` with your instance name
        -   `<namespace>` with the namespace of the domain your Kafka topic belongs to \(optional\)
        -   `<app_id>` with the application ID
        -   `<topic_name>` with a unique test topic name
        **Note:** Each part of the topic name is case-sensitive.

    3.  Send test messages to the test topic.

        For example:

        ```
        test1
        test2
        test3
        ```


## Result

Test messages are produced to the test topic in the Hermes Kafka cluster.

## What to do next

[Consume test messages from a Hermes topic using the Kafka client](consume-messages-hermes.md)

