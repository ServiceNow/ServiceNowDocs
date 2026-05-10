---
title: Configure the Kafka metrics connector instance
description: Configure the Kafka metric consumer connector instance to read message send to Kafka server over topic.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the Kafka metrics connector instance

Configure the Kafka metric consumer connector instance to read message send to Kafka server over topic.

## Before you begin

To activate metric collection, ensure that the MID Server that retrieves metrics is configured with the Metric Intelligence extension and that the extension is in **Started** mode. See [Manually configure the Metric Intelligence extension](configure-itoa-metric-extension.md).

-   For PLAINTEXT in the Credential field, create a Basic authentication credential.

    Select the Search icon \(![search icon](../image/search-icon.png)\) next to the Credential field.

-   ServiceNow does not support discovery for Kafka. Therefore, create the CI entry manually in the respective table.

Role required: evt\_mgmt\_admin

## Procedure

1.  On the Credentials screen, select **New**.

2.  From the list of available credentials, select **Basic Auth Credentials**.

3.  On the Basic Authentication screen, give information for PLAINTEXT authentication, which doesn’t require credentials.

    For PLAINTEXT authentication, in the **Name** field, type any value and leave the **User Name** and **Password** fields empty.

4.  Select **Submit**.

5.  For a SASL\_PLAINTEXT, SSL, or SASL\_SSL authentication credential, in the Credential field, create a Kafka SSL credential.

    1.  Select the Search icon \(![search icon](../image/search-icon.png)\) next to the Credential field.
    2.  On the Credentials screen, select **New**.
    3.  From the list of available credentials, select **Kafka SSL Credentials**.

        For the Kafka SSL credentials fields descriptions, see [Kafka SSL credentials fields](../../health-log-analytics-admin/reference/hla-data-input-kafka-credentials.md).

        **Note:** If you clear the **Disable hostname verification** field, then in the **Additional Kafka consumer properties** field, enter the value of the **ssl.endpoint.identification.algorithm** parameter the same as of the Kafka server parameter value. For example:

        ```
        ssl.enabled.protocols=TLSv1.2,TLSv1.1,TLSv1;
        sasl.jaas.config=org.apache.kafka.common.security.plain.PlainLoginModule required username=<username> password=<password>;
        sasl.enabled.mechanisms=PLAIN;ssl.endpoint.identification.algorithm=;
        ```


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

