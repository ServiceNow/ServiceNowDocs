---
title: Supported features in Virtual Agent API
description: You can use the Virtual Agent API to integrate many of the same features that are available in Virtual Agent and Agent Chat into your chat environment. Feature support varies depending on your ServiceNow release and the store app version number of the Virtual Agent API.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
breadcrumb: [Explore, Virtual Agent API, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Supported features in Virtual Agent API

You can use the Virtual Agent API to integrate many of the same features that are available in Virtual Agent and Agent Chat into your chat environment. Feature support varies depending on your ServiceNow release and the store app version number of the Virtual Agent API.

For information about the request and response templates for Virtual Agent API, as well as examples of common use cases, see [Virtual Agent Bot Integration API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/bot-api.md).

## Version 4.3.0

**Support for premium chat in Virtual Agent API**

## Version 4.1.1

**Support for synthesized response in Virtual Agent API**

-   With synthesized response enabled through Now Assist experience, Virtual Agent API sends the response with citations to the primary bot. Citations are included in **citations** parameter along with separate citation links.
-   Here's an example JSON for synthesized response with citations and citation links:

    ```
    {
      "clientSessionId": "va_api_conv_16875",
      "score": 1,
      "interactionId": "0dce3e37ffe1f610f71affffffffff8a",
      "requestId": "1765195564288",
      "streamActive": false,
      "streamState": "END",
      "message": {
        "typed": true,
        "text": "what is spam?"
      },
      "body": [
        {
          "feedback": {
            "messageId": "dcde7a7739e1f610beed69f9e5960355",
            "feedbackEnabled": true
          },
          "maskType": "NONE",
          "citations": [
            {
              "citationHref": "http://10.160.66.170:8080/sp?id=kb_article&sys_id=24d9243187032100deddb882a2e3ec33",
              "sysId": "24d9243187032100deddb882a2e3ec33",
              "icon": "sn_nowassist_va.source-kb-article.png",
              "header": "KB article",
              "description": "What is Spam?",
              "index": 0,
              "source": "internal",
              "category": "kb",
              "citationLabel": "What is Spam?",
              "table": "kb_knowledge",
              "citationRef": "[1]"
            },
            {
              "citationHref": "http://10.160.66.170:8080/sp?id=kb_article&sys_id=0b48fd75474321009db4b5b08b9a71c2",
              "sysId": "0b48fd75474321009db4b5b08b9a71c2",
              "icon": "sn_nowassist_va.source-kb-article.png",
              "header": "KB article",
              "description": "How to Deal with Spam",
              "index": 1,
              "source": "internal",
              "category": "kb",
              "citationLabel": "How to Deal with Spam",
              "table": "kb_knowledge",
              "citationRef": "[2]"
            },
            {
              "citationHref": "http://10.160.66.170:8080/sp?id=kb_article&sys_id=3020c9b1474321009db4b5b08b9a712d",
              "sysId": "3020c9b1474321009db4b5b08b9a712d",
              "icon": "sn_nowassist_va.source-kb-article.png",
              "header": "KB article",
              "description": "What are phishing scams and how can I avoid them?\n\t\t",
              "index": 2,
              "source": "internal",
              "category": "kb",
              "citationLabel": "What are phishing scams and how can I avoid them?\n\t\t",
              "table": "kb_knowledge",
              "citationRef": "[3]"
            }
          ],
          "streamId": "4fcef677ffe1f610f71affffffffffee",
          "uiType": "OutputText",
          "messageId": "dcde7a7739e1f610beed69f9e5960355",
          "relatedList": [],
          "value": "Spam refers to unsolicited commercial email (UCE) or unsolicited bulk email (UBE), commonly known as junk email. It often includes phishing scams, foreign bank scams, pyramid schemes, quack health products, pornographic site ads, offers for bulk emailing services, chain letters, and pirated software. Most reputable marketers do not use spam for advertising. To reduce spam:\n\n- Do not reply to spam, as it confirms your address to spammers.\n- Be cautious when sharing your email address online.\n- Adjust browser security settings to limit personal information exposure.\n- Avoid forwarding chain mail, as most are hoaxes.\n- Use judgment when unsubscribing or responding to unfamiliar sources \u200b[1]\u200b\u200b[2]\u200b.\n\nPhishing scams, a dangerous form of spam, attempt to trick you into revealing personal information by pretending to be legitimate organizations. Always verify requests for sensitive information and avoid clicking suspicious links \u200b[3]\u200b.\n\n[1] [What is Spam?](http://10.160.66.170:8080/sp?id=kb_article&sys_id=24d9243187032100deddb882a2e3ec33)\n[2] [How to Deal with Spam](http://10.160.66.170:8080/sp?id=kb_article&sys_id=0b48fd75474321009db4b5b08b9a71c2)\n[3] [What are phishing scams and how can I avoid them?\n\t\t](http://10.160.66.170:8080/sp?id=kb_article&sys_id=3020c9b1474321009db4b5b08b9a712d)",
          "group": "DefaultText"
        }
      ],
      "userId": "admin",
      "clientVariables": {
        "bot": {
          "id": "va-bot-12345"
        },
        "channelId": "postman"
      }
    }
    ```

-   For more information, see [Enable synthesized response in Virtual Agent API](../task/va-api-enable-synthesized-response.md).

**Support for agentic response in Virtual Agent API**

-   Virtual Agent API supports agentic response through Now Assist experience. With agentic response enabled in Virtual Agent API, the output messages are shown to the user as loading or processing.
-   Virtual Agent API sends message to the primary bot through a new **DynamicLoader** parameter.
-   Here's an example JSON for agentic response:

    ```
    {
      "clientSessionId": "va_api_conv_16875",
      "score": 1,
      "interactionId": "0dce3e37ffe1f610f71affffffffff8a",
      "requestId": "1765195564288",
      "message": {
        "typed": true,
        "text": "what is spam?"
      },
      "body": [
        {
          "progressMessages": [
            {
              "message": "Searched for relevant documents and actions",
              "status": "COMPLETED"
            },
            {
              "message": "Generated the response",
              "status": "COMPLETED"
            }
          ],
          "actionType": "DynamicLoader",
          "defaultHeader": "View AI Steps",
          "uiType": "ActionMsg",
          "parentMessageId": "87cef677ffe1f610f71affffffffff4d",
          "header": "View AI Steps",
          "messageId": "87cef677ffe1f610f71affffffffff4d",
          "shouldUpdateParentMessage": true
        }
      ],
      "userId": "admin",
      "clientVariables": {
        "bot": {
          "id": "va-bot-12345"
        },
        "channelId": "postman"
      }
    }
    ```


**Support for response streaming in Virtual Agent API**

-   Virtual Agent API supports response streaming through Now Assist experience. To learn more, see [Enable Now Assist experience in Virtual Agent API](../task/enable-now-assist-in-virtual-agent-experience-in-virtual-agent-api.md).

    **Note:** The primary bot must pass the streaming responses to the end user. For more information, see [Chat streaming responses](streaming-responses-requestor.md).

-   Virtual Agent API supports the following states for response streaming:
    -   START

        ```
        {
          "clientSessionId": "va_api_conv_16875",
          "requestId": "1762864530268",
          "streamActive": true,
          "streamState": "START",
          "message": {
            "typed": true,
            "text": "what is spam?"
          },
          "body": [
            {
              "streamId": "cb928c9f53097e10f71a6dc230e5e639",
              "uiType": "StreamStart",
              "streamSequence": 1,
              "value": "Looking into your request"
            }
          ],
          "userId": "admin",
          "clientVariables": {
            "bot": {
              "id": "va-bot-12345"
            },
            "channelId": "postman"
          }
        }
        ```

    -   INPROGRESS

        ```
        {
          "clientSessionId": "va_api_conv_16875",
          "requestId": "1762864530268",
          "streamActive": true,
          "streamState": "INPROGRESS",
          "message": {
            "typed": true,
            "text": "what is spam?"
          },
          "body": [
            {
              "streamId": "cb928c9f53097e10f71a6dc230e5e639",
              "uiType": "StreamChunk",
              "streamSequence": 2,
              "value": "Spam refers to unsolicited commercial email (UCE) or unsolicited bulk email (UBE), commonly known as junk email. It often"
            }
          ],
          "userId": "admin",
          "clientVariables": {
            "bot": {
              "id": "va-bot-12345"
            },
            "channelId": "postman"
          }
        }
        ```

    -   END

        ```
        {
          "clientSessionId": "va_api_conv_16875",
          "score": 1,
          "interactionId": "d592c89f53097e10f71a6dc230e5e68c",
          "requestId": "1762864530268",
          "streamActive": false,
          "streamState": "END",
          "message": {
            "typed": true,
            "text": "what is spam?"
          },
          "body": [
            {
              "feedback": {
                "messageId": "6f92cc9f34097e108001c582b67b2a1f",
                "feedbackEnabled": true
              },
              "maskType": "NONE",
              "citations": [
                {
                  "citationHref": "http://192.168.29.27:8080/sp?id=kb_article&sys_id=24d9243187032100deddb882a2e3ec33",
                  "sysId": "24d9243187032100deddb882a2e3ec33",
                  "icon": "sn_nowassist_va.source-kb-article.png",
                  "header": "KB article",
                  "description": "What is Spam?",
                  "index": 0,
                  "source": "internal",
                  "category": "kb",
                  "citationLabel": "What is Spam?",
                  "table": "kb_knowledge",
                  "citationRef": "[1]"
                },
                {
                  "citationHref": "http://192.168.29.27:8080/sp?id=kb_article&sys_id=0b48fd75474321009db4b5b08b9a71c2",
                  "sysId": "0b48fd75474321009db4b5b08b9a71c2",
                  "icon": "sn_nowassist_va.source-kb-article.png",
                  "header": "KB article",
                  "description": "How to Deal with Spam",
                  "index": 1,
                  "source": "internal",
                  "category": "kb",
                  "citationLabel": "How to Deal with Spam",
                  "table": "kb_knowledge",
                  "citationRef": "[2]"
                }
              ],
              "streamId": "cb928c9f53097e10f71a6dc230e5e639",
              "uiType": "OutputText",
              "messageId": "6f92cc9f34097e108001c582b67b2a1f",
              "relatedList": [],
              "value": "Spam refers to unsolicited commercial email (UCE) or unsolicited bulk email (UBE), commonly known as junk email. It often includes phishing scams, foreign bank scams, pyramid schemes, \"get rich quick\" offers, quack health products, ads for pornographic sites, offers for bulk emailing services, chain letters, and pirated software. To reduce spam:\n\n- Do not reply to spam, as it confirms your address to spammers.\n- Be cautious when sharing your email address online or with companies.\n- Adjust browser security settings to limit personal information exposure.\n- Avoid forwarding chain mail, as most are hoaxes \u200b[1]\u200b\u200b[2]\u200b.\n\n[1] [What is Spam?](http://192.168.29.27:8080/sp?id=kb_article&sys_id=24d9243187032100deddb882a2e3ec33)\n[2] [How to Deal with Spam](http://192.168.29.27:8080/sp?id=kb_article&sys_id=0b48fd75474321009db4b5b08b9a71c2)",
              "group": "DefaultText"
            }
          ],
          "userId": "admin",
          "clientVariables": {
            "bot": {
              "id": "va-bot-12345"
            },
            "channelId": "postman"
          }
        }
        ```

-   Enable streaming in Virtual Agent API by the following configuration:
    1.  Ensure that **Allow response streaming** is selected in Now Assist in Virtual Agent. To learn more, see [Enable additional chat features](../../now-assist-in-va/task/additional-chat-features.md).
    2.  Navigate to **All** and enter `sys_now_assist_channel_config.list` in the navigation filter.
    3.  In the Now Assist Channel configuration \[now\_assist\_channel\_config\] table, set the **Streaming Ready** field value to `true` for Bot to Bot device.

        ![Set the Streaming Ready field value to true for Bot to Bot device.](../images/va-api-streaming.png "Now Assist Channel Configs table")


**Support for new outbound authentication**

-   Virtual Agent API is now configured to use Workflow Studio REST step instead of earlier ServiceNow AI Platform REST message.
-   To learn more, see [Configure output response REST endpoint and outbound authentication for the Virtual Agent API \(v4.1 or above\)](../task/configure-response-endpoint-auth-va-api.md).

## Version 4.0.0

-   Virtual Agent API updates the message text and the delivery status for messages between the live agent and the primary bot.
-   Virtual Agent API sends the interaction Id and message Id \(agent Id for conversations with the live agent\) in response to the primary bot.

    Interaction record stores the **clientSessionId** parameter sent by the supported third-party chat application \(or the primary bot\) for each of its conversations with the end user. To learn more, see [Configure interaction record to store clientSessionId in Virtual Agent API](../task/va-api-interaction-record-third-party-chat.md).

-   The chat history from the primary bot's conversation with the end user includes timestamp of individual messages. The live agents can now see this chat history either in individual messages or in a single block. To learn more, see [Configure to support chat history in Virtual Agent API](../task/va-api-support-chat-history.md). You can customize your Agent chat interface by setting a logo for the primary bot that appears in the chat history. For more information, see [Setting logo for the primary bot in Virtual Agent API](../task/va-api-support-set-logo.md).

## Version 3.0.x

**Agent Chat enhancements in version 3.14.3**

-   When the primary bot transfers a chat to a live agent, Virtual Agent API sends the agent Id, in addition to agent name and avatar, to the primary bot.
-   Virtual Agent API sends chat history from primary bot to live agent anywhere in the request during an ongoing conversation. This behavior is controlled by the following system property: allow\_storing\_history\_in\_ongoing-conversation. Set the value of the property to true to send chat history anywhere in the request.
-   Interaction record contains transcript of chat history along with timestamp of individual messages.

**Support for Now Assist experience**

-   Now Assist experience in Virtual Agent API offers generative AI skills across multiple provider channels.
-   For more information, see [Enable Now Assist experience in Virtual Agent API](../task/enable-now-assist-in-virtual-agent-experience-in-virtual-agent-api.md).

**Support for configuring multiple provider applications**

-   Virtual Agent API enables configuration of multiple provider applications to support use cases where there are multiple primary bots using Virtual Agent API and you need to distinguish between them.
-   For more information, see [Configure multiple provider applications](../task/configure-multiple-provider-applications.md).

**Support for transformation of Virtual Agent API request and response**

-   Virtual Agent API supports transformation of request and response payloads to and fro Virtual Agent API. This is helpful in cases where the primary bot has a common response template across all secondary bots.
-   For more information, see [Transform Virtual Agent API request and response](../task/transform-virtual-agent-api-request-and-response.md).

**Secure file uploads from a private URL**

-   Virtual Agent API supports file uploads up to 1 GB in size from a private URL. The primary bot must pass the user ID, optional provider application ID, and the name of the file. Observe the following guidelines:
    -   Provider application ID is optional.
    -   The user ID and provider application ID should be sent before the file name in the payload.
    -   The end user must have a role specified in the **glide.attachment.role** property. For more information, see [Require a role to attach files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_DisablingTheDragAndDropFeature.md).
    -   Basic or OAuth authentication is supported, but Message Authentication is not.
-   Example message payload from the primary bot:   

    ```
    curl -X POST \
      https://instance.service-now.com/api/now/v1/cccif/media/upload \
      -H 'authorization: Basic YWRtaW46YWRtaW4=' \
      -H 'content-type: multipart/form-data; \
      -F user_id=xxxxxx \
      -F provider_application_id=optionalId \
      -F 'file=@SomeFile.png'
    ```

-   Virtual Agent API sends the following example JSON:

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


**Support for silentMessage flag**

-   A silent message is a message that does not require a response. If Virtual Agent receives a request with **silentMessage=true**, all subsequent bot messages are suppressed until Virtual Agent receives a request to turn off silent mode \(**silentMessage=false**\).
-   Example message payload from the primary bot:

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


**Support for action messages**

-   In addition to passing messages to a ServiceNow® Virtual Agent secondary bot, the primary bot or chat client can pass messages to an agent through Agent Chat. Use the **action** parameter passed in the request body to specify how the content should be handled.
-   Virtual Agent API supports the following action message types:

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
</table>
**Synchronous handshake enhancements**

-   Virtual Agent API can transfer to a live agent synchronously. When a user or agent finishes a conversation, the transfer back to Virtual Agent is done synchronously as well. Some system messages and wait time messages are also sent synchronously.
-   To use synchronous transfer to a live agent, be aware of the following guidelines:
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
-   To disable these features and enable synchronous support, see [Enable synchronous support in Virtual Agent API](../task/virtual-agent-api-enable-synchronous-support.md).

**Improved topic switching errors and troubleshooting**

-   Topic switching may fail for any of the following reasons:
    -   The request includes both the topic name and topic ID \(keyword topic discovery\) or the topic intent name and topic intent ID \(NLU topic discovery\). Specify one or the other.
    -   The request includes an invalid topic or intent name or ID.
    -   The topic/intent name or ID is valid, but Virtual Agent can't run it because it's inactive or not a topic. For example, if the name or ID refer to a topic block or custom control asset.
    -   The requested topic is already running.
    -   The requested topic is valid, but a security condition is preventing access. For example, the topic may not be permitted to run in the channel or some other access-control condition may apply.
-   If topic switching fails, Virtual Agent API responds in the following ways, whether you're using it synchronously or asynchronously:
    -   If topic switching fails, the conversation is closed with a message stating that the conversation cannot continue. The conversation will no longer remain in an open state.
    -   The previous request is marked as processed so that a new request can be made without waiting for a timeout.
    -   The reason for the failure is logged in the system log table \(**Automated Test Framework** &gt; **System Logs** &gt; **Errors**\).

**Improved Virtual Agent API response time**

-   Virtual Agent API responses include parameters like Take Control and NLU Score. These parameters are processed while preparing the response.
-   Starting with version 3.9.0, you can exclude the Take Control and/or NLU Score parameters from the Virtual Agent API response to improve the response time.
-   To exclude Take Control and NLU Score parameters from the Virtual Agent API response, complete the following steps:
    1.  Navigate to **All** &gt; **sys\_cs\_custom\_adapter\_property.list**.
    2.  Search for **enable\_take\_control** and **send\_nlu\_score** properties.
    3.  Set the value of **enable\_take\_control** property to false to exclude Take Control setting and **send\_nlu\_score** property to false to exclude NLU Score calculation while processing the response. These properties are set to true by default.

**Ending abandoned Virtual Agent conversations**

-   If a conversation is incomplete due to an error, Virtual Agent can ask the primary bot to take control. If the **takeControl** flag is **true**, Virtual Agent \(as the secondary bot\) will close the conversation automatically. If the primary bot wants to start a conversation, it can send the following action message: `"hi"/START_CONVERSATION`.
-   You can ask the primary bot to take control in the following situations:
    -   Idle time out: Interaction State is `Closed Abandoned`. State Reason is `No Activity`.
    -   Technical issues: Interaction State is `Closed Abandoned`. State Reason is `Bot issues`.
    -   Invalid user input: Interaction State is `Closed Abandoned`. State Reason is `Invalid user input`.
-   To request that the primary bot take control, send the **takeControl** flag in the body of the payload to the primary bot with a value of **true**.
-   Example message payload:   

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


**Parent Topic:**[Exploring Virtual Agent API](explore-virtual-agent-api.md)

