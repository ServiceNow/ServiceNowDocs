---
title: Configure Zoom to create a touchpoint meeting summary
description: Set up the Zoom spoke integration and the bi-directional web hook to generate summaries for virtual touchpoint meetings.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Touchpoint home page, Customer success, Use, Customer Success Management]
---

# Configure Zoom to create a touchpoint meeting summary

Set up the Zoom spoke integration and the bi-directional web hook to generate summaries for virtual touchpoint meetings.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_application\_admin

## Procedure

1.  To configure the Zoom spoke, follow the steps listed in Set up the Zoom spoke.

    A token is generated for Zoom connectivity.

2.  Navigate to **All** &gt; **System Properties**, edit the **sn\_acct\_lc.zoom\_integration\_user\_id** property, and specify the Zoom account User ID in the Name field.

    These steps enable you to generate a Zoom meeting link when you create a touchpoint meeting.

3.  Navigate to **All** &gt; **Zoom Spoke** &gt; **Zoom Webhook Validations** and select **New**.

4.  Enter the following details:

    -   Name: A unique name to identify the webhook validation record. For example, Zoom spoke webhook validation.
    -   Secret token: Secret token of the app in your Zoom account.
5.  Log in to your Zoom marketplace, open the General app, select **Access** &gt; **Event Subscriptions**.

    ![Event notification endpoint URL](../image/account-lifecycle-zoom-endpoint.jpg)

6.  Add the **Meeting summary has been completed** event and specify the **Event notification endpoint URL**.

    The next step is to register a Zoom webhook in ServiceNow to track events occurring in Zoom.

7.  In your ServiceNow instance, navigate to **All** &gt; **Zoom Spoke** &gt; **Zoom Webhook Registries**.

8.  Select **New**.

9.  On the form, fill in the fields.

<table id="table_fqr_v2z_1gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger Type

</td><td>

Type of the Zoom event that triggers the subflow. Select **Summary Completed** from the list.

</td></tr><tr><td>

Secret token

</td><td>

Secret token from your Zoom account used for validating event notification.

</td></tr><tr><td>

Subflow Name

</td><td>

Subflow that is to be triggered when the specified conditions are met. Select the **Process Zoom Meeting** subflow.

</td></tr><tr><td>

Input

</td><td>

Input for the webhook registry. Select the following fields from the list:-   Account ID
-   Event
-   Event TS
-   Object


</td></tr><tr><td>

Trigger Object

</td><td>

Zoom object that is used to trigger the subflow. Select **Meeting** from the list.

</td></tr><tr><td>

Name

</td><td>

Name of the webhook registry.

</td></tr></tbody>
</table>    ![Zoom webhook registry](../image/account-lifecycle-zoom-webhook.jpg)

    For more details on configuring the webhook, see Set up a bi-directional webhook for Zoom spoke.


## Result

When these steps have been completed, you can generate the meeting summary for touchpoint meetings that have been created using Zoom.

-   **[Generate summary for Zoom meetings](account-lifecycle-zoom-meeting-summary.md)**  
Generate the meeting summary for virtual meetings conducted using Zoom.

**Parent Topic:**[Touchpoint home page](../concept/account-lifecycle-touchpoint-home.md)

