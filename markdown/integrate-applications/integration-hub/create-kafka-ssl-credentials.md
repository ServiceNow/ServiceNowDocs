---
title: Create Kafka SSL credentials
description: Configure SSL credentials for your Apache Kafka connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/create-kafka-ssl-credentials.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Message replication, Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Create Kafka SSL credentials

Configure SSL credentials for your Apache Kafka connection.

## Before you begin

Role required: connection\_admin or message\_replication\_admin

## About this task

Configure connection and credential records for connecting to your local Apache Kafka environment.

-   The connection record contains the information required for making the connection to your local Kafka. Connection records are stored in the Kafka Connections \[kafka\_connection\] table.
-   The credential record stores the authentication data required for the connection. Credential records are stored in the Kafka SSL credentials \[kafka\_ssl\_credentials\] table.

After you've created both the connection record and the credential record, you can [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/connections-and-credentials/connection-alias.md), which links your connection information and the credential data under a single name.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

3.  On the form asking what type of credentials you would like to create, select **Kafka SSL credentials**.

4.  On the Kafka SSL credentials form, fill in the fields.

    For a description of the fields, see [Kafka SSL credentials fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/health-log-analytics/hla-data-input-kafka-credentials.md).

5.  Select **Submit**.


## What to do next

[Configure a Kafka connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/configure-kafka-connection.md).

**Parent Topic:**[Stream Connect Message Replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/stream-connect-message-replication.md)

