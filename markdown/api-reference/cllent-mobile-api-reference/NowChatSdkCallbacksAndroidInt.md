---
title: NowChatSdkCallbacks interface - Android
description: The NowChatSdkCallbacks interface provides functions that enable callbacks for host applications to configure or handle actions from the NowChatSDK.Called when the chat screen is closed and the chat session ends.Handles the specified URI, such as opening it in a webview, custom tab, or external browser.Sets the result code to return when NowChat is exited.Returns the view to display when the NowChat UI data is loading; typically a configured indeterminate progress bar.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - Android, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatSdkCallbacks interface- Android

The NowChatSdkCallbacks interface provides functions that enable callbacks for host applications to configure or handle actions from the NowChatSDK.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isFileCollectionBlocked

</td><td>

Boolean

</td><td>

Flag that indicates whether the host application should prevent NowChat from opening the file picker.Valid values:

-   true: Prevent the file picker from opening.
-   false: Allow the file picker to open.

</td></tr><tr><td>

isGalleryCollectionBlocked

</td><td>

Boolean

</td><td>

Flag that indicates whether the host application should prevent NowChat from opening the photo gallery.Valid values:

-   true: Prevent the photo gallery from opening.
-   false: Allow the photo gallery to open.

</td></tr><tr><td>

isLocationCollectionBlocked

</td><td>

Boolean

</td><td>

Flag that indicates whether the host application should prevent NowChat from accessing geolocation positioning.Valid values:

-   true: Prevent access to geolocation positioning.
-   false: Do not prevent access to geolocation positioning.

</td></tr><tr><td>

isPhotoCollection Blocked

</td><td>

Boolean

</td><td>

Flag that indicates whether the host application should prevent NowChat from accessing the camera.Valid values:

-   true: Prevent access to the camera.
-   false: Do not prevent access to the camera.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - Android](../../concept/MobileSDKAndroidAPI.md)

## NowChatSdkCallbacks - didEndSessionWithId\(sessionId: String\)

Called when the chat screen is closed and the chat session ends.

**Note:** You must define the desired functionality for this callback by overriding the function as the default implementation simply writes the message "Chat session $sessionId ended." in the log.

<table id="table_izz_j4x_t2c" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sessionId

</td><td>

String

</td><td>

Sys\_id of the session that ended.Table: Conversation Session \[sys\_cs\_session\]

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows where to place your code to override the default functionality.

```
class SampleNowChatSDKCallbacks : NowChatSdkCallbacks {
  override fun didEndSessionWithId(sessionId: String) {
    Log.i("NowChat", "Chat session $sessionId ended.")
  }

//override other methods

}
```

## NowChatSdkCallbacks - loadUri\(uri: Uri, context: Context\)

Handles the specified URI, such as opening it in a webview, custom tab, or external browser.

|Name|Type|Description|
|----|----|-----------|
|uri|[Uri](https://developer.android.com/reference/kotlin/android/net/Uri.html)|URI to open.|
|context|[Context](https://developer.android.com/reference/kotlin/android/content/Context.html)|Application context.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
class SampleNowChatSDKCallbacks : NowChatSdkCallbacks {
  override fun loadUri(uri: Uri, context: Context) {

    // Open the uri in a webview
    val webview = WebView(context)
    webview.loadUrl(uri.toString())
  }

  // Override other methods
}
```

## NowChatSdkCallbacks - onExit\(exitCode: NowChatExitCode\)

Sets the result code to return when NowChat is exited.

This callback gets called when that full screen chat is closed and the user is returned back to the host application.

<table id="table_pj1_z1g_tpb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

exitCode

</td><td>

NowChatExitCode

</td><td>

Reason for exiting NowChat.Valid values:

-   ChatPluginNotInstalledError: Chat plugin not installed on instance.
-   SessionInitializationError: Unable to initialize session with instance.
-   UserExit: User exited using the up button or back button
-   Unknown: Any unknown reason.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
class SampleNowChatSDKCallbacks : NowChatSdkCallbacks {

  override fun onExit(exitCode: NowChatExitCode) {
    when (exitCode) {
      NowChatExitCode.UserExit -> Log.i("NowChat", "User exited using the up button or back button")
      NowChatExitCode.SessionInitializationError -> Log.i("NowChat", "Unable to initialize session with instance")
      NowChatExitCode.ChatPluginNotInstalledError -> Log.i("NowChat", " Chat plugin not installed on instance.")
      NowChatExitCode.Unknown -> Log.i("NowChat", "User exited for Unknown reason")
    }
  }

  // Override other methods
}
```

## NowChatSdkCallbacks - provideProgressView\(context: Context\)

Returns the view to display when the NowChat UI data is loading; typically a configured indeterminate progress bar.

|Name|Type|Description|
|----|----|-----------|
|context|[Context](https://developer.android.com/reference/kotlin/android/content/Context.html)|Application context to use to create the view.|

|Type|Description|
|----|-----------|
|[View](https://developer.android.com/reference/kotlin/android/view/View.html)|View that the NowChat service uses when loading.|

The following code example shows how to call this function.

```
class SampleNowChatSDKCallbacks : NowChatSdkCallbacks {
  override fun provideProgressView(context: Context): View? {
    return ProgressBar(context).apply {
      indeterminateTintList = ColorStateList.valueOf(
        MaterialColors.getColor(
          context,
          android.R.attr.colorPrimary,
          Color.BLACK)
      )
    }

    // Override other methods
  }
}
```

