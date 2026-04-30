---
title: Create Kafka SSL credentials
description: Configure SSL credentials for your Apache Kafka connection.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Stream Connect Message Replication, Using Stream Connect for Apache Kafka, Importing and streaming data in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Create Kafka SSL credentials

Configure SSL credentials for your Apache Kafka connection.

## Before you begin

Role required: connection\_admin or message\_replication\_admin

## About this task

Configure connection and credential records for connecting to your local Apache Kafka environment.

-   The connection record contains the information required for making the connection to your local Kafka. Connection records are stored in the Kafka Connections \[kafka\_connection\] table.
-   The credential record stores the authentication data required for the connection. Credential records are stored in the Kafka SSL credentials \[kafka\_ssl\_credentials\] table.

After you've created both the connection record and the credential record, you can [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US), which links your connection information and the credential data under a single name.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

3.  On the form asking what type of credentials you would like to create, select **Kafka SSL credentials**.

4.  On the Kafka SSL credentials form, fill in the fields.

    For a description of the fields, see [Kafka SSL credentials fields](https://www.servicenow.com/docs/access?context=hla-data-input-kafka-credentials&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

5.  Select **Submit**.


## What to do next

[Configure a Kafka connection](configure-kafka-connection.md).

**Parent Topic:**[Stream Connect Message Replication](../concept/stream-connect-message-replication.md)

