---
title: Integrate ThousandEyes with basic authentication
description: Integrate ThousandEyes with Event Management by adding a webhook in the ThousandEyes platform.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Integrate ThousandEyes platform events, Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate ThousandEyes with basic authentication

Integrate ThousandEyes with Event Management by adding a webhook in the ThousandEyes platform.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Discovery for ThousandEyes services is not supported, so you must create a CI manually in the ServiceNow instance for event binding to work.

Role required: evt\_mgmt\_admin

## About this task

Configure the Event Management environment for the collection of events from ThousandEyes by authenticating ThousandEyes as a data source. In your ThousandEyes platform, set your ServiceNow AI Platform instance as a rest endpoint using a webhook.

## Procedure

1.  In the ServiceNow instance, complete the following steps to create a CI.

    1.  From the navigation bar, navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.

    2.  Click **Hierarchy** and search for `HTTP(S) Endpoint`.

    3.  Select **CI List** and create a new CI.

2.  In the ThousandEyes platform, create a notification destination.

    1.  From the navigation bar, navigate to **Alerts** &gt; **Alert Rules**.

    2.  Click on any existing alert rule and select the **Notification** tab.

    3.  Select **Edit Webhook** and enter the following information.

<table id="table_mb4_fwf_1rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the webhook.

</td></tr><tr><td>

URL

</td><td>

Provide the webhook URL.**Note:** The default format of the URL to push events from ThousandEyes to the ServiceNow instance is `https://<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=thousandeyes`.

</td></tr><tr><td>

Auth Type

</td><td>

Select **Basic**.

</td></tr></tbody>
</table>    4.  Click **Add New Webhook**.


## Result

The default severity for the ThousandEyes alert is **Major -2**, which can be changed in the **Push Connector Configuration** section of **Push Connectors** &gt; **ThousandEyes Push Connector**. The valid values of severity are **1- Critical**, **2- Major**, **3- Minor**, **4- Warning**, and **5- Info**.

The default timezone of the ThousandEyes alert is GMT, if you want to send the alert in a different timezone, it can be changed in the **Push Connector Configuration** section of **Push Connectors** &gt; **ThousandEyes Push Connector**. The valid value format is **GMT+01:00**, **GMT+02:00**, **GMT-05:30**, **GMT-02:00**, etc.

