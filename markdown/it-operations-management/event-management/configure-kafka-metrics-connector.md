---
title: Configure the Kafka metrics connector instance
description: Configure the Kafka metric consumer connector instance to read message send to Kafka server over topic.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the Kafka metrics connector instance

Configure the Kafka metric consumer connector instance to read message send to Kafka server over topic.

## Before you begin

To activate metric collection, ensure that the MID Server that retrieves metrics is configured with the Metric Intelligence extension and that the extension is in **Started** mode. See [Manually configure the Metric Intelligence extension](configure-itoa-metric-extension.md).

OAuth authentication for the Kafka Metrics Connector is supported only in the Australia release and later. Ensure your instance is upgraded to Australia or a newer version before configuring OAuth.

-   Create Kafka SSL credentials on ServiceNow instance. For more information, see [Kafka SSL credentials fields](../../health-log-analytics-admin/reference/hla-data-input-kafka-credentials.md).
-   ServiceNow does not support discovery for Kafka. Therefore, create the CI entry manually in the respective table.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Select **New** and create a connector instance.

    For details on the connector instance fields displayed on the page, see [Kafka connector instance form](../reference/kafka-connector-instance-form.md).

3.  In the MID Servers for connectors section,specify a MID Server that is up and is valid.

4.  Right-click the form header and select **Save**.

5.  In the table presenting the connector instance values, verify the populated connector instance values based on your Kafka setup and the message \(JSON payload\) that you received from the Kafka topic with &lt;field\_mappings&gt; value.

6.  In the Connector Instance Values section, you can edit the values of the mandatory Kafka parameters.

    For details on the connector instance value parameters, see [Kafka connector instance value parameters](../reference/kafka-connector-instance-value-parameters.md).

7.  Right-click the form header and select **Save**.

8.  Test the connection between the MID Server and the Kafka Metric Consumer connector.

    -   Select **Test Connector**.
    -   If the test connection fails, verify whether the credential is valid, and that the network is connected from the MID Server to the Kafka broker.

        **Note:** Kafka topic name validation occurs only in Test Connector validation.

9.  After a successful test, make the connector instance active by selecting the **Active** check box.

10. Select **Update**.


**Parent Topic:**[Configure a pull connector](t_EMConfigureConnectorInstance.md)

