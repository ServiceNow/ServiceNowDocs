---
title: Properties installed with Connect
description: Properties are added with activation of Connect.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Properties installed with Connect

Properties are added with activation of Connect.

**Note:** To open the System Property \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_vmr_bbd_br"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

collaboration.email\_interval

</td><td id="entry_CollaborationEmailIntervalDescription">

Sets the number of minutes the system waits before sending a Connect notification email to an inactive user.-   **Type**: integer
-   Default value: 3
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**
-   Learn more: [Configure the email notification interval](../concept/c_CollaborationAdministration.md#)

</td></tr><tr><td>

collaboration.frameset

</td><td id="entry_CollaborationFramesetDescription">

Determines whether the Connect overlay is visible \(enabled\). This property also impacts Connect Support.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**
-   Learn more: [Disable the Connect overlay](../task/t_DisableTheCollaborationOverlay.md)

</td></tr><tr><td>

collaboration.polling\_interval

</td><td>

Sets the number of seconds the system waits between polling for new Connect messages. This property also impacts Connect Support.-   **Type**: integer
-   Default value: 10
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

connect.notification.audio\_alert

</td><td id="entry_ConnectNotificationAudioAlertDescription">

Specifies the audio file to play to notify users of new messages, support conversation transfers, and @mentions in Connect. This property's value must point to the **Name** field of a record in the Audio File \[db\_audio\] table. This property also impacts Connect Support.-   **Type**: string
-   Default value: connect\_alert.mp3
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**
-   Learn more: [Customize the Connect audio notification sound](../task/t_CustomizeConnectAudioNotifSound.md)

</td></tr><tr><td>

connect.retrieve\_external\_link\_content

</td><td id="entry_ConnectRetrieveExternalLinkContentDescription">

Enables Connect to render URLs for external sites as links. When this property is disabled, URLs that point anywhere outside the instance appear as plain text. This property also impacts Connect Support.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

connect.roles

</td><td id="entry_ConnectRolesDescription">

Determines which user roles are required to access Connect. When the value is blank, no role is required. This property also impacts Connect Support.**Note:** If you choose to restrict Connect access to specific roles, consider updating the role requirements for Connect modules and other access points.

 -   **Type** : string
-   Default value: &lt;empty&gt;
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

glide.connect.enabled

</td><td id="entry_GlideConnectEnabledDescription">

Hides the **Create or Join Chat Room** related link, which appears on the Incident form when legacy chat is enabled. Legacy chat and Connect Chat should not be used concurrently and this property should not be modified.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

glide.connect.chat.disabled

</td><td>

Disables and hides all UI elements related to Connect.-   **Type**: true \| false
-   Default value: false
-   Location: System Property \[sys\_properties\] table

</td></tr><tr><td>

glide.live\_feed.task\_header\_button

</td><td id="entry_GlideLiveFeedTaskHeaderButtonDescription">

Determines whether the show Live Feed icon \(![Show Live Feed icon](../../live-feed/image/ShowLiveFeedIcon.png)\) and **Follow** button are available in the form header of tables that have the **live\_feed=true** dictionary attribute.-   **Type**: choice list
-   Default value: collaboration
-   Other possible values:
    -   **both**: enables both the show Live Feed icon and the **Follow** button.
    -   **live\_feed**: enables the show Live Feed icon.
    -   **none**: disables both the show Live Feed icon and the **Follow** button.
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**
-   Learn more: [Configure record conversations](../concept/c_CollaborationAdministration.md#)

</td></tr></tbody>
</table>