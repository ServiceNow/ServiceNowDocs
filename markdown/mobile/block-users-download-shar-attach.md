---
title: Block users from downloading or sharing attachments
description: Set the glide.sg.block\_mobile\_attachments\_sharing system property to true to hide the sharing button in the mobile app native viewer.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-05-19"
reading_time_minutes: 1
breadcrumb: [Mobile system property configurations, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Block users from downloading or sharing attachments

Set the **glide.sg.block\_mobile\_attachments\_sharing** system property to `true` to hide the sharing button in the mobile app native viewer.

## Before you begin

Role required: admin

## About this task

When **glide.sg.block\_mobile\_attachments\_sharing** system property is set to `false`, users can download or share attachments by tapping the share button on their device screens:

![Mobile app with share button displaying](../image/share-button-displayed.png)

When **glide.sg.block\_mobile\_attachments\_sharing** system property is set to `true`, the share button on users' device screens isn't displayed. In this case, users can't download or share attachments:

![Mobile app without the share button](../image/no-share-button-displayed.png)

## Procedure

1.  Type `sys_properties.list` in the Application Navigator.

2.  Open the record for **glide.sg.block\_mobile\_attachments\_sharing**.

3.  In the form match the following values:

<table id="table_imb_bjr_jfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

**glide.sg.block\_mobile\_attachments\_sharing**

</td></tr><tr><td>

Type

</td><td>

**true \| false**

</td></tr><tr><td>

Value

</td><td>

Enter one of the following values:

 -   Enter `true` to turn off the share button in mobile app screens.
-   Enter `false` to display the share button in mobile app screens.


</td></tr></tbody>
</table>4.  Right-click the banner at the top of the **glide.sg.block\_mobile\_attachments\_sharing** form and select **Save**.


**Parent Topic:**[Mobile system property configurations](../concept/additional-mobile-configuration.md)

