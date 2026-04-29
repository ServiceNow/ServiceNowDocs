---
title: Create a test topic in Hermes using the Kafka client
description: Create a topic for sending and receiving test messages in the Hermes Kafka cluster.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Produce and consume messages, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a test topic in Hermes using the Kafka client

Create a topic for sending and receiving test messages in the Hermes Kafka cluster.

## Before you begin

-   Secure your Kafka topics by generating a ServiceNow® instance-signed certificate and keystore. You must provide truststore and keystore details when you configure a producer to create a topic in Hermes. See [Set up a secure connection to the Hermes Messaging Service](set-up-secure-connection-to-hermes.md).
-   Download and install Apache Kafka. See [Prepare your Apache Kafka client environment](prepare-kafka-client-environment.md).

Role required: admin

## About this task

The full Hermes Kafka topic name is composed of the following elements:

```
snc.<instance_name>.<namespace>.<app_id>.<topic_name>
```

where:

-   `<instance_name>` is the name of your instance
-   `<namespace>` is the namespace of the domain your Kafka topic belongs to \(optional\)
-   `<app_id>` is your application ID

    The topic you create belongs to this application. Specify either of the following:

    -   `sn_logstoanalytics` for Log Export Service topics
    -   `sn_streamconnect` for Stream Connect topics
-   `<topic_name>` is the unique name for your topic

**Note:** The full topic name is case-sensitive and limited to 200 characters.

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

3.  Navigate to your Kafka directory.

4.  Create a test topic by running the following command:

    -   Unix:

        ```
        ./bin/kafka-topics.sh --create --topic snc.<instance_name>.<namespace>.sn_<app_id>.<topic_name> --command-config ./config/producer.properties --bootstrap-server <instance_name>.service-now.com:4000,<instance_name>.service-now.com:4001,<instance_name>.service-now.com:4002,<instance_name>.service-now.com:4003
        ```

    -   Windows:

        ```
        bin\windows\kafka-topics.bat --create --topic snc.<instance_name>.<namespace>.sn_<app_id>.<topic_name> --command-config config\producer.properties --bootstrap-server <instance_name>.service-now.com:4000,<instance_name>.service-now.com:4001,<instance_name>.service-now.com:4002,<instance_name>.service-now.com:4003
        ```

    Replace the following placeholder variables:

    -   `<instance_name>` with your instance name \(case-sensitive\)
    -   `<namespace>` with the namespace of the domain your Kafka topic belongs to \(optional\)
    -   `<app_id>` with the application ID \(case-sensitive\)
    -   `<topic_name>` with the unique topic name you want to use \(case-sensitive\)

## Result

A test topic is created in the Hermes Kafka cluster.

## What to do next

[Produce test messages to a Hermes topic using the Kafka client](produce-messages-hermes.md)

