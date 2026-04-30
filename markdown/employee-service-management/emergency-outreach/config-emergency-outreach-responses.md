---
title: Configure Emergency Outreach response options
description: Configure the response options that employees choose from to respond to an Emergency Outreach health status request. You can modify the base system responses, add new responses, and deactivate responses you no longer use.
locale: en-US
release: xanadu
product: Emergency Outreach
classification: emergency-outreach
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Emergency Outreach notifications, Emergency Outreach, Emergency Response Management, Workplace Service Delivery, Employee Service Management]
---

# Configure Emergency Outreach response options

Configure the response options that employees choose from to respond to an Emergency Outreach health status request. You can modify the base system responses, add new responses, and deactivate responses you no longer use.

## Before you begin

Role required: sn\_imt\_checkin.checkin\_admin or admin

## About this task

Response options appear in the Emergency Outreach email notification that employees receive.

![Email notification message](../image/voluntary_health_checkin_email.png "Email message with responses")

## Procedure

1.  Navigate to **All** &gt; **Emergency Outreach** &gt; **Response Options**.

2.  Change the text of a response option.

    1.  Open the response option.

    2.  Edit the text in the **Response text** field.

    3.  Click **Update**.

3.  Change the order in which response options appear.

    The easiest way to change the order is to use the list edit feature in the list of response options. You can also open each option to update the order number. Responses appear in numerical order.

    1.  In the **Order** list, double-click the order value to update.

        ![List edit open to change the number value](../image/list-edit-change-order-number.png)

    2.  Enter the number and click the green check mark icon.

    3.  Verify that the responses appear in the appropriate order by clicking the **Order** column header until it is sorted in descending order.

4.  Add a response option.

    1.  In the Response Options list, click **New.**

    2.  Fill in the fields.

<table id="table_okc_rgy_llb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Response text

</td><td>

The text the user can select as a response.

</td></tr><tr><td>

Order

</td><td>

The number that specifies the position of this response in the list. To put the new response:-   First, give it the lowest number.
-   In the middle, give it a number between the numbers of the responses above and below.
-   At the end, give it the latest number.


</td></tr><tr><td>

Response value

</td><td>

Read-only, unique value based on the response text.

</td></tr><tr><td>

Active

</td><td>

Option for ensuring that this response option appears in the notification.

</td></tr><tr><td>

SMS Option

</td><td>

The number a user selects to reply to an SMS notification with this response. Every SMS option must have a unique number.**Note:** Assign a number if your company will use this response in SMS notifications.

</td></tr><tr><td>

Response mode

</td><td>

The mode of the outreach notification, such as Outreach Acknowledgements.

</td></tr></tbody>
</table>    3.  Click **Submit**.

5.  Deactivate a response option by clearing the **Active** check box and clicking **Update**.


