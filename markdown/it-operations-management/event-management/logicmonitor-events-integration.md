---
title: Integrate Logicmonitor events
description: Integrate Logicmonitor with Event Management to send events into ServiceNow by adding a webhook using Basic Authentication, it will also be available with bi-directional functionality.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate Logicmonitor events

Integrate Logicmonitor with Event Management to send events into ServiceNow by adding a webhook using Basic Authentication, it will also be available with bi-directional functionality.

## Before you begin

-   Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.
-   The Event Management plugin must be installed on the ServiceNow AI Platform instance.
-   Role required: evt\_mgmt\_integration

## About this task

Configure the Event Management environment for the collection of events from Logicmonitor. In your Logicmonitor console, set your ServiceNow AI Platform instance as the rest endpoint using a standard webhook.

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

## Procedure

1.  In the Logicmonitor console, create a custom HTTP Delivery integration.

    1.  Navigate to **Settings** &gt; **Integrations** and click **Add** &gt; **Custom HTTP Delivery Integration**.

    2.  In the Manage Custom HTTP Delivery Integration form, fill in the **Name** and **Description** field and select the **Use the same URL and data to notify on various alert activity** check box.

    3.  Specify when to send a notification on alert activities by selecting the **Acknowledged**, **Cleared**, and **Escalated/De-escalated** check boxes as needed.

        **Note:** If you are using the bi-directional Connector update, do not select the **Acknowledged** check box. Doing so can trigger a loop back to the Alert and close the Alert record unintentionally.

    4.  In the HTTP method menu, select **HTTP POST**.

    5.  Fill in the **Username** and **Password** field, and enter a URL with the format as, `https://{Instance-name}.service-now.com/api/sn_em_connector/em/inbound_event?source=logicmonitor`.

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

