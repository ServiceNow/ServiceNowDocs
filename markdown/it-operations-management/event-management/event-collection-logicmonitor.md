---
title: Event collection from Logicmonitor
description: The MID WebService Event Collector enables you to collect JSON formatted event messages from the Logicmonitor.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event collection from Logicmonitor

The MID WebService Event Collector enables you to collect JSON formatted event messages from the Logicmonitor.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Ensure that you:

-   Deploy and start the MID Server. See [MID Server configuration](https://www.servicenow.com/docs/access?context=c_MIDServerConfiguration&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) .
-   Configure and start the MID Web Server. See [Configure the MID Web Server extension](configure-mid-web-server-extension.md).
-   Configure and start the MID WebService Event Collector. See [Configure the MID WebService Event Collector Context](configure-em-context-extension.md).

Role required: evt\_mgmt\_admin

## About this task

JSON formatted event messages are sent from Logicmonitor. The MID Server transforms the collected event messages by parsing them using the TransformEvents\_MidLogicmonitor script include, located here: **Event Management** &gt; **Integrations** &gt; **PushConnectors**. In the Push Connectors page, click **Logicmonitor Mid Push Connector**.

The default format of the URL to push event messages from Logicmonitor to the MID Server is `http://<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=TransformEvents_MidLogicmonitor`.

|Variable|Description|
|--------|-----------|
|MID\_Server\_IP|IP address of the MID Web Server Extension.|
|MID\_Web\_Server\_Port|Listening port of the MID Web Server Extension.|
|MID\_Web\_Server\_User|Username for the MID Web Server Extension.|
|MID\_Web\_Server\_Password|Password of the user of the MID Web Server.|

## Procedure

1.  In the Logicmonitor console, create a custom HTTP Delivery integration.

    1.  Navigate to **Settings** &gt; **Integrations** and click **Add** &gt; **Custom HTTP Delivery Integration**.

    2.  In the Manage Custom HTTP Delivery Integration form, fill in the **Name** and **Description** field and select the **Use the same URL and data to notify on various alert activity** check box.

    3.  Specify when to send a notification on alert activities by selecting the **Acknowledged**, **Cleared**, and **Escalated/De-escalated** check boxes as needed.

    4.  In the HTTP method menu, select **HTTP POST**.

    5.  Fill in the **Username** and **Password** field, and enter a URL with the format as, `http://<MID_Server_IP>:<MID_Web_Server_Port>/api/mid/em/inbound_event?Transform=TransformEvents_MidLogicmonitor`.

    6.  Under the Alert Data section, select **Raw** and select the format as **JSON**.

    7.  Add the custom payload provided in the description of the connector.

    8.  Click **Test Alert Delivery** to verify the connection or **Save**.

2.  When you're finished creating the integration, create an escalation chain for the alert settings.

    1.  Navigate to **Settings** &gt; **Alert Settings** &gt; **Escalation Chains** and click **Add**.

    2.  In the Manage Testing chain form, fill in the **Name** and **Description** field and select the rate at which the alerts should be notified.

    3.  Under the Stages section, select the Add icon ![logicmonitor add icon](../image/logicmonitor-add-icon.png) to add a stage and click **Save**.

    4.  When you create the new stage, select the Add icon ![logicmonitor add icon](../image/logicmonitor-add-icon.png) again to search for the user and add the integration as the Contact Method and click **Save**.

3.  After creating the escalation chain, configure alert rules for the chain you created.

    1.  Navigate to **Settings** &gt; **Alert Settings** &gt; **Alert Rules**, and click **Add**.

    2.  On the Add Alert window, configure the conditions that initiates the alerts when conditions are violated.

    3.  Under the Escalation chain menu, select the escalation chain you created.

    4.  Click **Save**.

    **Note:** To map the CI to the **cmdb\_ci\_vm\_object** record instead of the **cmdb\_ci\_server**, enable the event rule created for Logicmonitor. The Logicmonitor's collector name, which comes in as a hostname in the payload, should be the same as the object\_id of the virtual machine discovered in the **cmdb\_ci\_vm\_object** record.


**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

