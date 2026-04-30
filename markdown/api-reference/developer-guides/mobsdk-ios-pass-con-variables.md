---
title: Passing context variables to Live Agent and Virtual Agent chat
description: You can pass chat context variables when starting a chat session by passing the contextData parameter.
locale: en-US
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Implement Virtual and Live Agent chat, Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Passing context variables to Live Agent and Virtual Agent chat

You can pass chat context variables when starting a chat session by passing the **contextData** parameter.

You can pass this value using the [NowChatService - startChat\(contextData: \[String: Any\]? = nil, \_ completion: @escaping \(Result&lt;Void, NowChatServiceError&gt;\) -&gt; Void\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowChatService/concept/NowChatServiceiOSAPI.md#) functions.

For additional information on chat context variables, see [Live agent chat context variables](https://www.servicenow.com/docs/access?context=live-agent-chat-context-vars&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

In addition, you can also pass an optional **NowChatConfiguration** parameter when starting a chat session to modify some of the behavior of NowChat.

-   **closePrompt**: Prompt text that appears before exiting a chat window. You define this prompt text through the following parameters:
    -   **header**: Nullable string value that appears on the prompt’s header.
    -   **message**: String value that appears on the prompt’s main body.
    -   **acceptButtonTitle**: String value that appears on the primary button of the prompt. This button closes the chat window.
    -   **declineButtonTitle**: String value that appears on the secondary button of the prompt. This button dismisses the prompt without closing the chat window.
-   **disabledFeatures**: List of NowChat features to disable. Refer to the NowChatConfiguration.Feature enum class for the list of features that you can disable.
-   **conversationOptions**: List of conversation options to apply to NowChat. Refer to the NowChatConvestation.ConversationOption enum class for the list of options that you can apply.
-   **uiConfiguration**: UIConfiguration value used to configure UI components in NowChat.

The following code example shows how to call this method:

```
// Close Button Type
func closeButtonText(title: String?) -> NowChatConfiguration.CloseButtonType? {
  guard let title else { return nil }
  return .text(title)
}  
  
func closeButtonImage(name imageName: String?) -> NowChatConfiguration.CloseButtonType? {
  guard let imageName,
  let buttonImage = UIImage(named: imageName) else { return nil }
  return .image(buttonImage)	
}


// Create the chat UI
func makeChatScreen() -> UIViewController? {
  guard let chatService = chatService else { return nil }
  let closePrompt = NowChatConfiguration.ClosePrompt(header: "Close Window",
    message: "Are you sure you want to close the chat window?",
    acceptButtonTitle: "Yes",
    declineButtonTitle: "No")     

  let attachmentUploadButton = NowChatConfiguration.AttachmentUploadButton(isVisible: false) // default isVisible = true         

  let chatConfiguration = NowChatConfiguration(closePrompt: closePrompt,
    disabledFeatures: [.startNewConversation],
    conversationOptions: [.forceNewConversation, .endConversationOnExit],
    uiConfiguration: NowChatConfiguration.UIConfiguration(closeButton: closeButtonImage(name: "arrow.left"), attachmentUploadButton: attachmentUploadButton))

  let result = chatService.makeChatUI(theme: CarrascoChatTheme(chatColors: ChatColors()), chatConfiguration: chatConfiguration)
         
  switch result {
    case .success(let chatViewController): 
      return chatViewController
    case .failure(let error):
      debugPrint("Chat screen creation failed with error: \(error)")
      return nil
  }
} 

// Start the chat session
func startChat() {
  guard let chatService = chatService else {
    debugPrint("Chat service is invalid")
    viewState = makeViewState()
    return
  } 
  chatService.startChat { [weak self] result in
    if case .failure(let error) = result {
      debugPrint("Chat session initialization failed with error: \(error)")
      self?.resetChat()
    }
  }
 }

// Initialize the chat service
private func initializeChatService() {
  NowChat.makeChatService(instanceUrl: instanceUrl, delegate: self) { [weak self] result in
    guard let self = self else { return }
    switch result {
      case .success(let service):
        self.chatService = service
      case .failure(let error):
        debugPrint("Creating the chat service failed with error: \(error)") 
    } 
    self.viewState = self.makeViewState()
  }
}
```

