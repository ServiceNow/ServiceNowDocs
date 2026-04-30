---
title: Create a flow notification action
description: Select Flow Action from the Notification Action wizard to create a flow notification action.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Select provider notification action capabilities, Create provider notification, Provider notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a flow notification action

Select **Flow Action** from the Notification Action wizard to create a flow notification action.

## Before you begin

Role required: admin

## Procedure

1.  Select **Flow Action**.

2.  On the form, fill in the fields.

<table id="table_ph5_fns_xjb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the notification action.

</td></tr><tr><td>

Notification

</td><td>

Name of the notification containing the notification action record.

</td></tr><tr><td>

Async

</td><td>

Option to execute configured flow or action asynchronously.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification action record.

</td></tr><tr><td>

Choose Flow or Action

</td><td>

Option to select either Flow or Action. See [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US) for more information.**Note:** You can select either Flow or Action, but not both.

</td></tr><tr><td>

Inputs

</td><td>

Script used for the creation of flow notification action.**Note:** The script returns Json of key value pairs, which is passed as input in executing configured flow or action.

</td></tr><tr><td>

Acknowledgement

</td><td>

Acknowledgement message after an action is selected from a notification.

</td></tr></tbody>
</table>3.  Click **Submit**.


**Parent Topic:**[Select provider notification action capabilities](noti-provider-action-capabilities.md)

