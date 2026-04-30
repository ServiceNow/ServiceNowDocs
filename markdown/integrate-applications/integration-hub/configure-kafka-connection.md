---
title: Configure a Kafka connection
description: Configure a connection to your Apache Kafka environment.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Stream Connect Message Replication, Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Configure a Kafka connection

Configure a connection to your Apache Kafka environment.

## Before you begin

-   Role required: connection\_admin or message\_replication\_admin
-   [Create Kafka SSL credentials](create-kafka-ssl-credentials.md).

## About this task

Configure connection and credential records for connecting to your local Apache Kafka environment.

-   The connection record contains the information required for making the connection to your local Kafka. Connection records are stored in the Kafka Connections \[kafka\_connection\] table.
-   The credential record stores the authentication data required for the connection. Credential records are stored in the Kafka SSL credentials \[kafka\_ssl\_credentials\] table.

After you've created both the connection record and the credential record, you can [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), which links your connection information and the credential data under a single name.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connections**.

2.  Select **New**.

3.  On the form asking what type of connection you would like to create, select **Kafka Connection**.

4.  On the Kafka Connection form, fill in the fields.

    | | |
    |---|---|
    |Name|Name for the connection.|
    |Credential|Name of the credential used to authorize this connection.|
    |Application|Application scope for the message replication. This field is automatically set.|
    |Active|Option to activate the connection.|
    |Connection alias|Name of the connection alias to associate with this connection.|
    |Bootstrap servers|Comma-separated list in the format HOST:PORT,HOST:PORT. The list doesn't need to include all of the Apache Kafka cluster servers.|
    |Consumer group id|Kafka consumer group.id. If not provided, the value is created with the format `{instance_name}-consumer-{kafka_connection.sys_id}`|
    |Additional client properties|Any additional client properties that should be specified when connecting to Kafka. For a full list and description of the available properties, see the Kafka documentation at [https://kafka.apache.org/documentation/](https://kafka.apache.org/documentation/).|
    |Use MID Server|Option to use a MID Server. This field is automatically selected.|
    |Advanced MID Server Configuration|
    |MID Selection|Option to select the specific MID Server or MID Cluster. This field is automatically set to **Specific MID Server**.|
    |MID Server|Name of the MID Server to use.|

5.  Select **Submit**.


## What to do next

[Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) with a **Connection type** of **Kafka**.

**Parent Topic:**[Stream Connect Message Replication](../concept/stream-connect-message-replication.md)

