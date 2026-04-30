---
title: Integrate ServiceNow Cloud Observability Events
description: Integrate ServiceNow Cloud Observability with Event Management by adding a standard webhook in the ServiceNow Cloud Observability platform. Download the Event Management Connector plugin from the ServiceNow Store so you can integrate with ServiceNow Cloud Observability.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate ServiceNow Cloud Observability Events

Integrate ServiceNow Cloud Observability with Event Management by adding a standard webhook in the ServiceNow Cloud Observability platform. Download the Event Management Connector plugin from the ServiceNow Store so you can integrate with ServiceNow Cloud Observability.

## Before you begin

-   Role required: evt\_mgmt\_integration

## About this task

Authenticate ServiceNow Cloud Observability as a data source to enable Event Management to collect events from ServiceNow Cloud Observability. In your ServiceNow Cloud Observability platform, use a standard webhook to set your ServiceNow AI Platform instance as the rest endpoint.

**Note:** Ensure the evt\_mgmt\_integration role is assigned to the selected user. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

## Procedure

1.  Create a CI.

    **Note:** Discovery for ServiceNow Cloud Observability services isn’t supported. Create a CI manually in a Service Instance \(cmdb\_ci\_service\_auto\) table to enable binding.

    1.  Navigate to **All** &gt; **Configuration** &gt; **Application Service**.

    2.  Select **New**.

    3.  In the form, enter the name.

        The name must be the service name provided in the ServiceNow Cloud Observability platform.

    4.  From the Operational Status list, set the operational status to **Operational**.

    5.  Select **Next**.

    6.  Select **Done**.

2.  In your ServiceNow Cloud Observability platform, create a notification destination.

    1.  From the navigation bar, select **Alerts**.

    2.  Select the **Notification destinations** tab.

    3.  Select **Create a destination**.

    4.  Select **ServiceNow** or **webhook**.

        Use the ServiceNow destination to connect only with the ServiceNow platform. If you have any issues with the ServiceNow destination, then use the **webhook** destination option.

        ![Choose ServiceNow](../image/choose-webhook.png)

3.  In your ServiceNow Cloud Observability platform, create a ServiceNow notification destination.

    1.  In the **Name** field, enter a name for the ServiceNow destination.

    2.  In the **URL** field, provide the ServiceNow instance URL.

        This is the default format of the URL to push events from ServiceNow Cloud Observability to the ServiceNow AI Platform instance. Use this format: `https//<instance-name>.servicenow.com/api/sn_em_connector/em/inbound_event?source=lightstep`

    3.  In the **Username** field, enter your ServiceNow user name.

    4.  In the **Password** field, enter your ServiceNow user password.

        ![ServiceNow Cloud Observability ServiceNow Destination](../image/lightstep-servicenow-destination.png "Create a ServiceNow destination")

        **Note:** In a ServiceNow instance, CI binding occurs only if the name of the service in the ServiceNow Cloud Observability platform value matches the name fields of the CI you created in the **cmdb\_ci\_service\_auto** table.

    5.  Select **Save**.

4.  **Note:** If you have any issues with the ServiceNow destination in the previous step, then use the **webhook** destination option.

    In your ServiceNow Cloud Observability platform, create a **webhook** notification destination.

    1.  In the **Name** field, enter a name for the webhook destination.

    2.  In the **URL** field, provide the webhook URL.

        This is the default format of the URL to push events from ServiceNow Cloud Observability to the ServiceNow AI Platform instance. Use this format: `https//&lt;username>:&lt;password>@&lt;instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=lightstep`

    3.  Select **Payload Template**.

    4.  Select the **ServiceNow Event Management** option.

        ![ServiceNow event management template](../image/lightstep-webhook-destination-payload-template.png)

        **Note:** In a ServiceNow instance, CI binding occurs only if the name of the service in the ServiceNow Cloud Observability platform value matches the name fields of the CI you created in the **cmdb\_ci\_service\_auto** table.

    5.  If you selected the **Default Template** option in the previous substep, then select **New Header** and in the **Headers** field, enter the **service-name** and define its **value**.

        **Note:** In a ServiceNow instance, CI binding occurs only if the **service-name** header value matches the name fields of the CI you created in the **cmdb\_ci\_service\_auto table**.

        ![Create a Webhook](../image/create-webhook.png "Create a Webhook")

    6.  Select **Create**.

5.  In the ServiceNow Cloud Observability platform, configure an alert.

    1.  From the navigation bar, select **Alerts**.

    2.  Select **Create an Alert** and enter an alert name.

    3.  In the Alert Configuration area, define the threshold.

    4.  According to the destination that you created, in the **Notification Rules** area, in the **Send Notifications to** field, select your notification destination type and search for the destination name.

        ![Send notification destinations type](../image/lightstep-send-alert-notification-types.png)

    5.  Select **Save**.

        The default severity for stream-based alerts is **Critical**. You can change the default in the Push Connector Configuration area of an ServiceNow AI Platform instance. The valid severity values are:

        -   1- Critical
        -   2- Major
        -   3- Minor
        -   4- Warning
        -   5- Info

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

