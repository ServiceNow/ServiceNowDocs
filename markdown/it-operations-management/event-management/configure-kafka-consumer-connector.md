---
title: Configure the Apache Kafka Consumer connector
description: Configure the Apache Kafka Consumer connector instance to create events from streaming messages collected by the Apache Kafka connector.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Apache Kafka Consumer Connector, Configure a pull connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure the Apache Kafka Consumer connector

Configure the Apache Kafka Consumer connector instance to create events from streaming messages collected by the Apache Kafka connector.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Integrations** &gt; **Connector Instances**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_bqf_1m2_sbb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive and unique name for the Kafka Consumer connector.

</td></tr><tr><td>

Description

</td><td>

Description to be used by the Kafka Consumer event collection instance.

</td></tr><tr><td>

Connector definition

</td><td>

Name of the required connector definition, which in this case should be Kafka Consumer.

</td></tr><tr><td>

Host IP

</td><td>

The host IP.**Note:** This field must contain a value to complete the creation process so the placeholder 1.1.1.1 should be entered as a temporary value.

</td></tr><tr><td>

Event collection last run time

</td><td>

This field is automatically set to the last runtime value.

</td></tr><tr><td>

Last event collection status

</td><td>

This field is automatically set to the last runtime status.

</td></tr><tr><td>

Event collection schedule \(seconds\)

</td><td>

The frequency in seconds that the system checks for new events from the Kafka Consumer. The default value is 60 seconds.

</td></tr><tr><td>

Last error message

</td><td>

This field is automatically set to the last error message.

</td></tr></tbody>
</table>4.  For PLAINTEXT or SASL\_PLAINTEXT, in the **Credential** field, create a Basic authentication credential.

    Use the **Kafka SSL credential** type for a new Kafka pull connector instance with **SASL\_PLAINTEXT** authentication. Go to step 5.

    Use the **Kafka SSL credential** type when the Kafka server’s **sasl.enabled.mechanisms** or **sasl.mechanism** parameter's value don’t equal **PLAIN**. Go to step 5.

    1.  Select the Search icon ![Search icon](../image/search-icon.png) next to the **Credential** field.

    2.  On the Credentials screen, select **New**.

    3.  From the list of available credentials, select **Basic Auth Credentials**.

    4.  On the Basic Authentication screen, give information for either PLAINTEXT authentication, which doesn’t require credentials, or SASL\_PLAINTEXT authentication, which requires credentials.

        -   For PLAINTEXT authentication, in the **Name** field, type any value and leave the **User Name** and **Password** fields empty.
        -   For SASL\_PLAINTEXT authentication, give a name for the credential in the **Name** field, preferably prefaced by `SASL`. Provide the user name and password In the **User Name** and **Password** fields.
    5.  Select **Submit**.

5.  For a SASL\_PLAINTEXT, SSL, or SASL\_SSL authentication credential, in the **Credential** field, create a Kafka SSL credential.

    1.  Select the Search icon ![Search icon](../image/search-icon.png) next to the **Credential** field.

    2.  On the Credentials screen, select **New**.

    3.  From the list of available credentials, select **Kafka SSL Credentials**.

    4.  On the Kafka SSL Authentication screen, fill in the Kafka SSL credentials fields.

        For the Kafka SSL credentials fields descriptions, see [.](../../health-log-analytics-admin/reference/hla-data-input-kafka-credentials.md)

        **Note:** If you clear the **Disable hostname verification** field, then in the **Additional Kafka consumer properties** field, enter the value of the **ssl.endpoint.identification.algorithm** parameter the same as of the Kafka server parameter value. For example:

        ```
        ssl.enabled.protocols=TLSv1.2,TLSv1.1,TLSv1;
        sasl.jaas.config=org.apache.kafka.common.security.plain.PlainLoginModule required username=<username> password=<password>;
        sasl.enabled.mechanisms=PLAIN;ssl.endpoint.identification.algorithm=;
        ```

    5.  Select **Submit**.

6.  Right-click the form header and select **Save**.

7.  In the table presenting the connector instance values, verify the populated connector instance values based on your Kafka setup and the message \(JSON payload\) that you received from the Kafka topic.

    Change the connector instance values if necessary.

<table id="table_lnf_nkb_3vb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

authentication\_type

</td><td>

The Kafka Consumer authentication type. The currently supported values are:

 -   PLAINTEXT \(no authentication\) \(Default\)

-   SASL\_PLAINTEXT \(basic authentication – user name and password\)

</td></tr><tr><td>

bootstrap\_servers

</td><td>

The servers that establish the connection with the Kafka cluster. Values in this field should be in the form host1:port1, host2:port2, and so on \(comma-separated\).

 This field is required.

</td></tr><tr><td>

consumer\_group\_name

</td><td>

The Consumer group name.

 If the same Kafka topic is being consumed from two different instances, use different consumer group names so all events are captured for both instances.

 This field is required.

</td></tr><tr><td>

time\_of\_event\_field

</td><td>

The name of the field in the JSON payload/message that includes the time of the event.

 If a field in the JSON payload/message includes the time of the event, that value should be the value for this parameter.

 If no time field value is given, then the received time of the event in the ServiceNow instance is set as time\_of\_event.

 The time\_of\_event field should be a first-level field in the JSON payload/message. Nested field names aren’t allowed.

</td></tr><tr><td>

timezone

</td><td>

The time zone of the time\_of\_event field in the JSON payload/message.

 The timezone value isn’t used when the time\_of\_event field is empty.

 For example, if the time\_of\_event in the payload/message is in the IST time zone, the value would be GMT+0530.

 Default: GMT.

</td></tr><tr><td>

date\_format

</td><td>

The date\_time format of the time\_of\_event field in the JSON payload/message.

 If no time field value is given, then the time when the event was received in the instance in GMT time is used. The date\_time value isn’t used when the time\_of\_event field is empty.

 Default: yyyy-MM-dd HH:mm:sss.

</td></tr><tr><td>

debug

</td><td>

Displays debug messages. Default value: false. Specify true to see debug messages.

</td></tr><tr><td>

logPayloadForDebug

</td><td>

Displays payload related debug messages. Default value: false. Specify true to see payload related debug messages.

</td></tr><tr><td>

topic

</td><td>

The Kafka topic from which the messages are fetched.

 This field is required.

</td></tr></tbody>
</table>8.  In the **MID Servers for Connectors** section, specify a MID Server that is up and is valid.

    **Note:** You can configure several MID Servers. If the first server is down, the next MID Server is used. If that MID Server isn’t available, the next is selected, and so on. MID Servers are sorted according to the order that their details were entered into the **MID Servers for Connectors** section.

    If you do not specify a MID Server, an available MID Server that has a matching IP range is used.

9.  Right-click the form header and select **Save**.

10. Test the connection between the MID Server and the Kafka Consumer connector.

    1.  Select **Test Connector**.

    2.  If the test connection fails, verify whether the credential is valid, and that the network is connected from the MID Server to the Kafka broker.

        **Note:** Kafka topic name validation occurs only in **Test Connector** validation.

11. After a successful test, make the connector instance active by selecting the **Active** check box.

12. Select the **Update** button.


## What to do next

After the connector is created, you must map the fields. For more information, see [Map Kafka message payload attributes to alert fields](map-kafka-message-payload-attributes-to-alert-fields.md).

**Parent Topic:**[Apache Kafka Consumer Connector](../concept/apache-kafka-consumer-connector.md)

