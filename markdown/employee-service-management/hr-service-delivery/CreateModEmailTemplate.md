---
title: Add or modify email content for notifications
description: Use the Email Content form to create notification templates to alert the assigned to of an HR task when a due date is approaching.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [HR notifications, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Add or modify email content for notifications

Use the **Email Content** form to create notification templates to alert the assigned to of an HR task when a due date is approaching.

## Before you begin

Roles required: sn\_hr\_core.case\_writer, sn\_hr\_le.activity\_writer

You must have the HR Case Writer \[sn\_hr\_core.case\_writer\] or Lifecycle Event Activity Writer \[sn\_hr\_le.activity\_writer\] role to select an **Email Content** template. For Lifecycle Events, you must have the Lifecycle Event Activity Writer \[sn\_hr\_le.activity\_writer\] role to create or edit an HR task template for Lifecycle Events.

When setting up notifications, an email template must be created. The base system provides an email template that can be used as a model.

Email notifications can be sent for HR tasks with due dates and can be configured:

-   To be sent relative to the due date.
-   To be sent at intervals until the task is completed or skipped.
-   With customized content.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **Email Content**.

2.  From the **Email Contents** list, select **New** or an existing email template to edit.

3.  Enter or edit the fields on the **Email Content** form.

<table id="choicetable_yhq_hsr_mbb"><thead><tr><th align="left" id="d617836e107">

Field

</th><th align="left" id="d617836e110">

Description

</th></tr></thead><tbody><tr><td id="d617836e116">

**Name**

</td><td>

Enter or edit the name of the email template.

</td></tr><tr><td id="d617836e125">

**Type**

</td><td>

Select the type of notification:-   Activity Notification
-   HR Task Reminder


</td></tr><tr><td id="d617836e143">

**Subject**

</td><td>

Enter or edit the subject line of the reminder notification. The text appears in the subject line of the email sent as a reminder notification.

</td></tr><tr><td id="d617836e152">

**Message HTML**

</td><td>

Enter or edit text that is the main body of the email notification. Use the formatting tools to format the text such as bold, italic, underline, font styling, justification, bullets, insert image, and numbers.

</td></tr><tr><td id="d617836e162">

**- +**

</td><td>

Click the - to delete lines from the message area or + to add lines.

</td></tr><tr><td id="d617836e171">

**Select variables**

</td><td>

This section provides a list of variables that can be used in the email template. Variables pull information from a table so information can be repeatable and customizable depending on the type of notification selected.The variables that appear depend on the **Type** field.

-   Activity Notification: HR Lifecycle Events Case \[sn\_hr\_le\_case\]
-   HR Task Reminder: HR Case \[sn\_hr\_core\_case\]


</td></tr></tbody>
</table>4.  Select **Save** to save the record and remain on the **Email Content** form.

    Or, select**Submit** or **Update** to return to the **Email Contents** list.


**Parent Topic:**[HR notifications](../concept/HRNotifications.md)

