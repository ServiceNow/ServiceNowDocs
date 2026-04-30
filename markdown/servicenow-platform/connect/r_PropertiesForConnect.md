---
title: Properties for Connect
description: The Connect Properties page provides several configuration options for Connect.
locale: en-US
release: yokohama
product: Connect
classification: connect
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Connect administration, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Properties for Connect

The Connect Properties page provides several configuration options for Connect.

**Important:**

Core UI is required to use Connect Chat. Connect Chat is not supported in Next Experience. If you turn on Next Experience, Connect Chat will no longer work. See [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for more information.

Users with the admin role can access these properties by navigating to **Connect** &gt; **Administration** &gt; **Properties**.

**Note:** Many of the properties also impact Connect Support.

<table id="table_ytc_kkb_mv"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Disable Presenceglide.ui.presence.disabled

</td><td>

Turns off user presence globally when enabled. Enabling this property turns off user presence throughout the platform, not just in Connect.-   **Type**: true \| false
-   Default value: false
-   Location: **Connect** &gt; **Administration** &gt; **Properties**
-   Learn more: [User presence](https://www.servicenow.com/docs/access?context=c_UserPresence&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)

</td></tr><tr><td>

Enable Connect in the framesetcollaboration.frameset

</td><td>

Determines whether the Connect overlay is visible \(enabled\). This property also impacts Connect Support.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**
-   Learn more: [Disable the Connect overlay](../task/t_DisableTheCollaborationOverlay.md)

</td></tr><tr><td>

Enable Connect to retrieve external link metadata in order to render richer content in messages with links to YouTube, news articles, images, etc.glide.ui.url.external, glide.ui.url.external.content

</td><td>

Enables Connect to render URLs for external sites as links. When this property is disabled, URLs that point anywhere outside the instance appear as plain text. This property also impacts Connect Support.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Number of minutes to wait before collecting unread messages and sending an email to offline users.collaboration.email\_interval

</td><td>

Sets the number of minutes the system waits before sending a Connect notification email to an inactive user.-   **Type**: integer
-   Default value: 3
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**
-   Learn more: [Configure the email notification interval](../concept/c_CollaborationAdministration.md#)

</td></tr><tr><td>

Maximum number of latest conversations to show during search. \(Default = 50\)

</td><td>

Sets the number of results that appear when you search conversations in Connect. In the System Properties \[sys\_properties\] table, this property appears as **connect.search.conversation\_limit**.-   Type: integer
-   Default value: 50

</td></tr><tr><td>

Audio file to play to notify users of new messages, support conversation transfers and @mentions in Connect. This property's value should point to the 'name' field of an audio file in the db\_audio table.connect.notification.audio\_alert

</td><td>

Specifies the audio file to play to notify users of new messages, support conversation transfers, and @mentions in Connect. This property's value must point to the **Name** field of a record in the Audio File \[db\_audio\] table. This property also impacts Connect Support.-   **Type**: string
-   Default value: connect\_alert.mp3
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**
-   Learn more: [Customize the Connect audio notification sound](../task/t_CustomizeConnectAudioNotifSound.md)

</td></tr><tr><td>

Comma separated allow list of roles able to access Connect. Empty allows all roles.connect.roles

</td><td>

Determines which user roles are required to access Connect. When the value is blank, no role is required. This property also impacts Connect Support.**Note:** If you choose to restrict Connect access to specific roles, consider updating the role requirements for Connect modules and other access points.

 -   **Type** : string
-   Default value: &lt;empty&gt;
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**

</td></tr><tr><td>

Determine whether or not a button is shown in task forms to view the Collaboration document conversation or Live Feed Record Feed related to the task. Note: The Collaboration button will only be enabled if the frameset view is also enabled with collaboration.frameset = trueglide.live\_feed.task\_header\_button

</td><td>

Determines whether the show Live Feed icon \(![Show Live Feed icon](../../live-feed/image/ShowLiveFeedIcon.png)\) and **Follow** button are available in the form header of tables that have the **live\_feed=true** dictionary attribute.-   **Type**: choice list
-   Default value: collaboration
-   Other possible values:
    -   **both**: enables both the show Live Feed icon and the **Follow** button.
    -   **live\_feed**: enables the show Live Feed icon.
    -   **none**: disables both the show Live Feed icon and the **Follow** button.
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**
-   Learn more: [Configure record conversations](../concept/c_CollaborationAdministration.md#)

</td></tr><tr><td>

Disable the legacy chat "Create or Join Chat Room" link on the Incident form \(Must have Chat plugin enabled to see link\)glide.connect.enabled

</td><td>

Hides the **Create or Join Chat Room** related link, which appears on the Incident form when legacy chat is enabled. Legacy chat and Connect Chat should not be used concurrently and this property should not be modified.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Administration** &gt; **Properties**

</td></tr></tbody>
</table>