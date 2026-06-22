---
title: Implement Virtual and Live Agent chat
description: The Mobile SDK enables you to easily implement Virtual and Live Agent chat services within your iOS application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/developer-guides/mobsdk-ios-imp-chat.html
release: zurich
product: Developer Guides
classification: developer-guides
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Mobile SDK Developer Guide - iOS, Developer guides, API implementation and reference]
---

# Implement Virtual and Live Agent chat

The Mobile SDK enables you to easily implement Virtual and Live Agent chat services within your iOS application.

You use the [NowChatService](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatServiceiOSAPI.md) API to create the chat user interface. Once the UI is created, you must then start the chat session, and then start the chat service. Similar to other Mobile SDK feature services, the NowChatService API provides two implementations for some of its methods, including the startChat\(\) method. One implementation returns a [Combine](https://developer.apple.com/documentation/combine) publisher, and the other calls a completion handler with the return results.

The following is a snippet from the sample application that shows how to initialize and start a chat UI and session.

```
func makeChatScreen() -> UIViewController? {
  guard let chatService = chatService else { return nil }
  let result = chatService.makeChatUI(theme: CarrascoChatTheme(chatColors: ChatColors())) 
  switch result {
    case .success(let chatViewController):
      return chatViewController
    case .failure(let error):
      debugPrint("Chat screen creation failed with error: \(error)")
      return nil 
  } 
}

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
```

Before you can leverage the chat functionality within your application, you must configure Virtual Agent within your ServiceNow instance. For details, see [Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/virtual-agent/virtual-agent-landing-page.md).

## Theme the chat user interface

You can customize the colors of the Live Agent and Virtual Agent chat UI by passing a theme object in the makeChatUI\(\) call. For a list of all of the elements that you can customize, see [NowChatColoring protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatColoringiOSProtocol.md). By default, the chat UI uses the **NowUIColor** theme for all NowSDK UI elements. Refer to the [NowChatThemeable protocol - iOS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/cllent-mobile-api-reference/NowChatThemeableiOSProtocol.md) for sample code snippets on how to apply a theme to your chat UI.

