---
title: NowChatOptions - iOS
description: The NowChatOptions class enables you to configure options, such as showing a prompt before closing a chat window or disable features while using chat, on a chat session.Creates and returns a ClosePrompt object based on the passed parameters. You then pass this object into the NowChatOptions\(\) method to configure the close prompt options within a chat session.Configures options for the current chat session. This method enables you to show a prompt before closing a chat window, disable features while using chat, and force a new chat conversation when the chat service starts.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatOptions - iOS

The NowChatOptions class enables you to configure options, such as showing a prompt before closing a chat window or disable features while using chat, on a chat session.

**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowChatOptions - ClosePrompt\(header: String?, message: String, acceptButtonTitle: String, declineButtonTitle: String\)

Creates and returns a ClosePrompt object based on the passed parameters. You then pass this object into the NowChatOptions\(\) method to configure the close prompt options within a chat session.

<table id="table_xb2_dcl_kbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

header

</td><td>

String

</td><td>

Text to display on the prompt's header.If you don't want to display a prompt header, pass "nil".

</td></tr><tr><td>

message

</td><td>

String

</td><td>

Text to display as the prompt's main text.

</td></tr><tr><td>

acceptButtonTitle

</td><td>

String

</td><td>

Text to display on the prompt's primary button for closing the chat window.

</td></tr><tr><td>

declineButtonTitle

</td><td>

String

</td><td>

Text to display on the prompt's secondary button that dismisses the prompt.

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
func makeChatScreen() -> UIViewController? {
  guard let chatService = chatService else { return nil }
  let closePrompt = NowChatOptions.ClosePrompt(
    header: "Close Window",
    message: "Are you sure you want to close the chat window?",
    acceptButtonTitle: "Yes",
    declineButtonTitle: "No")

  let disabledFeatures = [.startNewConversation]
    
  let chatOptions = NowChatOptions(closePrompt: closePrompt,
    disabledFeatures: disabledFeatures,
    forceNewConversation: true)
    
  let result = chatService.makeChatUI(theme: CarrascoChatTheme(chatColors: ChatColors()), chatOptions: chatOptions)
    
  switch result {
  case .success(let chatViewController):
    return chatViewController
  case .failure(let error):
    return nil
  }
}
```

## NowChatOptions - NowChatOptions\(closePrompt: ClosePrompt?, disabledFeatures: \[Feature\]?, forceNewConversation: Bool\)

Configures options for the current chat session. This method enables you to show a prompt before closing a chat window, disable features while using chat, and force a new chat conversation when the chat service starts.

<table id="table_lpt_3lk_kbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

closePrompt

</td><td>

[ClosePrompt](NowChatOptionsiOS.md#) object

</td><td>

Prompt to display before closing the associated chat window.If you don't want to display a close prompt, pass "nil".

</td></tr><tr><td>

disabledFeatures

</td><td>

\[Feature\]

</td><td>

List of chat features to disable within the current chat session.Valid value:

-   startNewConversation: Hide/disable the **StartNew Conversation** button that appears in a chat window.

The available chat features are defined in the NowChatOptions.Feature enum class.

If you don't want to disable any features, pass "nil".

</td></tr><tr><td>

forceNewConversation

</td><td>

Boolean

</td><td>

Flag that indicates whether to force a new chat conversation when the chat session starts. Any current conversations are closed.Valid values:

-   true: Start a new chat conversation; a new chat window opens.
-   false: Don't start a new chat conversation; use the existing chat window.

Default: false

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|chatOptions|Returns a chatOptions object that you can pass in the [NowChatService - makeChatUI\(theme: NowChatThemeable, chatOptions: NowChatOptions? = nil\) -&gt; Result&lt;UIViewController, NowChatServiceError&gt;\)](../../NowChatService/concept/NowChatServiceiOSAPI.md#) method.|

The following code example shows how to call this function.

```
func makeChatScreen() -> UIViewController? {
  guard let chatService = chatService else { return nil }
  let closePrompt = NowChatOptions.ClosePrompt(
    header: "Close Window",
    message: "Are you sure you want to close the chat window?",
    acceptButtonTitle: "Yes",
    declineButtonTitle: "No")

  let disabledFeatures = [.startNewConversation]
    
  let chatOptions = NowChatOptions(closePrompt: closePrompt,
    disabledFeatures: disabledFeatures,
    forceNewConversation: true)
    
  let result = chatService.makeChatUI(theme: CarrascoChatTheme(chatColors: ChatColors()), chatOptions: chatOptions)
    
  switch result {
  case .success(let chatViewController):
    return chatViewController
  case .failure(let error):
    return nil
  }
}
```

