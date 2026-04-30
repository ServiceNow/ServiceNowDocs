---
title: Implement Virtual and Live Agent chat
description: The Mobile SDK enables you to easily implement Virtual and Live Agent chat services within your iOS application.
locale: en-US
release: xanadu
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Implement Virtual and Live Agent chat

The Mobile SDK enables you to easily implement Virtual and Live Agent chat services within your iOS application.

You use the [NowChatService](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowChatService/concept/NowChatServiceiOSAPI.md#) API to create the chat user interface. Once the UI is created, you must then start the chat session, and then start the chat service. Similar to other Mobile SDK feature services, the NowChatService API provides two implementations for some of its methods, including the startChat\(\) method. One implementation returns a [Combine](https://developer.apple.com/documentation/combine) publisher, and the other calls a completion handler with the return results.

The following is a snippet from the sample application that shows how to initialize and start a chat UI and session.

```
// Create the chat UI
func makeChatScreen() -> UIViewController? {
  guard let chatService = chatService else { return nil }
  let result = chatService.makeChatUI(theme: CarrascoChatTheme(baseTheme: CarrascoTheme()))
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

Before you can leverage the chat functionality within your application, you must configure Virtual Agent within your ServiceNow instance. For details, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Passing context variables to Live Agent and Virtual Agent chat

You can pass chat context variables when starting a chat session by passing the **contextData** parameter in the [NowChatService - startChat\(contextData: \[String: Any\]?\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowChatService/concept/NowChatServiceiOSAPI.md#) or [NowChatService - startChat\(contextData: \[String: Any\]? = nil, \_ completion: @escaping \(Result&lt;Void, NowChatServiceError&gt;\)\)](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowChatService/concept/NowChatServiceiOSAPI.md#) functions. For additional information on chat context variables, see [Live agent chat context variables](https://www.servicenow.com/docs/access?context=live-agent-chat-context-vars&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

```
func startChat() {
  guard let chatService = chatService else {
    debugPrint("Chat service is invalid")
    viewState = makeViewState()
    return
  }
  let contextData = ["sys_id": "123456789", "table_name": "wm_task", "active": true] as [String: Any]
  chatService.startChat(contextData: contextData) { [weak self] result in
    if case .failure(let error) = result {
      debugPrint("Chat session initialization failed with error: \(error)")
      self?.resetChat()
    }
  }
}
```

## Theme the chat user interface

You can customize the colors of the Live Agent and Virtual Agent chat UI by passing a theme object in the makeChatUI\(\) call. For a list of all of the elements that you can customize, see [NowChatColoring protocol - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowChatColoring/concept/NowChatColoringiOSProtocol.md#). By default, the chat UI uses the **NowUIColor** theme for all NowSDK UI elements. Refer to the [NowChatThemeable protocol - iOS](../../../../../app-store/dev_portal/API_reference/MobileSDKiOS/NowChatThemeable/concept/NowChatThemeableiOSProtocol.md) for sample code snippets on how to apply a theme to your chat UI.

