---
title: Integrate Sentry events
description: Integrate Sentry with Event Management by adding a standard webhook in the Sentry platform.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Integrate Sentry events

Integrate Sentry with Event Management by adding a standard webhook in the Sentry platform.

## Before you begin

Ensure that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Discovery for Sentry services are not supported. You must create a CI manually in a ServiceNow instance in the \[cmdb\_ci\_service\_auto\] table to enable binding by completing the following steps:

1.  From the navigation bar, go to **Configuration/Application Service**.
2.  Provide the project name you are monitoring on the Sentry application.
3.  Set the operational status to **Operational**.
4.  Click **Next** then **Done**.

Role required: evt\_mgmt\_admin

## About this task

Configure Event Management for the collection of events from Sentry by authenticating Sentry as a data source. In your Sentry platform, use a standard webhook to set your ServiceNow AI Platform as the rest endpoint.

## Procedure

1.  In the Sentry console, create an internal integration.

    1.  Navigate to **Settings** &gt; **Developer Settings**.

    2.  Click **New Internal Integration**.

    3.  In the Internal Integration Details section, on the Sentry Integration Details page, fill in the fields.

<table id="table_bhz_3zr_2tb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of your integration.

</td></tr><tr><td>

Webhook URL

</td><td>

The default format of the URL to push events from Sentry to the ServiceNow AI Platform instance. For example, `https://<username>:<password>@<instance-name>.service-now.com/api/sn_em_connector/em/inbound_event?source=sentry`.

</td></tr><tr><td>

Alert Rule Action

</td><td>

Option to enable the integration.**Note:** When enabled, the integration becomes available in the Issue Alert and Metric Alert rules in Sentry. The alerts will be sent to the ServiceNow instance.

</td></tr><tr><td>

Schema

</td><td>

Schema for your UI components. This field should be left empty.

</td></tr><tr><td>

Overview

</td><td>

Description for the integration.

</td></tr><tr><td>

Authorized JavaScript Origins

</td><td>

Auth Tokens from the browser to enable the origins of the pages making the requests. This field should be left empty.

</td></tr></tbody>
</table>    4.  In the Permissions section, under Issue &amp; Event, specify the level of access you want.

        You can select **Read**, **Read &amp; Write**, or **Admin**.

    5.  In the Webhooks section, select the **Issue** check box.

    6.  Click **Save Changes**.

2.  In the Sentry console, create alert rules and configure them to receive alerts for issues from Sentry to the ServiceNow instance.

    1.  Navigate to **Alerts** &gt; **Create Alert Rule**.

    2.  Select the alert type and click **Set Conditions**.

        **Note:** The Issues alert type creates issue alerts. The other alert options create metric alerts.

    3.  On the Alert Rule page, create either an issue alert or a metric alert.

<table id="table_ptp_xhs_2tb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Issue alert

</td><td>

1.  Enter the environment, team, and alert name for your alert.
2.  Under Set conditions, enter the **When** and **If** conditions that will trigger the alert.
3.  For the **Then** condition, select **Send a notification via an integration** and select your internal integration from the list.
4.  Set the action interval for the alert.


</td></tr><tr><td>

Metric alert

</td><td>

1.  Add a filter to your transactions.
2.  Select the function and time interval.
3.  Set the thresholds that will trigger the alert.
4.  Add the actions to be performed when the thresholds defined are met.
5.  Add your internal integration from the list to the list of actions to receive the alerts.
6.  Add a rule name and team for the alert.


</td></tr></tbody>
</table>    4.  Click **Save Rule**.


**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

