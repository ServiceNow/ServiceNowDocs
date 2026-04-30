---
title: Set up the Confluent Kafka REST Proxy spoke
description: Integrate Confluent Kafka REST proxy with your ServiceNow instance using basic authentication.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Confluent Kafka REST Proxy Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Confluent Kafka REST Proxy spoke

Integrate Confluent Kafka REST proxy with your ServiceNow instance using basic authentication.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Confluent Kafka REST Proxy spoke.
-   Role required: admin.

**Note:** This procedure outlines steps to set up Confluent Kafka REST Proxy spoke using basic authentication. However, based on your customisations, you can also set up the spoke using ay other HTTP authentication mechanism that is currently supported by the ServiceNow Platform.

## Procedure

1.  Create a credential record for the Confluent Kafka REST Proxy spoke.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

    2.  Click **New**.

        The system displays the message **What type of Credentials would you like to create?**.

    3.  Select **Basic Auth Credentials**.

        A blank Basic Auth Credentials form displays.

    4.  Enter these values.

        |Field|Value required|
        |-----|--------------|
        |Name|Name to uniquely identify the record. For example, enter `Kafka spoke Credentials`.|
        |User name|User name to connect to the Confluent Kafka REST Proxy API endpoint.|
        |Password|Password to connect to the Confluent Kafka REST Proxy API endpoint.|
        |Active|Option to actively use the record.|
        |Order|Order to apply this credential. For example, enter `100`.|

    5.  Click **Submit**.

2.  Create a connection record for the Confluent Kafka REST Proxy spoke.

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

    2.  Open for the record, **Kafka REST** .

    3.  From the **Connections** tab, click **New**.

        The system displays a blank HTTP\(s\) Connection form.

    4.  Enter these values.

        |Field|Value required|
        |-----|--------------|
        |Name|Name to uniquely identify the connection record. For example, enter `Kafka spoke Connection`.|
        |Credential|Credential record you created for the Confluent Kafka REST Proxy spoke. For example, select **Kafka spoke Credentials**.|
        |Connection URL|URL to connect to the Confluent Kafka REST Proxy API.|

    5.  Click **Submit**.


