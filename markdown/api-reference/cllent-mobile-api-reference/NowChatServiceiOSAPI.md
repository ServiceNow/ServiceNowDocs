---
title: NowChatService class - iOS
description: The NowChatService class provides Virtual and Live Agent chat capabilities.Initializes a new NowChatService instance.Creates a UIViewController that hosts the chat user interface.Shuts down the chat service, including any active chat sessions.Starts a chat session and executes a completion block after chat session has started.Subscribes to the unread message count listener.Unsubscribes from receiving the unread message count listener.Updates the NowChat UI theme with the specified UI theme. Use this function to update the chat UI theme after it has been initially set using the makeChatUI\(\) function such as when changing the theme from light to dark.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowChatService class- iOS

The NowChatService class provides Virtual and Live Agent chat capabilities.

Using this class you can start and stop chat services, start chat sessions, create a chat user interface, and subscribe/unsubscribe to unread messages.

<table class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

Configuration settings provided when the service was initialized.Data type: [NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)

</td></tr><tr><td>

instanceVersion

</td><td>

Version of the associated ServiceNow instance, such as vancouver or xanadu.Data type: String

</td></tr><tr><td>

networkService

</td><td>

Network service associated with this chat service.Data type: NetworkService

</td></tr><tr><td>

sessionType

</td><td>

Type of session.Possible values:

-   authenticated
-   guest
-   impersonated
-   unknown

Data type: SessionType

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowChatService - init\(configuration: NowServiceConfiguration, delegate: NowChatServiceDelegate?, coreServiceProvider: NowCoreServiceProviding? = nil\)

Initializes a new NowChatService instance.

<table id="table_jgv_vqp_npb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

configuration

</td><td>

[NowServiceConfiguration](../../NowServiceConfiguration/concept/NowServiceConfigurationiOSStruct.md#)

</td><td>

Configuration information needed to properly initialize the service.

</td></tr><tr><td>

delegate

</td><td>

Now​Chat​Service​Delegate

</td><td>

Optional. NowChat callback delegate object implementing the NowChatServiceDelegate protocol.Default: nil

</td></tr><tr><td>

coreServiceProvider

</td><td>

NowCoreServiceProviding

</td><td>

Optional. Object implementing the NowCoreServiceProviding protocol. Provides access to NowChat services.Default: nil

</td></tr></tbody>
</table>The following code example shows how to call this function.

```
guard let coreService = NowSDK.core() else {
  // Error with NowServiceError.sdkNotConfigured
  return
}

guard 
  let instanceUrl = URL(string: "http://sample.service-now.com"), 
  let serviceConfig = NowSDK.makeServiceConfiguration(for: instanceUrl) else {
    // Could not create service – 
    // NowServiceError.serviceConfigurationInvalid
    return
  }
    
let chatService = NowChatService(configuration: serviceConfig, delegate: delegate, coreServiceProvider: coreService)
```

## NowChatService - makeChatUI\(theme: NowChatThemeable, chatConfiguration: NowChatConfiguration? = nil\) -&gt; Result&lt;UIViewController, NowChatServiceError&gt;\)

Creates a `UIViewController` that hosts the chat user interface.

Although this function creates the chat UI, you must still initiate the chat session by calling the [startChat\(\)](NowChatServiceiOSAPI.md#) function. You should make this call as the chat UI becomes visible. For more details, see the associated sample application and the [Mobile SDK Developer Guide - iOS](../../../../../../integrate/guides/mobile_sdk/mobile_sdk-ios/concept/mobsdk-ios-overview.md).

|Name|Type|Description|
|----|----|-----------|
|theme|[NowChatThemeable protocol - iOS](../../NowChatThemeable/concept/NowChatThemeableiOSProtocol.md)|Theme information for the chat UI to create.|
|chatConfiguration|[NowChatConfiguration?](../../NowChatOptions/concept/NowChatOptionsiOS.md#)|Optional. Options to apply to the chat session.|

<table id="table_mkt_lvj_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Success: UIViewController object that contains the UI view controller configuration information.Failure: NowChatServiceError object.

Possible errors:

-   chatServiceInvalid
-   coreServiceInvalid
-   guestUserNotAllowed
-   invalidCredentials
-   noSession
-   unknown
-   unsupportedServer

</td></tr></tbody>
</table>The following code example shows how to call this function to create the chat UI.

```
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
```

## NowChatService - shutdown\(\)

Shuts down the chat service, including any active chat sessions.

After calling this function, the associated `NowChatService` is inactive and cannot be reused. To establish another chat session, create a new `NowChatService` instance by calling the NowChat.makeChatService\(\) function.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
private func resetChat() {
  chatService?.shutdown()
  chatService = nil
  initializeChatService()
  viewState = makeViewState()
}

func initializeChatService() {
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

func makeViewState() -> ViewState {
  ViewState(chatEnabled: chatService != nil,
    menuItems: menuItems)
}
```

## NowChatService - startChat\(contextData: \[String: Any\]? = nil, \_ completion: @escaping \(Result&lt;Void, NowChatServiceError&gt;\) -&gt; Void\)

Starts a chat session and executes a completion block after chat session has started.

<table id="table_tk1_bbk_npb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contextData

</td><td>

\[String: Any\]?

</td><td>

Optional. Dictionary containing chat context variables that are passed into the chat session.For additional information on chat context variables, see [Live agent chat context variables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/live-agent-chat-context-vars.md).

</td></tr><tr><td>

completion

</td><td>

Object

</td><td>

Completion block to execute after the chat session has started.

</td></tr></tbody>
</table><table id="table_uk1_bbk_npb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

void or String

</td><td>

Return values for the completion block:

-   Success: void
-   Error: NowChatServiceError

 Possible errors:

-   chatServiceInvalid
-   coreServiceInvalid
-   guestUserNotAllowed
-   invalidCredentials
-   noSession
-   unknown
-   unsupportedServer

</td></tr></tbody>
</table>The following code example shows how to call this function without context data.

```
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

func makeViewState() -> ViewState {
  ViewState(chatEnabled: chatService != nil,
    menuItems: menuItems)
}
```

The following code example shows how to call this function with context data.

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

func makeViewState() -> ViewState {
  ViewState(chatEnabled: chatService != nil,
    menuItems: menuItems)
}
```

## NowChatService - subscribeToUnreadMessageCount\(pollingInterval: TimeInterval, completion: @escaping \(Int\) -&gt; Void\)

Subscribes to the unread message count listener.

<table id="table_pv1_3ln_1qb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

pollingInterval

</td><td>

TimeInterval

</td><td>

Frequency at which to poll the web service for the unread chat message count.Unit: Seconds

</td></tr><tr><td>

completion

</td><td>

@escaping \(Int\) -&gt; Void\)

</td><td>

Completion handler to call to report the unread chat message count.**Int**: Number of unread chat messages.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
…
if viewModel.isPolling {
  viewModel.unsubscribeFromUnreadMessageCount()
  viewState.pollingInterval = ""
} else {
  viewModel.subscribeToUnreadMessageCount(pollingInterval: timeInterval)
}
…

func subscribeToUnreadMessageCount(pollingInterval: TimeInterval) {
  chatService.subscribeToUnreadMessageCount(pollingInterval: pollingInterval) { [weak self] count in
    self?.unreadMessageCount = count
  }
  isPolling = true
}
```

## NowChatService - unsubscribeFromUnreadMessageCount\(\)

Unsubscribes from receiving the unread message count listener.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
…
if viewModel.isPolling {
  viewModel.unsubscribeFromUnreadMessageCount()
  viewState.pollingInterval = ""
} else {
  viewModel.subscribeToUnreadMessageCount(pollingInterval: timeInterval)
}
…
func unsubscribeFromUnreadMessageCount() {
  chatService.unsubscribeFromUnreadMessageCount()
  isPolling = false
  unreadMessageCount = 0
}
```

## NowChatService - updateTheme\(theme: NowChatThemeable\)

Updates the NowChat UI theme with the specified UI theme. Use this function to update the chat UI theme after it has been initially set using the makeChatUI\(\) function such as when changing the theme from light to dark.

|Name|Type|Description|
|----|----|-----------|
|theme|[NowChatThemeable](../../NowChatThemeable/concept/NowChatThemeableiOSProtocol.md)|Theme to update the chat UI with.|

|Type|Description|
|----|-----------|
|None| |

The following code example shows how to update a light UI theme to the dark UI theme using the updateTheme\(\) function.

```
struct LightNowChatColoring: NowChatColoring {
  let nowUIColor: NowUIColoring = LightNowUIColor()
  let brand = UIColor.now_color(withHexString: "#032D42")
  let primary = UIColor.now_color(withHexString: "#00566E")
  let secondary = UIColor.now_color(withHexString: "#002832")
  let destructive = UIColor.now_color(withHexString: "#E52239")
  let textPrimary = UIColor.now_color(withHexString: "#10171A")
  let textSecondary = UIColor.now_color(withHexString: "#232E33")
  let textTertiary = UIColor.now_color(withHexString: "#37444A")
  let textActionable = UIColor.now_color(withHexString: "#ffffff")
  let screenHeaderText = UIColor.now_color(withHexString: "#ffffff")
  let backgroundPrimary = UIColor.now_color(withHexString: "#ffffff")
  let backgroundSecondary = UIColor.now_color(withHexString: "#F5F6F7")
  let backgroundTertiary = UIColor.now_color(withHexString: "#E2E5E7")
  let backgroundPrimaryActionable = UIColor.now_color(withHexString: "#10171A")
  let backgroundSecondaryActionable = UIColor.now_color(withHexString: "#232E33")
  let brandBackground = UIColor.now_color(withHexString: "#BDDEE7")
  let borderTertiary = UIColor.now_color(withHexString: "#d3d6dc")
  let separatorPrimary = UIColor.now_color(withHexString: "#859095")
  let separatorTertiary = UIColor.now_color(withHexString: "#CFD5D7")
  let alertCritical0 = UIColor.now_color(withHexString: "#F9C8CE")
  let alertCritical3 = UIColor.now_color(withHexString: "#E52239")
  let shadow = UIColor.now_color(withHexString: "#10171A")
  let linkPrimary = UIColor.now_color(withHexString: "#1955BE")
  let linkSecondary = UIColor.now_color(withHexString: "#113A82")
  let notification = UIColor.now_color(withHexString: "#E52239")
  let highlightBlue = UIColor.now_color(withHexString: "#C4DBFE")
  let highlightGray = UIColor.now_color(withHexString: "#DCDDDE")
}

struct DarkNowChatColoring: NowChatColoring {
  let nowUIColor: NowUIColoring = DarkNowUIColor()
  let brand = UIColor.now_color(withHexString: "#032D42")
  let primary = UIColor.now_color(withHexString: "#6CBBD0")
  let secondary = UIColor.now_color(withHexString: "#99C6D2")
  let destructive = UIColor.now_color(withHexString: "#E46775")
  let textPrimary = UIColor.now_color(withHexString: "#FFFFFF")
  let textSecondary = UIColor.now_color(withHexString: "#E2E5E7")
  let textTertiary = UIColor.now_color(withHexString: "#BCC3C7")
  let textActionable = UIColor.now_color(withHexString: "#050809")
  let backgroundPrimary = UIColor.now_color(withHexString: "#050809")
  let backgroundSecondary = UIColor.now_color(withHexString: "#161F23")
  let backgroundTertiary = UIColor.now_color(withHexString: "#1D272B")
  let backgroundPrimaryActionable = UIColor.now_color(withHexString: "#FFFFFF")
  let backgroundSecondaryActionable = UIColor.now_color(withHexString: "#BCC3C7")
  let brandBackground = UIColor.now_color(withHexString: "#002934")
  let separatorPrimary = UIColor.now_color(withHexString: "#97A2A6")
  let separatorTertiary = UIColor.now_color(withHexString: "#4F5C62")
  let borderTertiary = UIColor.now_color(withHexString: "#454d5b")
  let screenHeaderText = UIColor.now_color(withHexString: "#FFFFFF")
  let alertCritical0 = UIColor.now_color(withHexString: "#7B1D28")
  let alertCritical3 = UIColor.now_color(withHexString: "#E46775")
  let shadow = UIColor.now_color(withHexString: "#10171A")
  let notification = UIColor.now_color(withHexString: "#E46775")
  let linkPrimary = UIColor.now_color(withHexString: "#339EFC")
  let linkSecondary = UIColor.now_color(withHexString: "#70BBFD")
  let highlightBlue = UIColor.now_color(withHexString: "#004652")
  let highlightGray = UIColor.now_color(withHexString: "#363D3D")
}

struct LightNowChatTheme: NowChatThemeable {
  let color: NowChatColoring = LightNowChatColoring()
}

struct DarkNowChatTheme: NowChatThemeable {
  let color: NowChatColoring = DarkNowChatColoring()
}

func chatService(_ chatService: NowChat.NowChatService, systemThemeDidChange traitCollection: UITraitCollection) {
  // The systemThemeDidChange delegate method can be used to call updateTheme() to apply theme changes when the system theme changes.
  debugPrint("System Theme did change")
  chatService.updateTheme(theme: traitCollection.userInterfaceStyle == .dark ? DarkNowChatTheme() : LightNowChatTheme())
}
```

