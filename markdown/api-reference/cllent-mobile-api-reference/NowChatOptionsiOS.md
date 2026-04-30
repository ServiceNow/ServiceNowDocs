---
title: NowChatConfiguration - iOS
description: The NowChatConfiguration class enables you to configure options on a chat session, such as showing a prompt before closing a chat window, disabling features while using chat, applying different conversation options when using chat, and configuring UI components in NowChat.Configures options for the current chat session. This method enables you to show a prompt before closing a chat window, disable features while using chat, apply different conversation options when using chat, and configure UI components in NowChat.Defines the UI configurations to apply to the upload attachment button that appears next to the text input while talking with a live agent.Creates and returns a ClosePrompt object based on the passed parameters. You then pass this object into the NowChatConfiguration\(\) constructor to configure the close prompt options within a chat session.Creates and returns a UIConfiguration object based on the passed parameters. You then pass this object into the NowChatConfiguration\(\) constructor to configure UI components in NowChat.
locale: en-US
release: yokohama
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Mobile SDK API reference - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatConfiguration - iOS

The NowChatConfiguration class enables you to configure options on a chat session, such as showing a prompt before closing a chat window, disabling features while using chat, applying different conversation options when using chat, and configuring UI components in NowChat.

**Parent Topic:**[Mobile SDK API reference - iOS](../../concept/MobileSDKiOSAPI.md)

## NowChatConfiguration - NowChatConfiguration\(closePrompt: ClosePrompt?, disabledFeatures: \[Feature\]? = nil, conversationOptions: \[ConversationOption\]? = nil, uiConfiguration: UIConfiguration? = nil\)

Configures options for the current chat session. This method enables you to show a prompt before closing a chat window, disable features while using chat, apply different conversation options when using chat, and configure UI components in NowChat.

<table id="table_lpt_3lk_kbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

closePrompt

</td><td>

[ClosePrompt?](NowChatOptionsiOS.md#)

</td><td>

Prompt to display before closing the associated chat window.Call the [NowChatConfiguration.ClosePrompt\(\)](NowChatOptionsiOS.md#) struct to define the value of this parameter.

For example:

```
closePrompt = NowChatConfiguration.ClosePrompt(
  header = nil,
  message = "Are you sure you want to leave?",
  acceptButtonTitle = "Yes",
  declineButtonTitle = "No"
)
```

If you don't want to display a close prompt, omit the **closePrompt**argument in the NowChatConfiguration\(\) call.

</td></tr><tr><td>

disabledFeatures

</td><td>

\[NowChatConfiguration.​Feature\]?

</td><td>

List of chat features to disable within the current chat session.Valid value: startNewConversation - Hide/disable the **StartNew Conversation** button that appears in a chat window.

The available chat features are defined in the NowChatOptions.Feature enum class.

For example:

```
let disabledFeatures: [NowChatConfiguration.Feature]? = [.startNewConversation]
```

If you don't want to disable any features, omit the **disabledFeatures** argument in the NowChatConfiguration\(\) call.

</td></tr><tr><td>

conversationOptions

</td><td>

\[NowChatConfiguration.​ConversationOption\]?

</td><td>

List of conversation options to apply to NowChat. Valid values:

-   endConversationOnExit: Ongoing conversation is terminated when exiting the NowChat window.
-   forceNewConversation: Forces a new chat conversation when NowChat starts.

The available conversation options are defined in the NowChatConfiguration.ConversationOption enum class.

For example:

```
let conversationOptions: [NowChatConfiguration.ConversationOption]? = [.endConversationOnExit, .forceNewConversation]
```

If you don't want to disable any features, omit the **conversationOptions** argument in the NowChatConfiguration\(\) call.

</td></tr><tr><td>

uiConfiguration

</td><td>

[UIConfiguration?](NowChatOptionsiOS.md#)

</td><td>

UIConfiguration values to use to configure UI components in NowChat. Valid values:

-   attachmentUploadButton: Configuration for the `AttachmentUploadButton` that is shown next to the text input while talking with a live agent.
-   closeButton: Configuration for the `CloseButton` used for back navigation on the NowChat toolbar.

For example:

```
let attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible: false) // Default isVisible = true

// Configure close button as Text
let closeButtonText: NowChatConfiguration.CloseButtonType = .text("Exit")
let uiConfigurationWithText = NowChatConfiguration.UIConfiguration(closeButton: closeButtonText)

// Configure close button as image   
let buttonImage = UIImage(systemName: "arrow.left.circle") ?? nil 
var closeButtonImage: NowChatConfiguration.CloseButtonType?   
if let buttonImage { closeButtonImage = .image(buttonImage) }   
  let uiConfigurationWithImage = NowChatConfiguration.UIConfiguration(closeButton: closeButtonImage)
```

If you want to use custom images instead of the provided system images, the images should be between 22 to 44 pixels in width and 30 pixels in height, for optimal resolution.

To use the default for either **AttachmentUploadButton** or **CloseButtonType**, omit the associated button from the UIConfiguration argument.

To use the default for both buttons, omit the **UIConfiguration** parameter in the NowChatConfiguration\(\) call.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|NowChatConfiguration|Returns a NowChatConfiguration object that you can pass when calling the [NowChatConfiguration\(\)](NowChatOptionsiOS.md#) method.|

The following code example shows how to call this method to configure the chat UI.

```
func makeChatScreen() -> UIViewController? {
  let closePrompt = NowChatConfiguration.ClosePrompt(
    header: nil,
    message: "Are you sure you want to leave?",
    acceptButtonTitle: "Yes",
    declineButtonTitle: "No"
  )

  let disabledFeatures: [NowChatConfiguration.Feature]? = [.startNewConversation]

  let conversationOptions: [NowChatConfiguration.ConversationOption]? = [.endConversationOnExit, .forceNewConversation] 

  let attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible: false) 

  // Configure close button as Text
  let closeButtonText: NowChatConfiguration.CloseButtonType = .text("Exit")
  let uiConfigurationWithText = NowChatConfiguration.UIConfiguration(closeButton: closeButtonText, attachmentUploadButton: attachmentUploadButton) 
 
  // Configure close button as image 
  let buttonImage = UIImage(systemName: "arrow.left.circle") ?? nil 

  var closeButtonImage: NowChatConfiguration.CloseButtonType?
  if let buttonImage {
    closeButtonImage = .image(buttonImage)
  }
  let uiConfigurationWithImage = NowChatConfiguration.UIConfiguration(closeButton: closeButtonImage, attachmentUploadButton: attachmentUploadButton)    

  let chatConfiguration = NowChatConfiguration(closePrompt: closePrompt, 
    disabledFeatures: disabledFeatures,
    conversationOptions: conversationOptions,
    uiConfiguration: uiConfigurationWithImage)

  let result = chatService.makeChatUI(theme: CarrascoChatTheme(chatColors: ChatColors()), chatConfiguration: chatConfiguration)  

  switch result { 
    case .success(let chatViewController):
      return chatViewController
    case .failure(let error):
      debugPrint("Chat screen creation failed with error: \(error)")
      return nil
  }
}
```

## NowChatConfiguration - AttachmentUploadButton\(isVisible: Boolean = true\)

Defines the UI configurations to apply to the upload attachment button that appears next to the text input while talking with a live agent.

AttachmentUploadButton is a struct of the NowChatConfiguration class.

<table id="table_tym_brc_fdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

isVisible

</td><td>

Boolean

</td><td>

Flag that indicates the visibility of the upload attachment button.Valid values:

-   true: Upload attachment button is visible.
-   false: Upload attachment button is hidden.

Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to hide the AttachmentUploadButton.

```
func makeChatScreen() -> UIViewController? {
  let attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible: false)
  let uiConfigurationWithAttachmentButton = NowChatConfiguration.UIConfiguration(attachmentUploadButton: attachmentUploadButton)         

  let chatConfiguration = NowChatConfiguration(uiConfiguration: uiConfigurationWithAttachmentButton) 

  let result = chatService.makeChatUI(theme: CarrascoChatTheme(chatColors: ChatColors()), chatConfiguration: chatConfiguration) 

  switch result {
    case .success(let chatViewController):
      return chatViewController
    case .failure(let error):
      debugPrint("Chat screen creation failed with error: \(error)")
      return nil
  }
}
```

## NowChatConfiguration - ClosePrompt\(header: String?, message: String, acceptButtonTitle: String, declineButtonTitle: String\)

Creates and returns a ClosePrompt object based on the passed parameters. You then pass this object into the NowChatConfiguration\(\) constructor to configure the close prompt options within a chat session.

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

## NowChatConfiguration - UIConfiguration\(closeButton: CloseButtonType? = nil, attachmentUploadButton: AttachmentUploadButton? = nil\)

Creates and returns a UIConfiguration object based on the passed parameters. You then pass this object into the NowChatConfiguration\(\) constructor to configure UI components in NowChat.

UIConfiguration\(\) is a struct of the NowChatConfiguration class.

<table id="table_fwq_z3j_fdc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

closeButton

</td><td>

CloseButtonType?

</td><td>

Configuration for the `CloseButtonType` that appears on the NowChat toolbar and is used for back navigation.Valid values:

-   image \(UIImage\): Create a close button with an image.
-   text \(String\): Create a close button as text. Use this to pass a custom name for the back button.

The available `CloseButtonType` options are defined in the NowChatConfiguration.CloseButtonType enum class.

For example:

```
func makeChatScreen() -> UIViewController? {
  // Configure close button as Text
  let closeButtonText: NowChatConfiguration.CloseButtonType = .text("Exit")
  let uiConfigurationWithText = NowChatConfiguration.UIConfiguration(closeButton: closeButtonText)

  // Configure close button as image
  let buttonImage = UIImage(systemName: "arrow.left.circle") ?? nil

  var closeButtonImage: NowChatConfiguration.CloseButtonType?
  if let buttonImage {
    closeButtonImage = .image(buttonImage)
  }
  let uiConfigurationWithImage = NowChatConfiguration.UIConfiguration(closeButton: closeButtonImage)

  let chatConfiguration = NowChatConfiguration(uiConfiguration: uiConfigurationWithImage) 

  // or 
  // let chatConfiguration = NowChatConfiguration(uiConfiguration: uiConfigurationWithText) 

```

</td></tr><tr><td>

attachmentUploadButton

</td><td>

[AttachmentUploadButton?](NowChatOptionsiOS.md#)

</td><td>

Configuration for the `AttachmentUploadButton` that is shown next to the text input while talking with a live agent.Call the [NowChatConfiguration - AttachmentUploadButton\(isVisible: Boolean = true\)](NowChatOptionsiOS.md#) method to define the value of this parameter.

For example:

```
let attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible: false)
let uiConfigurationWithAttachmentButton = NowChatConfiguration.UIConfiguration(attachmentUploadButton: attachmentUploadButton)         

let chatConfiguration = NowChatConfiguration(uiConfiguration: uiConfigurationWithAttachmentButton)
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Object|UI configuration object|

The following code example shows how to call the UIConfiguration\(\) subclass to set the chat UI configuration.

```
func makeChatScreen() -> UIViewController? {

  let attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible: false)

  // Configure close button as image
  let buttonImage = UIImage(systemName: "arrow.left.circle") ?? nil

  var closeButtonImage: NowChatConfiguration.CloseButtonType?
  if let buttonImage {
    closeButtonImage = .image(buttonImage)
  }
  let uiConfigurationWithImage = NowChatConfiguration.UIConfiguration(closeButton: closeButtonImage, attachmentUploadButton: attachmentUploadButton)         

  let chatConfiguration = NowChatConfiguration(uiConfiguration: uiConfigurationWithImage) 

  let result = chatService.makeChatUI(theme: CarrascoChatTheme(chatColors: ChatColors()), chatConfiguration: chatConfiguration)

  switch result { 
    case .success(let chatViewController):
      return chatViewController
    case .failure(let error):
      debugPrint("Chat screen creation failed with error: \(error)")
      return nil
  }
}
```

