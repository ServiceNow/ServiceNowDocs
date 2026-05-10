---
title: Configure a Kafka connection
description: Configure a connection to your Apache Kafka environment.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Message replication, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Configure a Kafka connection

Configure a connection to your Apache Kafka environment.

## Before you begin

-   Role required: connection\_admin or message\_replication\_admin
-   [Create Kafka credentials](create-kafka-ssl-credentials.md).

## About this task

Configure connection and credential records for connecting to your local Apache Kafka environment.

-   The connection record contains the information required for making the connection to your local Kafka. Connection records are stored in the Kafka Connections \[kafka\_connection\] table.
-   The credential record stores the authentication data required for the connection. Credential records are stored in the Kafka credentials \[kafka\_credentials\] table.

After you've created both the connection record and the credential record, you can [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md), which links your connection information and the credential data under a single name.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connections**.

2.  Select **New**.

3.  On the form asking what type of connection you would like to create, select **Kafka Connection**.

4.  On the Kafka Connection form, fill in the fields.

<table id="table_pqn_ngv_pzb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the connection.

</td></tr><tr><td>

Credential

</td><td>

Name of the credential used to authorize this connection.

</td></tr><tr><td>

Application

</td><td>

Application scope for the message replication. This field is automatically set.

</td></tr><tr><td>

Active

</td><td>

Option to activate the connection.

</td></tr><tr><td>

Connection alias

</td><td>

Name of the connection alias to associate with this connection.

</td></tr><tr><td>

Bootstrap servers

</td><td>

Comma-separated list in the format HOST:PORT,HOST:PORT. The list doesn't need to include all of the Apache Kafka cluster servers.

</td></tr><tr><td>

Consumer group id

</td><td>

Kafka consumer group.id. If not provided, the value is created with the format `{instance_name}-consumer-{kafka_connection.sys_id}`

</td></tr><tr><td>

Additional client properties

</td><td>

Any additional client properties that should be specified when connecting to Kafka. For a full list and description of the available properties, see the Kafka documentation at [https://kafka.apache.org/documentation/](https://kafka.apache.org/documentation/).

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use a MID Server. This field is automatically selected.

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Advanced MID Server Configuration

</td></tr><tr><td>

MID Selection

</td><td>

Option to select a specific MID Server or MID Cluster. Options are:-   **Specific MID Server**
-   **Specific MID Cluster**


</td></tr><tr><td>

MID Server or MID Cluster

</td><td>

Name of the MID Server or MID Cluster to use.

</td></tr></tbody>
</table>5.  Select **Submit**.


## What to do next

[Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md) with a **Connection type** of **Kafka**.

**Parent Topic:**[Stream Connect Message Replication](../concept/stream-connect-message-replication.md)

