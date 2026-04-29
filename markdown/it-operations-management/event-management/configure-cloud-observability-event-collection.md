---
title: Configure ServiceNow Cloud Observability event collection
description: Integrate ServiceNow Cloud Observability with Event Management by adding a standard webhook in the ServiceNow Cloud Observability platform. Download the Event Management Connector plugin from the ServiceNow Store so you can integrate with ServiceNow Cloud Observability.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure ServiceNow Cloud Observability event collection

Integrate ServiceNow Cloud Observability with Event Management by adding a standard webhook in the ServiceNow Cloud Observability platform. Download the Event Management Connector plugin from the ServiceNow Store so you can integrate with ServiceNow Cloud Observability.

## Before you begin

-   Role required: evt\_mgmt\_integration

## About this task

Authenticate ServiceNow Cloud Observability as a data source to enable Event Management to collect events from ServiceNow Cloud Observability. In your ServiceNow Cloud Observability platform, use a standard webhook to set your ServiceNow AI Platform instance as the rest endpoint.

## Procedure

1.  Create a CI.

    **Note:** Discovery for ServiceNow Cloud Observability services is not supported. Create a CI manually in a ServiceNow instance \(cmdb\_ci\_service\_auto table\) to enable binding.

    1.  Navigate to **All** &gt; **Configuration** &gt; **Application Service**.

    2.  Select **New**.

    3.  In the form, enter the name.

        The name must be the service name provided in the ServiceNow Cloud Observability platform.

    4.  From the Operational Status list, set the operational status to **Operational**.

    5.  Select **Next**.

    6.  Select **Done**.

2.  In your ServiceNow Cloud Observability platform, create a notification destination.

    1.  From the navigation bar, click  **Alerts**.

    2.  Select the  **Notification destinations**  tab.

    3.  Select  **Create a destination**.

    4.  Select **webhook**.

        ![Choose Webhook](../image/choose-webhook.png "Select Webhook")

    5.  In the Name field, enter a name for the webhook.

    6.  In the URL field,  provide the webhook URL.

        This is the default  format of the URL to push events from  ServiceNow Cloud Observability to the  ServiceNow AI Platform Instance. Use this format: `https//&lt;username>:&lt;password>@&lt;instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=lightstep`

    7.  Select **New Header**.

    8.  In the Headers field, enter the **service-name** and define its **value**.

        **Note:** In a ServiceNow instance, CI binding occurs only if the **service-name** header value matches the name fields of the CI you created in the**cmdb\_ci\_service\_auto table**.

        ![Create a Webhook](../image/create-webhook.png "Create a Webhook")

    9.  Click **Create**.

3.  In the ServiceNow Cloud Observability platform, configure an alert.

    1.  From the navigation bar, click  **Alerts**.

    2.  Select  **Create an Alert** and enter an alert name.

    3.  In the Alert Configuration area, define the threshold.

    4.  In the Notification Rules area, in the Send Notifications to fields, select the notification destination as **webhook** and search for the destination name for the webhook that you created in step 2.

    5.  Select **Save**.

        The default severity for stream based alerts is **Critical**. You can change the default in the  Push Connector Configuration area of an ServiceNow AI Platform instance. The valid severity values are:

        -   1- Critical
        -   2- Major
        -   3- Minor
        -   4- Warning
        -   5- Info

