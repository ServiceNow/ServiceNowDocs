---
title: Set up Twilio spoke
description: Integrate the ServiceNow instance and Twilio using basic authentication to authenticate ServiceNow requests.Add and configure Twilio Base, Twilio Messaging, and Twilio Notify connections to authenticate ServiceNow requests in Twilio spoke.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Twilio Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Twilio spoke

Integrate the ServiceNow instance and Twilio using basic authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Twilio spoke.
-   Role required: admin.

## Configure connection for Twilio spoke

Add and configure Twilio Base, Twilio Messaging, and Twilio Notify connections to authenticate ServiceNow requests in Twilio spoke.

### Before you begin

Role required: admin

### Procedure

1.  Configure the **Twilio\_Base** connection alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Integrations** tab.

    3.  Under **Connections**, toggle and enable the **Outbound** connections.

    4.  Locate the alias for **Twilio\_Base** and click **View Details**.

        -   To configure the default connection and credential alias record that is shipped along with the Twilio spoke, click **View Details**.

            ![Connection template for Twilio Base](../image/twilio-base-conn.png)

        -   To manage more than one Twilio Base spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
        If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

        ![Twilio Base connection configuration](../image/twilio-base-conn-config.png)

    5.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Name to uniquely identify the connection record. For example, enter `Twilio_Base`.|
        |Connection URL|Connection URL for Twilio Base. This field is automatically set to `https://api.twilio.com`.|
        |Account SID|Account String Identifier \(SID\) of Twilio Base.|
        |Page Size|Page size for data stream of Twilio Base.|
        |Credential Name|Name to uniquely identify the Twilio Base credential record. For example, `Twilio Base Spoke Credential`.|
        |User name|Account String Identifier \(SID\) of Twilio Base.|
        |Password|Auth Token of the Twilio account.|

        ![](../image/twilio-base-conf-temp.png)

    6.  Click **Configure Connection**.

2.  Configure the **Twilio\_Messaging** connection alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Integrations** tab.

    3.  Under **Connections**, toggle and enable the **Outbound** connections.

    4.  Locate the alias for **Twilio\_Messaging** and click **View Details**.

        -   To configure the default connection and credential alias record that is shipped along with the Twilio spoke, click **View Details**.

            ![Connection template for Twilio Messaging](../image/twilio-messg-conn.png)

        -   To manage more than one Twilio Messaging spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
        If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

        ![Twilio Messaging Connection configuration](../image/twilio-messg-conn-config.png)

    5.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Name to uniquely identify the connection record. For example, enter `Twilio_Messaging`.|
        |Connection URL|Connection URL for Twilio Messaging. This field is automatically set to `https://messaging.twilio.com`.|
        |Account SID|Account String Identifier \(SID\) of Twilio Messaging.|
        |Page Size|Page size for data stream of Twilio Messaging.|
        |Credential Name|Name to uniquely identify the Twilio Messaging credential record. For example, `Twilio Messaging Spoke Credential`.|
        |User name|Account String Identifier \(SID\) of the Twilio Messaging account.|
        |Password|Auth token of the Twilio account.|

        ![](../image/twilio-messaging-conf-temp.png)

    6.  Click **Configure Connection**.

3.  Configure the **Twilio\_Notify** connection alias.

    1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

    2.  Click the **Integrations** tab.

    3.  Under **Connections**, toggle and enable the **Outbound** connections.

    4.  Locate the alias for **Twilio\_Notify** and click **View Details**.

        -   To configure the default connection and credential alias record that is shipped along with the Twilio spoke, click **View Details**.

            ![Connection template for Twilio Notify](../image/twilio-notify-conn.png)

        -   To manage more than one Twilio Notify spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
        If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

        ![Twilio Notify connection configuration](../image/twilio-notify-conn-config.png)

    5.  On the **Connection** form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Connection Name|Name to uniquely identify the connection record. For example, enter `Twilio_Notify`.|
        |Connection URL|Connection URL for Twilio Notify. This field is automatically set to `https://notify.twilio.com`.|
        |Account SID|Account String Identifier \(SID\) of Twilio Notify.|
        |Page Size|Page size for data stream of Twilio Notify.|
        |Credential Name|Name to uniquely identify the Twilio Notify credential record. For example, `Twilio Notify Spoke Credential`.|
        |User name|Account String Identifier \(SID\) of the Twilio Notify account.|
        |Password|Auth token of the Twilio account.|

        ![](../image/twilio-notify-conf-temp.png)

    6.  Click **Configure Connection**.


### Result

The spoke connection is configured and ready to be used.

