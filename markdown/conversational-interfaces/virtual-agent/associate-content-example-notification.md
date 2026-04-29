---
title: Associate content with the Asset Refresh notification
description: After creating the actionable notification for the Asset Refresh topic, go back into the notification and add content. This links the notification with the Virtual Agent topic that you created.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Associate, Asset Refresh, content, virtual agent, notification, provider]
breadcrumb: [Example Asset Refresh Virtual Agent conversation with notifications, Virtual Agent chat widget interface for NLU, Explore, Virtual Agent, Conversational Interfaces]
---

# Associate content with the Asset Refresh notification

After creating the actionable notification for the Asset Refresh topic, go back into the notification and add content. This links the notification with the Virtual Agent topic that you created.

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications**.

2.  Select the Asset Refresh Notification to open the record.

    New fields for content are available in the record.

    ![New tabs and fields are available in the record: Additional Recipients, Contents, Actions, Link Actions to Content, and Logs.](../images/crawl-ex-notif-content.png)

3.  Select the **Contents** tab and create the content for the notification.

    1.  Select **New Provider Content**.

    2.  When prompted for the type of notification content, select **Virtual Agent Content - Chat**.

    3.  On the form, fill in the fields.

<table id="table_apt_v4b_rxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the content. For example, enter `Asset Refresh Notification Content`.

</td></tr><tr><td>

Notification

</td><td>

By default, **Asset Refresh Notification**.

</td></tr><tr><td class="sub-head" colspan="2">

Format tab

</td></tr><tr><td>

Type

</td><td>

Select **Simple**.

</td></tr><tr><td>

Table

</td><td>

Specify **Hardware \[alm\_hardware\]**.

</td></tr><tr><td class="sub-head" colspan="2">

Message tab

</td></tr><tr><td>

Advanced

</td><td>

Leave this option unselected.

</td></tr><tr><td>

Message heading

</td><td>

A suitable heading for the notification, such as `Upgrade your device`.

</td></tr><tr><td>

Message

</td><td>

The contents of your message letting the user know that it's time for them to upgrade. You can customize the message using variables in the record for a more personal touch.

</td></tr><tr><td class="sub-head" colspan="2">

Channels tab

</td></tr><tr><td>

Delivery channels

</td><td>

Select **mweb**, which is the default channel for Virtual Agent. You can configure other channels to run Virtual Agent as well. For more information, see [Integrating Virtual Agent with other channels](../concept/integrate-virtual-agent.md).

</td></tr></tbody>
</table>    4.  Select **Submit**.

    ![The Asset Refresh Notification Content record displays on the Contents tab for the notification.](../images/crawl-ex-notif-content-done.png)

4.  On the Asset Refresh Notification record, select the **Actions** tab and create the action.

    1.  Select **New Provider Action**.

    2.  When prompted for the type of notification action, select **Virtual Agent**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for this action. For example, enter `Asset Refresh Notification Action`.|
        |Notification|By default, **Asset Refresh Notification**.|
        |Active|Ensure this option is selected.|
        |Topic|The name of the published Asset Refresh Virtual Agent topic you created in previous steps.|

    4.  Select **Submit**.

    ![The Asset Refresh Notification Actions record displays on the Actions tab for the notification.](../images/crawl-ex-notif-actions.png)

5.  On the Asset Refresh Notification record, select the **Link Actions to Content** tab to map the actions to the content.

    1.  Select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name for the actionable content. For example, enter `Asset Refresh Actionable Content`.|
        |Notification|By default, **Asset Refresh Notification**.|
        |Actions|Select the lock icon ![Lock icon.](../../../common/image/icon-lock.png), and then type in the search field or select the search icon ![Search icon.](../images/icon-search.png) to locate the action you created on the **Actions** tab in the previous step.|
        |Content|The name of the Asset Refresh provider content record you created on the **Contents** tab in a previous step.|
        |Disable skip|Leave this option unselected.|
        |Active|Leave this option selected.|

        ![The Actionable Content form references both the action and the content that you created in a previous step.](../images/crawl-ex-actionable-content-rec.png)

    3.  Select **Submit**.


