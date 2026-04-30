---
title: NowChatService class - Android
description: The NowChatService class provides functions that enable you to launch the NowChat activity and set error configurations.Launches the intent used to open the NowChat activity. Typically used for creating a \[android.app.PendingIntent\].Launches the specified NowChat activity.Subscribes to the unread chat message count listener.Unsubscribes from receiving the unread message count.Updates the NowChat UI theme with the specified UI theme. Use this function to update the chat UI theme after it has been initially set using the start\(\) function, such as when changing the theme from light to dark.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Mobile SDK API reference - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatService class - Android

The NowChatService class provides functions that enable you to launch the NowChat activity and set error configurations.

**Parent Topic:**[Mobile SDK API reference - Android](../../concept/MobileSDKAndroidAPI.md)

## NowChatService - launchIntent\(context:Context, nowChatTheme:NowChatTheme\):Intent

Launches the intent used to open the NowChat activity. Typically used for creating a `[android.app.PendingIntent]`.

<table id="table_yv2_43l_nrb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

context

</td><td>

Context

</td><td>

Context used to build the intent.

</td></tr><tr><td>

nowChatTheme

</td><td id="Chat-themeColors-entry1">

[NowChatTheme](../../NowChatTheme/concept/NowChatThemeColorsAndroidInterface.md)

</td><td>

Optional. Theme object to use in the NowChat UI.Default: Default colors

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Intent|Intent and theme colors used to launch the associated NowChat activity.|

This example shows how to call the launchIntent\(\) method and process the return activity.

```
val intent = nowChatService.launchIntent(this) 
val pendingIntent = PendingIntent.getActivity( 
    this, 
    REQUEST_CODE,
    intent,
    PendingIntent.FLAG_IMMUTABLE 
) 

val notification = createNotification(title, message, pendingIntent)
notificationManager.notify(push.notificationId, notification) 
```

## NowChatService - start\(activity: Activity, themeColors: NowChatTheme = object: NowChatTheme\{\}, contextData: Map&lt;String, Any&gt; = mapOf\(\), chatConfiguration: NowChatConfiguration? = null\)

Launches the specified NowChat activity.

<table id="table_lbg_cyg_tpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

activity

</td><td>

[Activity](https://developer.android.com/reference/kotlin/android/app/Activity.html)

</td><td>

Activity context to use to launch the NowChat activity and to receive the `NowChatExitCode` as a resultCode through the onActivityResult.

</td></tr><tr><td>

nowChatTheme

</td><td id="Chat-themeColors-entry1">

[NowChatTheme](../../NowChatTheme/concept/NowChatThemeColorsAndroidInterface.md)

</td><td>

Optional. Theme object to use in the NowChat UI.Default: Default colors

</td></tr><tr><td>

contextData

</td><td>

Map&lt;String, Any&gt;

</td><td>

Optional. Additional chat context variables to pass into the chat session.For additional information on chat context variables, see [Live agent chat context variables](https://www.servicenow.com/docs/access?context=live-agent-chat-context-vars&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

chatConfiguration

</td><td>

[NowChatConfiguration](../../NowChatOptions/concept/NowChatOptionsAndroid.md#)

</td><td>

Optional. ChatConfiguration to apply while using NowChat.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
suspend fun launchChat() {
    val chatService = getNowChatService()

    val chatTheme = object : NowChatTheme {
        override val brand: Int
            get() = Color.BLUE

        override val textPrimary: Int
            get() = Color.BLACK

        // Override remaining theme colors

    }
    val contextData = mapOf("sys_id" to "123456789", "table" to "wm_task")

    //drawable to be used instead of the default NowChat back button.
    val myDrawable = ContextCompat.getDrawable(activity, R.drawable.my_drawable)

    val chatConfiguration = NowChatConfiguration(
        closePrompt = NowChatConfiguration.ClosePrompt(
            header = null,
            message = "Are you sure you want to leave?",
            acceptButtonTitle = "Yes",
            declineButtonTitle = "No"
        ),
        disabledFeatures = listOf(NowChatConfiguration.Feature.START_NEW_CONVERSATION),
        conversationOptions = listOf(NowChatConfiguration.ConversationOption.FORCE_NEW_CONVERSATION),
        uiConfiguration = NowChatConfiguration.UIConfiguration(
            closeButton = NowChatConfiguration.CloseButton(
                icon = myDrawable
            ),
            attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible = false)
        )
    )

    chatService?.start(activity, chatTheme, contextData, chatConfiguration)
}
```

## NowChatService - subscribeToUnreadMessageCount\(pollingInterval: Long, listener: NowChatUnreadMessagesCountListener\)

Subscribes to the unread chat message count listener.

<table id="table_zrg_k1m_cqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pollingInterval

</td><td>

Long

</td><td>

Frequency at which to poll the web service for the unread chat message count.Unit: Milliseconds

</td></tr><tr><td>

listener

</td><td>

NowChatUnreadMessagesCountListener

</td><td>

Listener that you implement to obtain the number of unread chat messages. You must also unsubscribe to this listener when you no longer want to obtain the unread message count using the [NowChatService - unsubscribeFromUnreadMessageCount\(listener: NowChatUnreadMessagesCountListener\)](NowChatServiceAndroidAPI.md#) method.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following example shows how to subscribe to and unsubscribe from a chat unread message count listener.

```
private val unreadMessageCountListener = object: NowChatUnreadMessagesCountListener {
  override fun unreadMessagesCountDidChange(unreadMessageCount: Int) {
  }
}

fun setup() {
  nowChatService.subscribeToUnreadMessageCount(pollingInterval:1000, unreadMessageCountListener)
}

fun teardown() {
  nowChatService.unsubscribeFromUnreadMessageCount(unreadMessageCountListener)
}

```

## NowChatService - unsubscribeFromUnreadMessageCount\(listener: NowChatUnreadMessagesCountListener\)

Unsubscribes from receiving the unread message count.

|Name|Type|Description|
|----|----|-----------|
|listener|NowChatUnreadMessagesCountListener|Listener that you implement to unsubscribe from the chat unread message count listener.|

|Type|Description|
|----|-----------|
|None| |

The following example shows how to subscribe to and unsubscribe from a chat unread message count listener.

```
private val unreadMessageCountListener = object: NowChatUnreadMessagesCountListener {
  override fun unreadMessagesCountDidChange(unreadMessageCount: Int) {
  }
}

fun setup() {
  nowChatService.subscribeToUnreadMessageCount(pollingInterval:1000, unreadMessageCountListener)
}

fun teardown() {
  nowChatService.unsubscribeFromUnreadMessageCount(unreadMessageCountListener)
}

```

## NowChatService – updateTheme\(nowChatTheme: NowChatTheme\)

Updates the NowChat UI theme with the specified UI theme. Use this function to update the chat UI theme after it has been initially set using the start\(\) function, such as when changing the theme from light to dark.

|Name|Type|Description|
|----|----|-----------|
|nowChatTheme|[NowChatTheme](../../NowChatTheme/concept/NowChatThemeColorsAndroidInterface.md)|Theme object to use in the NowChat UI.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to update a light UI theme implemented using the start\(\) function to the dark UI theme using the updateTheme\(\) function.

```
val chatService = serviceManager.getNowChatService()

val chatThemeLight = object : NowChatTheme {
    override val backgroundPrimary: Int
        get() = Color.WHITE

    override val textPrimary: Int
        get() = Color.BLACK

    // Override remaining theme colors
}

val chatThemeDark = object : NowChatTheme {
    override val backgroundPrimary: Int
        get() = Color.BLACK

    override val textPrimary: Int
        get() = Color.WHITE

    // Override remaining theme colors
}

//start NowChat with light theme
chatService?.start(activity, chatThemeLight)


//update NowChat theme to dark theme
chatService?.updateTheme(chatThemeDark)

```

