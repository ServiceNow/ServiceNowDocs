---
title: Create Kafka credentials
description: Configure credentials for your Apache Kafka connection.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Message replication, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Create Kafka credentials

Configure credentials for your Apache Kafka connection.

## Before you begin

Role required: connection\_admin or message\_replication\_admin

## About this task

Configure connection and credential records for connecting to your local Apache Kafka environment.

-   The connection record contains the information required for making the connection to your local Kafka. Connection records are stored in the Kafka Connections \[kafka\_connection\] table.
-   The credential record stores the authentication data required for the connection. Credential records are stored in the Kafka credentials \[kafka\_credentials\] table.

After you've created both the connection record and the credential record, you can [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md), which links your connection information and the credential data under a single name.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

3.  On the form asking what type of credentials you would like to create, select **Kafka credentials**.

4.  On the Kafka credentials form, fill in the fields.

    For a description of the fields, see [Kafka credentials fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/health-log-analytics/hla-data-input-kafka-credentials.md).

5.  Select **Submit**.


## What to do next

[Configure a Kafka connection](configure-kafka-connection.md).

**Parent Topic:**[Stream Connect Message Replication](../concept/stream-connect-message-replication.md)

