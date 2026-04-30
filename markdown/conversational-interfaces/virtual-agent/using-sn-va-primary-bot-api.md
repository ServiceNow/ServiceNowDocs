---
title: Using Virtual Agent Bot Interconnect in your configuration
description: Use Virtual Agent Bot Interconnect to create a unified chat experience across multiple channels. You can support secondary bots, such as Google Dialogflow, Microsoft Power Virtual Agents, and ServiceNow Virtual Agent.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Virtual Agent, Bot interconnect, Google Dialogflow, Microsoft, Power, Pro, unified, chat, experience, multiple, channels]
breadcrumb: [Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Using Virtual Agent Bot Interconnect in your configuration

Use Virtual Agent Bot Interconnect to create a unified chat experience across multiple channels. You can support secondary bots, such as Google Dialogflow, Microsoft Power Virtual Agents, and ServiceNow® Virtual Agent.

Virtual Agent Bot Interconnect functions as the primary bot in a diverse chat environment. It can help you reduce complexity and create a unified chat experience for your end users. Virtual Agent Bot Interconnect gives your end users access to multiple channels and a wide variety of enterprise tasks that are available from ServiceNow.

Bot Interconnect provides the following benefits:

-   Ready integration with third-party bots such as Google Dialogflow and Microsoft Power Virtual Agents.
-   Easy integration with ServiceNow Virtual Agent bots on other instances.
-   The ability to add any other third-party bot as a secondary bot in the system.
-   User authentication and account linking in Bot Interconnect.
-   Intent discovery in Bot Interconnect across all skills that are supported by the primary and secondary bots.
-   LLM topic conversations across primary and secondary bots
-   Conversations occur with one bot at a time.
-   Bot Interconnect provides a common conversation model and data storage, which unifies reporting and analytics.

**Note:** The Virtual Agent Bot Interconnect requires a Pro license similar to that of Virtual Agent.

## Supported Controls

All input controls and bot response controls are supported.

## Features and default behavior

-   **Language support**

    Responses in Bot Interconnect are not translated. Bot Interconnect passes the user language to the secondary bot and expects the secondary bot to return any responses in that language. For example, if the primary bot has a German-speaking user and the secondary instance is localized in German, then German responses are returned to the primary bot.

-   **Timeout value from the secondary bot**

    The timeout value is the maximum time the primary bot waits for a response from the secondary bot. You can pass a custom timeout value \(in milliseconds\) in the Bot Interconnect Topic Block properties to override this.

    1.  Select the **Bot Interconnect Topic Block** node in the shell topic on your primary instance.
    2.  In the **Additional Params \(String\)** area, select the script icon ![Script icon.](../images/icon-script.png).
    3.  Add the following script:

        ```
        return JSON.stringify({ timeout : 30000 })
        ```

        In this example, 30000 equals 30 seconds.

    4.  Save and publish the topic.
-   **Closed conversations**

    Conversations are closed on the secondary bot when a user closes the conversation on Bot Interconnect or when the Bot Interconnect conversation times out.

    **Note:** Conversations always remain open in Microsoft Power Virtual Agents.

-   **Debug logs**

    To enable debug logs in the Bot Interconnect instance, set the **sn\_va\_bot\_ic.bot\_interconnect.enable.logging** system property to **true**. You will see a conversation ID attached to most logs, as well as the file name.

-   **Pass output from the secondary bot topic to the primary bot**

    You can apply custom logic to the output of the secondary bot conversation in the Bot Interconnect shell topic.

-   **Support for custom transformation maps**

    Developers can pass a custom transformation map using the getTransformerMap method. A custom transformation map lets you override the default transformation logic.

    Example in the DialogflowInboundTransformer script include for Google Dialogflow:

    ```
    /** Custom transformation map based on control types in DialogFlow messenger **/
    
    getTransformationMap: function() {
    	return {
    		‘text’: ‘transformText’,
    		‘info’: ‘transformInfoCards2’,
    		‘description’: ‘transformDescription’,
    		‘button’: ‘transformButtonLink’,
    		‘image’: ‘transformImage’,
    		‘chips’: ‘transformChips’,
    
    		/* fallback logic in case VA API response format is mentioned in Dialogflow custom response payload */
    		‘servicenow’: ‘transformServiceNowResponse’
    	};
    },
    
    ```

    In this example, `text`, `info`, `description`, and so forth are the control types that correspond to the secondary bot. The specified method \(such as transformText is called to do the transformation for the control type. For each secondary bot response, Virtual Agent uses the getControlType method to return the control type specified in the transformation map for the secondary bot message. The inbound transformer in Google Dialogflow provides a good example for how to use this.

    If the transformation method called does not exist, Virtual Agent API logs it as an error.

-   **Live agent connection**

    You can enable live agent connection to route a Virtual Agent interaction in the primary instance to a live agent on the secondary instance. The following are the possible connection scenarios.

    -   If there are no matching agents available in the primary instance to cater to the interaction, Bot Interconnect will evaluate the matching conditions configured in the live agent connection and route the interaction to the appropriate live agent in the secondary instance.
    -   If there is only one matching connection, the interaction is routed to that connection and agent availability is checked in the secondary instance.
    -   If there are multiple matching connections, the user is presented with options in the order defined and is connected to the selected connection.
    -   If there are no matching agents available in the secondary instance, the following message is displayed: "There are no agents available. Please try again later.".
    -   If there are matching agents available in the secondary instance, the user is redirected to the available live agent who can cater to the interaction.
    Autopilot mode is currently not supported in the secondary instance when the conversation is initiated on the primary instance. Live agent connection in the secondary instance works only when the secondary instance is in asynchronous mode.


-   **[Install Virtual Agent Bot Interconnect](../task/install-bot-interconnect.md)**  
You can install the Bot Interconnect application if you have the admin role. The application is available from the ServiceNow® Store.
-   **[Using Google Dialogflow as a secondary bot with Virtual Agent Bot Interconnect](using-va-api-ggl-dialogflow.md)**  
With Bot Interconnect, you can use ServiceNow® Virtual Agent as the primary bot with a Google Dialogflow secondary bot. All of the skills and topics available to Google Dialogflow are made available to and executable from channels that are configured for ServiceNow® Virtual Agent.
-   **[Using Microsoft Power Virtual Agents as a secondary bot with Virtual Agent Bot Interconnect](using-va-api-ms-powerva.md)**  
With Bot Interconnect, you can use ServiceNow® Virtual Agent as the primary bot with a Microsoft Power Virtual Agents secondary bot. All of the skills and topics available to Power Virtual Agents are made available to and executable from channels that are configured for ServiceNow® Bot Interconnect.
-   **[Using ServiceNow Virtual Agent as a secondary bot with Virtual Agent Bot Interconnect](using-sn-secondary-bot-with-sn-primary.md)**  
Virtual Agent Bot Interconnect enables you to use ServiceNow® Virtual Agent as the primary bot with a ServiceNow Virtual Agent secondary bot.

**Parent Topic:**[Building and deploying Virtual Agent](using-virtual-agent.md)

