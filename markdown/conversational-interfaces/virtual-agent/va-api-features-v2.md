---
title: Virtual Agent API features available in Store release 2.0.x
description: Virtual Agent API version 2.0.x provides access to more of the same features that are available in Virtual Agent and Agent Chat, including rich control support and notifications.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 14
breadcrumb: [Using Virtual Agent API, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent API features available in Store release 2.0.x

Virtual Agent API version 2.0.x provides access to more of the same features that are available in Virtual Agent and Agent Chat, including rich control support and notifications.

## Support for additional rich controls

Virtual Agent API now supports the following rich controls.

-   **Boolean controls**

    Boolean controls return responses as strings \(either **Yes** or **No**\) for easier localization.

    For more information about topic localization, see [Localizing Virtual Agent conversations](localize-va-topic.md).

    Virtual Agent API sends the following example JSON for a boolean control:

    ```
    {
      "requestId": "asd2423-wrr434-weruyt-1234567",
      "clientSessionId": "",
      "nowSessionId": "",
      "message": {
        "text": "7a36412253a13010ff59ddeeff7b12fb",
        "typed": false,
        "clientMessageId": "ABC-123"
      },
      "userId": "beth.anglin",
      "body": [
        {
          "uiType": "Boolean",
          "group": "DefaultPicker",
          "required": true,
          "nluTextEnabled": false,
          "label": "Sample Response for boolean control",
          "options": [
            {
              "label": "Yes"
            },
            {
              "label": "No"
            }
          ]
        }
      ],
      "score": 1
    }
    ```

-   **Custom controls**

    Topics that use custom controls are now supported. For more information about custom controls, see [Customizing Virtual Agent with custom controls](custom-controls.md).

-   **Table bot response controls**

    Topics that use table bot response controls are now supported. For more information, see [Table bot response control](../reference/table-bot-response.md).

    All records are returned from Virtual Agent API at once. Virtual Agent will wait for a response from the API client to send the next control. Use the **paginationBreak** property to display records in chunks to the user. For example, if **paginationBreak** is set to 10, the user will see 10 records at a time. When the client is ready to move to the next control, it should send **DONE**.

    Virtual Agent API sends the following example JSON for a table bot response control:

    ```
    {
      "requestId": "asd2423-wrr434-weruyt-1234567",
      "clientSessionId": "",
      "nowSessionId": "",
      "message": {
        "text": "Yes",
        "typed": false,
        "clientMessageId": "ABC-123"
      },
      "userId": "beth.anglin",
      "body": [
        {
          "uiType": "OutputTable",
          "group": "DefaultOutputTable",
          "label": "Sample Table Rich control",
          "headers": [
            "Number",
            "Short description"
          ],
          "data": [
            [
              "INC0000005",
              "CPU load high for over 10 minutes"
            ],
            [
              "INC0000015",
              "I can't launch my VPN client since the last software update"
            ],
            [
              "INC0000025",
              "Need to add more memory to laptop"
            ],
            [
              "INC0000035",
              "Reset my password"
            ],
            [
              "INC0000055",
              "SAP Sales app is not accessible"
            ],
            [
              "INC0009005",
              "Email server is down."
            ]
          ],
          "paginationBreak": 10,
          "totalSearchResultsCount": 6,
          "navigationBtnLabel": "Click for more"
        }
      ],
      "score": 1
    }
    ```

-   **HTML bot response controls**

    Topics that use HTML bot response controls are now supported. For more information, see [HTML bot response control](../reference/va-html-output.md).

    Virtual Agent API sends the following example JSON for an HTML bot response control:

    ```
    {
      "requestId": "asd2423-wrr434-weruyt-1234567",
      "clientSessionId": "",
      "nowSessionId": "",
      "message": {
        "text": "Yes",
        "typed": false,
        "clientMessageId": "ABC-123"
      },
      "userId": "beth.anglin",
      "body": [
        {
          "uiType": "OutputHtml",
          "group": "DefaultOutputHtml",
          "style": "inline",
          "height": 100,
          "width": 100,
          "value": "<html> <body> Sample Response for Html control </body> </html> ",
          "imageUrl": null,
          "imageHeight": 0,
          "imageWidth": 0,
          "links": null
        },
        {
          "uiType": "InputText",
          "group": "DefaultText",
          "required": true,
          "nluTextEnabled": false,
          "label": "some text",
          "maskType": "NONE"
        }
      ],
      "score": 1
    }
    ```

-   **Multi-response bot response controls**

    Topics that use multi-response bot response controls are now supported. For more information, see [Multi-response bot response control](../reference/va-multi-flow-output.md).

    Virtual Agent API sends the following example JSON for a multi-response bot response control:

    ```
    {
      "requestId": "asd2423-wrr434-weruyt-1234567",
      "clientSessionId": "",
      "nowSessionId": "",
      "message": {
        "text": "Done",
        "typed": false,
        "clientMessageId": "ABC-123"
      },
      "userId": "beth.anglin",
      "body": [
        {
          "uiType": "MultiPartOutput",
          "group": "DefaultMultiPartOutput",
          "navigationBtnLabel": "Click for more",
          "content": {
            "uiType": "OutputText",
            "value": "Text response from multiflow control example",
            "maskType": "NONE"
          }
        }
      ],
      "score": 1
    }
    ```

-   **Rich text support**

    Topics that use rich text are now supported. Rich text includes bold or italicized text, hyperlinks, bulleted lists, and emojis.


## Additional Agent Chat features

The Virtual Agent API now supports the following features when transferring to Agent Chat.

-   **Pass agent name and avatar**

    When the primary bot transfers a chat to a live agent, Virtual Agent can send the agent name and avatar to the primary bot. To enable this, activate **Agent names and avatars** in Agent Chat settings.

    An example message payload might look like this:

    ```
    { 
    "requestId":"f42f3550-5b44-4cde-aa52-9b6756b3131c", 
    "clientSessionId":"U94CSJLEN", 
    "message":{ 
    "text":"Live Agent support.", 
    "typed":true 
    }, 
    "userId":"U94CSJLEN", 
    "body":[ 
    { 
    "uiType":"OutputText", 
    "group":"DefaultText", 
    "agentInfo":{ 
    "sentFromAgent":true, 
    "agentName":"Beth Anglin", 
    "agentAvatar":"ee4eebf30a0004d963b5c5ac0d734dc4.iix?t=small" 
    }, 
    "value":"Thank you for contacting support. I am looking into your question now and will be with you shortly." 
    } 
    ], 
    "agentChat":true, 
    "score":1 
    }
    ```

    For more information, see [Configure Agent Chat](../../conversational-interfaces/task/ac-configure-agent-chat.md).

-   **Live agent wait time**

    When transferring to a live agent, the primary bot can receive the wait time and display this to the user. To enable this, select **Wait Time** in the **Live chat wait status** field in Agent Chat settings. The **spinnerType** value is set to **wait\_time**. If the **Live chat wait status** is set to **None**, the **spinnerType** value is **none**.

    Virtual Agent API sends the following example JSON in the **body** parameter of the payload.

    ```
    {
    "uiType":"ActionMsg",
    "actionType":"StartSpinner",
    "spinnerType":"wait_time",
    "message":"Routing you to a live agent...",
    "waitTime":"8 Seconds"
    }
    
    ```

    For more information, see [Configure Agent Chat](../../conversational-interfaces/task/ac-configure-agent-chat.md).

-   **Send chat history from the primary bot to Virtual Agent**

    The primary bot can pass chat history to a live agent so that the agent can see the context of the conversation.

    Virtual Agent converts the message history to HTML and then to an image.

    -   The converted image is sent to the live agent as the first message of the chat.
    -   The primary bot should send the message history in the first request. In any other request after the first request, the message history payload will be ignored.
    -   Only text messages are supported.
    -   The primary bot can pass any URL as a value in the text message, but the live agent can only view it as part of the image. The live agent will not be able to click the link.
    Example message payload:

    ```
    {​ 
          "value": "Help me with password reset",​ 
          "displayName": "able",​ 
          "type": "text"​ 
          "isBotMessage": false,​ 
        } 
    ```

    **Note:** In the previous example, **type** is case sensitive and should have a value of **text**.


## Enriched requests from the primary bot

The Virtual Agent API now supports the following requests from the primary bot.

-   **System parameters and context variables**

    The primary bot can pass system parameters and context variables as input, and Virtual Agent will honor these  parameters. System parameters such as **liveagent\_devicetype**, **liveagent\_requester\_session\_language**, **liveagent\_topic**, **topic**, **live\_agent\_only**, and **liveagent\_devicetimezone** are supported. Custom context variables and Agent Chat context variables are also supported.

    Example message payload:

    ```
    {​ 
    "requestId": "f42f3550-5b44-4cde-aa52-xxxxxxxxxx",​ 
    "clientSessionId": "xxxxxxxxxx",​ 
    "token": "abcd",​ 
    "message": {​ 
        "text": "Test",​ 
        "typed": true​ 
    },​ 
    "contextVariables": {​ 
           "requester_session_language": "es"​ 
    },​ 
    "userId": ""abel.tuter",​ 
    "emailId": "abel.tuter@example.com"​ 
    }​ 
    
    ```

    For more information, see [Live agent chat context variables](../reference/live-agent-chat-context-vars.md) and [Configure context variables for storing chat-related information](../../conversational-interfaces/task/ac-configure-context-variables.md).

-   **User timezone**

    Set the user’s timezone by passing it in the request payload. Once set, that timezone setting is retained until it is reset.

    Example message payload:

    ```
    {​ 
    
        "requestId": "xxxxxx-xxxxxx-xxxx-xxxx-xxxxxxxxxx",​ 
        "clientSessionId": "xxxxxxxx-xxxx",​ 
        "token": "xxxxx",​ 
        "action" : "SET_USER_TIMEZONE",​ 
        "userId": "able.tuter",​ 
        "emailId": "abel.tuter@example.com",​ 
         "timezone":"Asia/Kolkata"​ 
    } 
    ```

    When using this functionality, consider the following:

    -   The conversation must be open \(current\) in order to convert date and time to the user's timezone.
    -   The primary bot must send date and time in one of the following formats:
        -   Timezone name. For example, **Asia/Kolkata** or **America/New\_York**.
        -   Date Time 24-hour format. For example: **YYYY-MM-DD HH:MM:SS**
    -   The Virtual Agent API uses the timezone specified by the primary bot, even if the timezone it sets differs from the value stored in the \[sys\_user\] table.
    -   To set the user timezone, send the **SET\_TIMEZONE** action. If the timezone name is not valid, the timezone value defaults to UTC time. For example, **2021-02-16 20:13:13**.

## Support for node skipping

Virtual Agent API supports skipping a node if it is designed to do so in the topic. For example, in Virtual Agent Designer, you can designate a user input control as skippable in the **Advanced** &gt; **Hide or skip this node** area of the property sheet.

![In this example, the Script option is selected and defines when the user can skip the node.](../images/va-api-skip-node-support.png "Condition or script that allows the user to skip the node")

For more information about defining a node as skippable, see [Virtual Agent Designer user input controls](../reference/va-user-inputs.md).

If a node is marked as skippable, the bot will present that option to the user. If the user skips it, the primary bot should pass the skip command as depicted in the following example.

```
{
"requestId": "f42f3550-5b44-4cde-aa52-9b6756b3131c",
"clientSessionId": "835607",
"token": "snow",
"message": {
"text": "_skip_",
"typed": false
},
"emailId": "beth.anglin@example.com",
"userId": "beth.anglin"
}
```

## Synchronous handshake support

**Note:** These requirements apply to version 2.0.x of the Virtual Agent API. For greater synchronous handshake functionality, upgrade to version 3.0.x, which supports live agent transfer and other enhancements. For details, see [Synchronous handshake enhancements](va-api-features-v3.md#synchronous_support_enhancements).

When enabled, Virtual Agent delivers responses to the primary bot synchronously. If you want to enable communication with Virtual Agent in synchronous mode, you must manually turn off the following features in order for the handshake to work:

-   Agent Chat
-   Notifications
-   Typing indicators

**Note:** Topics that use the following features are not supported in synchronous mode: [file upload](../reference/va-user-inputs.md), the [Action utility](../reference/va-action.md), and the [Pause topic block](../reference/va-platform-topicblocks.md).

To disable these features and enable synchronous support, follow these steps:

1.  Exclude the Bot to Bot channel from Agent Chat.
    1.  Navigate to **All**, and then enter `sys_properties.list` in the filter.
    2.  Select the **com.glide.cs.exclude.liveagent.support** system property to open it.
    3.  Add **Bot To Bot** to the **Value** field.

        ![The Value field for the system property contains "Alexa,Google Assistant,Bot to Bot." These channels are excluded from supporting Agent Chat.](../images/va-api-exclude-liveagent-btb.png "Exclude the Bot To Bot channel from Agent Chat")

    4.  Click **Update**.
2.  Navigate to **All**, and then enter `sys_cs_channel.list` in the navigation filter.
3.  Select the Bot to Bot record.
4.  Clear the **Enable Notifications** check box to disable it.
5.  Clear the **Support typing indicator** check box to disable it.
6.  Select the **Synchronous** check box.

    ![Bot to Bot channel configuration for Synchronous mode shows Enable Notifications and Support typing indicator boxes as unselected. The Synchronous box is selected.](../images/va-api-synchronous-mode.png "Bot to Bot channel with synchronous support enabled")

    **Note:** If the **Synchronous** field is not visible, you can [configure the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) to show it.

7.  Click **Update**.

## Notifications support

Use Virtual Agent API to send the following types of notifications in the Bot to Bot channel when it is enabled in asynchronous mode:

-   Simple: Text-only notifications. Simple notifications are delivered as soon as they arrive.
-   Image Card: An image that is uploaded to the server or specified with a URL.
-   Record Card: Specified columns from a record in a table.
-   Actionable: Provides the user with the opportunity to perform certain actions. Actionable notifications are queued. The user can retrieve them on demand by sending the **Show Notification** command.

For more information, see [Configuring Virtual Agent notifications](configuring-va-notifications.md).

Virtual Agent API sends the following example JSON for a simple notification:

```
{
  "requestId": "asd2423-wrr434-weruyt-1234567",
  "clientSessionId": "",
  "nowSessionId": "",
  "message": {
    "text": "Done",
    "typed": false,
    "clientMessageId": "ABC-123"
  },
  "userId": "beth.anglin",
  "body": [
    {
      "uiType": "OutputCard",
      "group": "DefaultOutputCard",
      "templateName": "Notification",
      "data": "{\"sys_id\":null,\"recordDisplayValue\":null,\"messageHeading\":\"[Heading]A notification has arrived. You can continue the conversation after viewing the notification.\",\"imageUrl\":null,\"tableLabel\":null,\"enableLink\":false,\"message\":\"[message]A notification has arrived. You can continue the conversation after viewing the notification.\",\"fields\":[],\"table_name\":null,\"url\":\"http://192.168.1.9:8080/null.do?sys_id=null\"}"
    }
  ],
  "completed": true,
  "score": 1
}
```

Virtual Agent API sends the following example JSON for an Image Card notification:

```
{
  "requestId": "asd2423-wrr434-weruyt-1234567",
  "clientSessionId": "",
  "nowSessionId": "",
  "message": {
    "text": "Done",
    "typed": false,
    "clientMessageId": "ABC-123"
  },
  "userId": "beth.anglin",
  "body": [
    {
      "uiType": "OutputCard",
      "group": "DefaultOutputCard",
      "templateName": "Notification",
      "data": "{\"sys_id\":null,\"recordDisplayValue\":null,\"messageHeading\":\"[Heading]A notification has arrived. You can continue the conversation after viewing the notification.\",\"imageUrl\":\"http://xxxxxx.service-now.com/2b2d0d2653a13010ff59ddeeff7b120d.iix\",\"tableLabel\":null,\"enableLink\":false,\"message\":\"[message]A notification has arrived. You can continue the conversation after viewing the notification.\",\"fields\":[],\"table_name\":null,\"url\":\"http://192.168.1.9:8080/null.do?sys_id=null\"}"
    }
  ],
  "completed": true,
  "score": 1
}
```

Virtual Agent API sends the following example JSON for a Record Card notification:

```
{
  "requestId": "asd2423-wrr434-weruyt-1234567",
  "clientSessionId": "",
  "nowSessionId": "",
  "message": {
    "text": "Done",
    "typed": false,
    "clientMessageId": "ABC-123"
  },
  "userId": "beth.anglin",
  "body": [
    {
      "uiType": "OutputCard",
      "group": "DefaultOutputCard",
      "templateName": "Notification",
      "data": "{\"sys_id\":\"552c48888c033300964f4932b03eb092\",\"recordDisplayValue\":\"INC0010112\",\"messageHeading\":\"[Heading]A notification has arrived. You can continue the conversation after viewing the notification.\",\"imageUrl\":null,\"tableLabel\":\"Incident\",\"enableLink\":true,\"message\":\"[message]A notification has arrived. You can continue the conversation after viewing the notification.\",\"fields\":[{\"fieldLabel\":\"Number\",\"fieldValue\":\"INC0010112\"},{\"fieldLabel\":\"Short description\",\"fieldValue\":\"Assessment : ATF Assessor\"}],\"table_name\":\"incident\",\"url\":\"http://192.168.1.9:8080/incident.do?sys_id=552c48888c033300964f4932b03eb092\"}"
    }
  ],
  "completed": true,
  "score": 1
}
```

Notifications for the Bot to Bot channel are disabled by default. To enable them, do the following:

1.  Navigate to **All**, and then enter `sys_cs_channel.list` in the navigation filter.
2.  Open the Bot to Bot record.

    If prompted, enable editing on the record.

3.  Select the **Enable Notifications** check box.
4.  Click **Update**.

Admins can limit the number of recipients per notification by modifying the **com.glide.cs.per\_notification\_user\_limit** property. The default value is 1000.

## Topic switching using the topic name

In addition to using the topic ID or topic intent ID to switch topics, you can use the topic or topic intent name. It is recommended that you only send either the topic ID or the topic name. Currently, if either is incorrect or if the bot is already in the specified topic, Virtual Agent does not send any response. Usage depends on the mode you are using, as follows:

-   NLU topic discovery: Use the topic intent name or ID.
-   Keyword topic discovery: Use the topic name or ID.

The primary bot can send the **SWITCH** action along with the topic name to switch directly to a  particular  topic.

Example message payload:   

```
{​ 
   "requestId": "xxxx-xxxx-xxxx-xxxx",
   "clientSessionId": "xxx-xxx-xxx-xxx",
   "action":"SWITCH",
   "topic":{
​      "name": "Topic Name"​
   },​
   "userId": "beth"​  
} 
```

## Typing indicator support

You can enable typing indicators for users and live agents. Currently, typing indicators are displayed as follows:

-   Displayed to the agent when the user is typing
-   Displayed to the user when the bot is preparing a response

When the typing indicator is enabled, Virtual Agent API sends the **StartTypingIndicator** and **EndTypingIndicator**  actions in the response payload. For example:

```
{​ 
        "uiType":"ActionMsg",​ 
        "actionType":"StartTypingIndicator"​ 
} ​ 
```

To send the user typing indicator to a live agent, the client should send  the **TYPING**  action. When the user finishes typing, the  client should  send the  **VIEWING**  action.​ For example:

```
{​ 
    "requestId": "xxxxxx-xxxxxx-xxxx-xxxx-xxxxxxxxxx",​ 
    "clientSessionId": "xxxxxxxx-xxxx",​ 
    "action": "TYPING/VIEWING",​ 
    "userId": "able.tuter",​ 
    "emailId": "abel.tuter@example.com",​ 
    "timezone":"Asia/Kolkata"​ 
}​ 
```

To enable typing indicators, follow these steps.

1.  Navigate to **All**, and then enter `sys_cs_channel.list` in the navigation filter.
2.  Select the Bot to Bot record.
3.  Select the **Support typing indicator** check box.
4.  Click **Update**.

**Parent Topic:**[Using Virtual Agent API](virtual-agent-api.md)

