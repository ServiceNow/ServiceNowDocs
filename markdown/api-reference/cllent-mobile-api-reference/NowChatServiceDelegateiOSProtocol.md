---
title: NowChatServiceDelegate protocol - iOS
description: The NowChatServiceDelegate protocol provides callbacks for notification of actions within the NowChatService such as a request to open a URL or dismiss the chat view controller.Callback that notifies the host application that the specified chat service received a request to open a URL. This callback is usually triggered by a user tapping on a link in the chat UI. It is the host application's responsibility to handle opening the URL or ignore the request.Callback that notifies the host application that the system chat theme changed.Callback that notifies the host application that the chat view controller was dismissed.Called when the chat screen is closed and the chat session ends.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatServiceDelegate protocol- iOS

The NowChatServiceDelegate protocol provides callbacks for notification of actions within the NowChatService such as a request to open a URL or dismiss the chat view controller.

**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowChatServiceDelegate - chatService\(\_chatService: NowChatService, didRequestOpenUrlurl: URL\)

Callback that notifies the host application that the specified chat service received a request to open a URL. This callback is usually triggered by a user tapping on a link in the chat UI. It is the host application's responsibility to handle opening the URL or ignore the request.

|Name|Type|Description|
|----|----|-----------|
|chatService|[NowChatService](../../NowChatService/concept/NowChatServiceiOSAPI.md#)|NowChatService object making the request.|
|didRequestOpenUrl url|URL|URL that the service has requested to open.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
func chatService(_ chatService: NowChatService, didRequestOpenUrl url: URL) {
  var updatedViewState = makeViewState()
  updatedViewState.urlToOpen = url
  viewState = updatedViewState
}
```

## NowChatServiceDelegate - chatService\(\_ chatService: NowChatService, systemThemeDidChange traitCollection: UITraitCollection\)

Callback that notifies the host application that the system chat theme changed.

|Name|Type|Description|
|----|----|-----------|
|chatService|[NowChatService](../../NowChatService/concept/NowChatServiceiOSAPI.md#)|NowChatService object making the request.|
|traitCollection|[UITraitCollection](https://developer.apple.com/documentation/uikit/uitraitcollection)|UITraitCollection that contains the new theme.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to override the systemThemeDidChange\(\) delegate function to call the updateTheme\(\) function to apply theme changes when the system theme changes.

```
func chatService(_ chatService: any SnowChat.ChatServiceProvider, systemThemeDidChange traitCollection: UITraitCollection) {

  /// The corresponding updateTheme() method can be called here to change the UI theme based on System Theme
  chatService.updateTheme(theme: traitCollection.userInterfaceStyle == .dark ? DarkNowChatTheme() : LightNowChatTheme())
  print(“System Theme Did Change)
}
```

## NowChatServiceDelegate - chatServiceViewControllerWasDismissed\(\_chatService: NowChatService\)

Callback that notifies the host application that the chat view controller was dismissed.

|Name|Type|Description|
|----|----|-----------|
|chatService|[NowChatService](../../NowChatService/concept/NowChatServiceiOSAPI.md#)|NowChatService object whose view controller was dismissed.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
func chatServiceViewControllerWasDismissed(_ chatService: NowChatService) {
  resetChat()
}
```

## NowChatServiceDelegate - didEndSessionWithId\(sessionId: String\)

Called when the chat screen is closed and the chat session ends.

**Note:** You can define the desired functionality for this callback by overriding the function.

<table id="table_j1t_hv2_52c" class="parameters"><thead><tr><th>

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
func chatService(_ chatService: NowChatService, didEndSessionWithId sessionId: String) {
  print("Chat Session ended with ID: \(sessionId)")
}
```

