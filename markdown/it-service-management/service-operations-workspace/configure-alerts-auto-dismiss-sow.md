---
title: Configure alerts in Service Operations Workspace
description: Configure the alert and notification messages in Service Operations Workspace \(SOW\) using UI Builder to automatically dismiss within a specified time and automatically expand the alert notification content.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure alerts in Service Operations Workspace

Configure the alert and notification messages in Service Operations Workspace \(SOW\) using UI Builder to automatically dismiss within a specified time and automatically expand the alert notification content.

## Before you begin

The UI Builder bundle must be installed or updated to version 28.1.

Role required: sn\_sow\_admin.sn\_sow\_admin or admin

## About this task

If you don't have the UI Builder application updated to version 28.1, you can still configure the alert notifications by navigating to **All** &gt; **Now Experience Framework** &gt; **Experiences** and then select Service Operations Workspace from the list of UX applications. You can then select the **alert\_auto\_dismiss\_config** UX page property and customize the script in the **Value** field to configure the alert notifications.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the **Experiences** tab, from the application list, search and select Service Operations Workspace.

3.  Select **View experience settings**.

4.  In the Configure alerts section, fill in the following fields:

<table id="table_xzy_jzg_vfc"><thead><tr><th>

Alert status

</th><th>

Auto-dismiss

</th><th>

Timeout \(Seconds\)

</th></tr></thead><tbody><tr><td>

Critical

</td><td>

Select the check box to automatically dismiss the critical alerts.**Note:** By default, this check box is cleared.

</td><td>

Specify the time in seconds within which the critical alert is dismissed automatically.**Note:** By default, this field is empty.

</td></tr><tr><td>

High

</td><td>

Select the check box to automatically dismiss the high alerts.**Note:** By default, this check box is cleared.

</td><td>

Specify the time in seconds within which the high alert is dismissed automatically.**Note:** By default, this field is empty.

</td></tr><tr><td>

Moderate

</td><td>

Select the check box to automatically dismiss the moderate alerts.**Note:** By default, this check box is cleared.

</td><td>

Specify the time in seconds within which the moderate alert is dismissed automatically.**Note:** By default, this field is empty.

</td></tr><tr><td>

Warning

</td><td>

Select the check box to automatically dismiss the warning alerts.**Note:** By default, this check box is cleared.

</td><td>

Specify the time in seconds within which the warning alert is dismissed automatically.**Note:** By default, this field is empty.

</td></tr><tr><td>

Info

</td><td>

Select the check box to automatically dismiss the info notification messages.**Note:** By default, this check box is selected.

</td><td>

Specify the time in seconds within which the info notification message is dismissed automatically.**Note:** By default, this field is set to three seconds.

</td></tr><tr><td>

Positive

</td><td>

Select the check box to automatically dismiss the positive or success notification messages.**Note:** By default, this check box is selected.

</td><td>

Specify the time in seconds within which the positive or success notification message is dismissed automatically.**Note:** By default, this field is set to three seconds.

</td></tr><tr><td>

Low

</td><td>

Select the check box to automatically dismiss the low notification messages.**Note:** By default, this check box is selected.

</td><td>

Specify the time in seconds within which the low notification message is dismissed automatically.**Note:** By default, this field is set to three seconds.

</td></tr></tbody>
</table>    **Note:** The **Timeout \(Seconds\)** field is enabled only if the **Auto-dismiss** check box is selected for the specific alert status such as Critical, Moderate and so on.

<table id="table_ydt_lzg_vfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show time label

</td><td>

Select the check box to display the time label along with the visual time indicator when alert notification is automatically dismissed within the set auto-dismiss time.**Note:** By default, this check box is cleared.

</td></tr><tr><td>

Expand alert content by default

</td><td>

Select the check box to automatically expand the alert content in the alert notification message.**Note:** By default, this check box is selected.

</td></tr></tbody>
</table>    ![Configure alerts settings](../image/sow-configure-alerts-ui-builder.png)

    **Note:** You can view the Configure alerts section only if you have updated UI Builder application to version 28.1 \(Zurich\).

5.  Select **Save**.


**Parent Topic:**[Configuring Service Operations Workspace for ITSM to improve your experience](../concept/configuring-sow-to-improve-experience.md)

