---
title: Virtual Agent API features available in Store release 3.0.x
description: Virtual Agent API version 3.0.x provides access to more of the same features that are available in Virtual Agent and Agent Chat, including the ability to upload files from a private URL and synchronous handshake enhancements.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Using Virtual Agent API, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent API features available in Store release 3.0.x

Virtual Agent API version 3.0.x provides access to more of the same features that are available in Virtual Agent and Agent Chat, including the ability to upload files from a private URL and synchronous handshake enhancements.

## Ending abandoned Virtual Agent conversations

If a conversation is incomplete due to an error, Virtual Agent can ask the primary bot to take control. If the **takeControl** flag is **true**, Virtual Agent \(as the secondary bot\) will close the conversation automatically. If the primary bot wants to start a conversation, it can send the following action message: `"hi"/START_CONVERSATION`.

You can ask the primary bot to take control in the following situations:

-   Idle time out: Interaction State is `Closed Abandoned`. State Reason is `No Activity`.
-   Technical issues: Interaction State is `Closed Abandoned`. State Reason is `Bot issues`.
-   Invalid user input: Interaction State is `Closed Abandoned`. State Reason is `Invalid user input`.

To request that the primary bot take control, send the **takeControl** flag in the body of the payload to the primary bot with a value of **true**.

Example message payload:   

```
{​ 
   "requestId": "xxxx-xxxx-xxxx-xxxx",
   "clientSessionId": "xxx-xxx-xxx-xxx",
   "message": {
       "text":"invalid3",
       "typed":true
       }
   "body":[{
       "uiType":"OutputText",
       "group":"DefaultText",
       "value":"Sorry, I didn't get that. Could you help me by answering this?"
       },
       {
       "uiType":"Boolean",
       "group":"DefaultPicker",
       "required":true,
       "nluTextEnabled": false,
       "label":"Choose a value",
       "options":[
          {"label":"Yes"},
          {"label":"No"}
          ]
       }],
    "takeControl":true,
    "score":0
} 
```

## Improved Virtual Agent API response time

Virtual Agent API responses include parameters like Take Control and NLU Score. These parameters are processed while preparing the response.

Starting with version 3.9.0, you can exclude the Take Control and/or NLU Score parameters from the Virtual Agent API response to improve the response time.

To exclude Take Control and NLU Score parameters from the Virtual Agent API response, complete the following steps:

1.  Navigate to **All** &gt; **sys\_cs\_custom\_adapter\_property.list**.
2.  Search for **enable\_take\_control** and **send\_nlu\_score** properties.
3.  Set the value of **enable\_take\_control** property to false to exclude Take Control setting and **send\_nlu\_score** property to false to exclude NLU Score calculation while processing the response. These properties are set to true by default.

## Improved topic switching errors and troubleshooting

Topic switching may fail for any of the following reasons:

-   The request includes both the topic name and topic ID \(keyword topic discovery\) or the topic intent name and topic intent ID \(NLU topic discovery\). Specify one or the other.
-   The request includes an invalid topic or intent name or ID.
-   The topic/intent name or ID is valid, but Virtual Agent can't run it because it's inactive or not a topic. For example, if the name or ID refer to a topic block or custom control asset.
-   The requested topic is already running.
-   The requested topic is valid, but a security condition is preventing access. For example, the topic may not be permitted to run in the channel or some other access-control condition may apply.

If topic switching fails, Virtual Agent API responds in the following ways, whether you're using it synchronously or asynchronously:

-   If topic switching fails, the conversation is closed with a message stating that the conversation cannot continue. The conversation will no longer remain in an open state.
-   The previous request is marked as processed so that a new request can be made without waiting for a timeout.
-   The reason for the failure is logged in the system log table \(**Automated Test Framework** &gt; **System Logs** &gt; **Errors**\).

## Synchronous handshake enhancements

Starting with version 3.0.x, Virtual Agent API can transfer to a live agent synchronously. When a user or agent finishes a conversation, the transfer back to Virtual Agent is done synchronously as well. Some system messages and wait time messages are also sent synchronously.

To use synchronous transfer to a live agent, be aware of the following guidelines:

-   Configure the Virtual Agent response endpoint. Agent Chat messages will be delivered to the endpoint you specify.
-   You must manually turn off Notifications for the instance.
-   If you are using synchronous transfer to a live agent, Virtual Agent API sends the typing indicator if it is enabled:

    ```
    {
      "uiType": "ActionMsg",
      "actionType": "StartTypingIndicator",
    }
    
    ```

-   Topics that use the following features are not supported in synchronous mode: [file upload](../reference/va-user-inputs.md), the [Action utility](../reference/va-action.md), and the [Pause topic block](../reference/va-platform-topicblocks.md).

To disable these features and enable synchronous support, follow these steps:

1.  Navigate to **All** &gt; **sys\_cs\_channel.list**.
2.  Select the Bot to Bot record.
3.  Clear the **Enable Notifications** check box to disable it.
4.  If you will not be transferring to a live agent in synchronous mode, clear the **Support typing indicator** check box to disable it.
5.  Select the **Synchronous** check box.

    ![Bot to Bot channel configuration for Synchronous mode shows Enable Notifications and Support typing indicator boxes as unselected. The Synchronous box is selected.](../images/va-api-synchronous-mode.png "Bot to Bot channel with synchronous support enabled")

6.  Click **Update**.

## Support for action messages

In addition to passing messages to a ServiceNow® Virtual Agent secondary bot, the primary bot or chat client can pass messages to an agent through Agent Chat. Use the **action** parameter passed in the request body to specify how the content should be handled.

Virtual Agent API supports the following action message types:

<table id="table_g3b_cyp_dsb"><thead><tr><th>

actionType value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ChatSubHeader

</td><td>

Outbound message indicating one of the following occurred:-   Dynamic translation failed.
-   Live agent autopilot was initiated and completed.

</td></tr><tr><td>

StartSpinner

</td><td>

Outbound message that starts a spinner when a message is in the pending state due to asynchronous processes, such as AI Search or the profanity filter.

</td></tr><tr><td>

EndSpinner

</td><td>

Outbound message that stops the spinner that was sent previously.

</td></tr><tr><td>

StartTypingIndicatorActionMsg

</td><td>

Outbound message indicating that a user or agent has begun to type \(after an agent has accepted the chat\).

</td></tr><tr><td>

EndTypingIndicatorActionMsg

</td><td>

Outbound message indicating that a user or agent has stopped typing.

</td></tr><tr><td>

SubscribeToSupportQueue

</td><td>

Indicates that the conversation is set to the support queue.

</td></tr><tr><td>

SubscribeToChatPresence

</td><td>

Outbound message indicating that a live agent conversation has begun.

</td></tr><tr><td>

SwitchToLiveAgent

</td><td>

Outbound message indicating that a live agent has accepted the conversation.

</td></tr><tr><td>

SwitchToVirtualAgent

</td><td>

Outbound message indicating that the live agent session has ended, and the conversation is returned to Virtual Agent.

</td></tr><tr><td>

SwitchConversation

</td><td>

Outbound message indicating that a notification was sent. This creates a new conversation, so Virtual Agent switches to the new conversation.

</td></tr><tr><td>

System

</td><td>

Outbound message indicating one of the following:-   A live agent has entered the cat.
-   Either the live agent or the user closed the chat.
-   The conversation with a live agent has timed out.

</td></tr></tbody>
</table>## Support for silentMessage flag

A silent message is a message that does not require a response. If Virtual Agent receives a request with **silentMessage=true**, all subsequent bot messages are suppressed until Virtual Agent receives a request to turn off silent mode \(**silentMessage=false**\).

Example message payload from the primary bot:

```
{ 
   "token": "BOT_TOKEN",
   "botToBot": true,
   "clientSessionId": "884502214730301027f83ee4070f589a",
   "clientVariables": {},
   "requestId": "48450221d23030107300b7756770bc9b",
   "silentMessage": "true",
   "timestamp": 1623916324820,
   "timezone": "GMT",
   "userId": "abel.tuter",
   "emailId": "abel.tuter@example.com" 
}
```

**Note:** If **silentMessage=true**, notifications are not delivered.

## Secure file uploads from a private URL

Virtual Agent API supports file uploads up to 1 GB in size from a private URL. The primary bot must pass the user ID, optional provider application ID, and the name of the file. Observe the following guidelines:

-   Provider application ID is optional.
-   The user ID and provider application ID should be sent before the file name in the payload.
-   The end user must have a role specified in the **glide.attachment.role** property. For more information, see [Require a role to attach files](https://www.servicenow.com/docs/access?context=t_DisablingTheDragAndDropFeature&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   Basic or OAuth authentication is supported, but Message Authentication is not.

Example message payload from the primary bot:   

```
curl -X POST \
  https://instance.service-now.com/api/now/v1/cccif/media/upload \
  -H 'authorization: Basic YWRtaW46YWRtaW4=' \
  -H 'content-type: multipart/form-data; \
  -F user_id=xxxxxx \
  -F provider_application_id=optionalId \
  -F 'file=@SomeFile.png'
```

Virtual Agent API sends the following example JSON:

```
{
  "result": {
    "mediaUrl": "http://123.456.7.8:8080//api/now/v1/cs/media/string",
    "name":"imagefile.png",
    "state":"pending",
    "attachmentId":"abcdefghijklmno12345"
  }
}
```

## Support for transformation of Virtual Agent API request and response

Virtual Agent API supports transformation of request and response payloads to and fro Virtual Agent API. This is helpful in cases where the primary bot has a common response template across all secondary bots. See [Transform Virtual Agent API request and response](transform-virtual-agent-api-request-and-response.md) for more information.

## Support for configuring multiple provider applications

Virtual Agent API enables configuration of multiple provider applications to support use cases where there are multiple primary bots using Virtual Agent API and you need to distinguish between them. See [Configure multiple provider applications](configure-multiple-provider-applications.md) for more information.

## Support for Now Assist experience

Now Assist experience in Virtual Agent API offers generative AI skills across multiple provider channels. See [Enable Now Assist experience in Virtual Agent API](enable-now-assist-in-virtual-agent-experience-in-virtual-agent-api.md)for more information.

## Agent Chat enhancements in Virtual Agent API version 3.14.3

-   When the primary bot transfers a chat to a live agent, Virtual Agent API sends the agent Id, in addition to agent name and avatar, to the primary bot.
-   Virtual Agent API sends chat history from primary bot to live agent anywhere in the request during an ongoing conversation. This behavior is controlled by the following system property: allow\_storing\_history\_in\_ongoing-conversation. Set the value of the property to true to send chat history anywhere in the request.
-   Interaction record contains transcript of chat history along with timestamp of individual messages.

**Parent Topic:**[Using Virtual Agent API](virtual-agent-api.md)

