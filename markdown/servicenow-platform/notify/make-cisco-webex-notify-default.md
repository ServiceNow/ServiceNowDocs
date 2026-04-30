---
title: Make Notify Cisco Webex Connector as default communication channel
description: Make Notify Cisco Webex Connector as a default communication channel to initiate a meeting to resolve the major incidents.
locale: en-US
release: yokohama
product: Notify
classification: notify
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Notify Cisco Webex Connector, Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Make Notify Cisco Webex Connector as default communication channel

Make Notify Cisco Webex Connector as a default communication channel to initiate a meeting to resolve the major incidents.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Provider Selector**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_o5z_hbm_1rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the provider you are adding. For Example, Notify Cisco Webex.

</td></tr><tr><td>

Order

</td><td>

Order in which this provider appears when multiple providers are configured.

</td></tr><tr><td>

Source table

</td><td>

The table to which Notify Cisco Webex must be added.For Example: incident.

</td></tr><tr><td>

Active

</td><td>

Option for indicating whether Notify Cisco Webex as a provider is active.

</td></tr><tr><td>

Default

</td><td>

Option for making Notify Cisco Webex the default provider if other notify providers like Zoom or Twilio are configured.

 Enable the default option.

</td></tr></tbody>
</table>4.  Select **Submit**.

5.  Select the newly created service provider.

6.  In the **Provider Selector Choices** section, select **New**.

    1.  Select **Webex** as the conference provider.

7.  Select **Submit**.


**Parent Topic:**[Configure Notify Cisco Webex Connector](../concept/setup-cisco-webex-notify.md)

