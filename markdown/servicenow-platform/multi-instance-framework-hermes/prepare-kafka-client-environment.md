---
title: Prepare your Apache Kafka client environment
description: Install the Apache Kafka binaries on your Unix or Windows client machine.
locale: en-US
release: zurich
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Produce and consume messages, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Prepare your Apache Kafka client environment

Install the Apache Kafka binaries on your Unix or Windows client machine.

## Before you begin

Confirm that you have Java 11.0 or higher installed by running the following command:

```
java --version
```

Role required: admin

## Procedure

1.  Download and install Apache Kafka.

    1.  Download the [Apache Kafka](https://kafka.apache.org/downloads) binaries.

        Ensure that you download the binaries, not the source code, from the Apache Kafka website.

    2.  Unzip the Apache Kafka package.

        For example:

        ```
        tar -zxvf kafka_2.13-3.2.0.tgz
        ```

2.  Navigate to the parent directory where you extracted the Apache Kafka package.

    -   For example, on Unix:

        ```
        cd /home/user/Software
        ```

    -   For example, on Windows:

        ```
        cd C:\Software
        ```

3.  Simplify the Apache Kafka directory name by renaming it to `kafka`.

    -   For example, on Unix:

        ```
        mv kafka_2.13-3.2.0 kafka
        ```

    -   For example, on Windows:

        ```
        rename kafka_2.13-3.2.0 kafka
        ```


## Result

The Apache Kafka client is installed in a simplified directory on your local machine.

## What to do next

[Create a test topic in Hermes using the Kafka client](create-hermes-topic.md)

