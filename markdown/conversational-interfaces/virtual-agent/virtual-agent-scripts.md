---
title: Virtual Agent scripts
description: Use ServiceNow Virtual Agent script methods and variables to write chat scripts, such as response, trigger, and flow scripts. Variables can also provide context for your live support topics and conversations.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
keywords: [Virtual Agent, scripts, context, topics, user input, record, variables, vaSystem, methods]
breadcrumb: [Virtual Agent technical reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent scripts

Use ServiceNow® Virtual Agent script methods and variables to write chat scripts, such as response, trigger, and flow scripts. Variables can also provide context for your live support topics and conversations.

Virtual Agent scripts can provide context for topics, such as retaining information about a user or a user's input. You can use this information to personalize a conversation, such as to present a scripted greeting or confirmation. Scripts can also specify certain actions to be performed on information that was obtained during a conversation. These actions can be used for creating or updating ServiceNow records.

Scripts run on the server in the scope in which a topic is defined. All scope protections apply. If you're developing a conversation for a scoped application, you must use the scoped API. You can use most APIs that run in server scripts.

## User input and ServiceNow record variables

In Virtual Agent, the following variables are available for use in scripts that you create for a topic.

-   **User input variables**

    When you add an input control to a topic, the system automatically creates a variable to store the user input \(a string, Boolean value, and so on.\). The syntax is `vaInputs.myvar` where `myvar` is the name that you assigned to the input node.

    For example, a text input prompt with the name `First prompt` has a system-defined variable called `vaInputs.first_prompt`. Spaces in the name are replaced with an underscore character, and uppercase characters are changed to lowercase.

-   **ServiceNow record variables**

    If you create a script for a topic that queries a ServiceNow table, then the record object \(GlideRecord\) returned is automatically available for use in the topic. The variable syntax is `vaInputs.myvar` where `myvar` is the record object. For details on querying ServiceNow tables to return a record object, see Querying tables in script.

    Use dot-walking in variables that contain a ServiceNow record to specify a particular field in the table. The syntax is `vaInputs.myvar.field`. For details on dot-walking within a script, see Dot-walking examples.

-   **Accessing user input and ServiceNow record variables**

    Use vaInputs objects to access ServiceNow record variables in scripts. For example, the `vaInputs.myvar == "expected value"`. To access values from user inputs that are not records, use `vaInputs.myvar.getValue()`.

    The following methods are available.

<table id="table_uht_pzs_cpb"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

vaInputs.myvar == "expected value"

</td><td>

Evaluates whether `myvar` matches an expected value. **Note:** Values for user input variables are assigned using user input controls. These values can’t be changed in your scripts.

 -   The Australia release supports additional data types. For more information, see [Input data types in Virtual Agent topics](../reference/va-data-types.md).
-   By default, the user variable is available and is a reference to the sys\_user record for the user.


</td></tr><tr><td>

vaInputs.myvar.getValue\(\);

</td><td>

Returns the value.

</td></tr><tr><td>

vaInputs.myvar.getDisplayValue\(\);

</td><td>

Returns the display value if the stored value is not a ServiceNow record. For variables that contain ServiceNow records, this method returns the display value, as defined by the display field for that table.

 The following example shows the label and choice values for a user input. In this case, `myVar.getValue()` would return a value of 10, 20, or 30, while `myVar.getDisplayValue()` would return Apple, Orange, or Pear.

 ![Label fields include Apple, Orange, and Pear for the choices. The values for each are 10, 20, and 30.](../images/va-value-vs-display.ong.png "Example choice list")

</td></tr><tr><td>

vaInputs.myvar.getDefaultValue\(\);

</td><td>

Returns the default value in a confirmation message.

</td></tr><tr><td>

vaInputs.myvar.getDefaultDisplayValue\(\);

</td><td>

Returns the display value for the default value in a confirmation message.

</td></tr><tr><td>

vaInputs.myvar.unbindEntity\(\);

</td><td>

Removes the value of input variables that the NLU prediction service slot-filled with extracted entities \(unbinds it from the initial input value\). For example, if the user decides to change their choice on a confirmation prompt, you can unbind the entity's value from the input variable. The user will then be prompted again when they loop back to the corresponding input node.

 **Note:** NLU must be enabled on the topic. In the Assistant Designer, select the **Properties** tab to set up NLU. For information about defining NLU entities, see Entities.

</td></tr></tbody>
</table>
## Script variables

You can define script variables for information that is not stored in ServiceNow tables but that can be used to share that information elsewhere in a topic. Script variables are similar to workflow scratchpad variables that store primitives such as integers, Boolean values, or strings. A string value can be either a static or dynamic scripted value. Use the Variables sidebar to define script variables for a topic in Assistant Designer.

![Sidebar in theAssistant Designer canvas for manually adding script variables that are used in topic scripts.](../images/ScriptVariablesExample.png "Variables sidebar")

**Note:** Script variables are intended for use by topic authors with advanced scripting skills.

The variable syntax is `vaVars.myvar`, where `myvar` is the name that you assign to the variable. For example, you can assign a value to the variable using `vaVars.myvar = value;`. Unlike user input variables, script variables can be assigned values in a script.

For information about defining a script variable in a topic, see [Define script variables for a topic](../task/define-script-variables-topic.md).

## Context variables

Context variables work in a global scope whereas system variables work within the scope of the topic. You can use context variables in system parameters within the web client URL. These variables can be used anywhere in the conversation using the `vaContext` object. Use these options to create links to Virtual Agent with predefined variables.

The following example link contains a parameter, `sysparm_city=milan`. In addition to opening a Virtual Agent conversation, using this link creates a variable called `city` with a value of `milan`. This variable can be accessed in a script using `vaContext.city`.

```
https://<instance>.service-now.com/$sn-va-web-client-app.do?sysparm_city=milan
```

A number of Live Agent variables are available for use in topic scripts. These variables include the following:

-   *application*
-   *language*
-   *portal*
-   *search\_text*
-   *short\_description*

The variable syntax is `vaContext.LiveAgent_myvar`, where `myvar` is one of the available [live agent context variables](../reference/live-agent-chat-context-vars.md). Access the variable using `vaContext.LiveAgent_myvar = value;`.

To use Live Agent variables in topic scripts, open the topic in Assistant Designer. On the **Properties** tab, select the pencil icon next to **Live Agent Variables** to add them to the topic.

For information about live agent context variables that are included with Virtual Agent, see [Live agent chat context variables](../reference/live-agent-chat-context-vars.md).

|Method|Description|
|------|-----------|
|vaVars.global\_utterance|Updates when skill picker renders and an utterance is typed in.|

## vaSystem methods

You can use methods in the vaSystem object to do various tasks. Some of these tasks include the following:

-   Attach images to records.
-   Access the search string that was used to find the current topic.
-   Verify that a live agent is available to receive a conversation.
-   Connect the user to a live agent.

**Note:** The use of undocumented system methods is not recommended, as they are unsupported and may be discontinued or altered at any time without prior notice.

<table id="table_xvn_c5r_h2b"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

vaSystem.applyLinkTemplate\(String sysId, String tableName, String actionName\)

</td><td>

Creates an external link that is specific to a portal.

</td></tr><tr><td>

vaSystem.attachRecordToConversation\(String tableName, String sysId\)

</td><td>

Attach ServiceNow records to the Related Tasks list in a Virtual Agent interaction record. These records are updated or created during a Virtual Agent conversation.

</td></tr><tr><td>

vaSystem.attachToRecord\(String mediaId, String tableName, String sysId\)

</td><td>

Attach an uploaded image to a ServiceNow record. The method uses the following parameters:

-   `mediaId`: The path for the image to be attached. To use an image entered by the customer, use `getValue()` on an image input variable. For example, `vaInputs.image_input.getValue()`.
-   `tableName`: A string that contains the name of the table.
-   `sysId`: The sys\_id of the record.

</td></tr><tr><td>

vaSystem.connectToAgent\(\)

</td><td>

Connects the customer to a live agent. For more information on this method, see [Transferring Virtual Agent conversations to a live agent](transfer-to-live-agent.md).

</td></tr><tr><td>

vaSystem.didConnectToLiveAgent\(\)

</td><td>

Returns a Boolean \(true or false\) value whether the current conversation was connected to a live agent.

</td></tr><tr><td>

vaSystem.getClosingMessage\(\)

</td><td>

Returns a closing message for a conversation from system property: **com.glide.cs.general.closing\_message**. \(The message is different for third-party messaging apps such as Microsoft Teams and Slack\).

</td></tr><tr><td>

vaSystem.getConversationId\(\)

</td><td>

Returns the conversation ID of the current conversation.

</td></tr><tr><td>

vaSystem.getGreetingMessage\(\)

</td><td>

Returns a greeting message from UI Message with the key "Hi, I'm your Virtual Agent. Let me know how I can help you today."

</td></tr><tr><td>

vaSystem.getInteractionSysId\(\)

</td><td>

Returns the interaction ID of the current conversation.

</td></tr><tr><td>

vaSystem.getSearchText\(\)

</td><td>

Returns the last utterance typed by the user.

</td></tr><tr><td>

vaSystem.getTopicSelectionMessage\(\)

</td><td>

Returns a UI message with the key "What's your issue or request? Or take a look at what I can help with." \(The message is different for third party messaging apps such as Microsoft Teams and Slack\). This method is returned from the system property **com.glide.cs.topic\_picker\_msg**.

</td></tr><tr><td>

vaSystem.getTranscript\(\)

</td><td>

Gets the conversation transcript.

</td></tr><tr><td>

vaSystem.isLiveAgentAvailable\(\)

</td><td>

Checks whether a live agent is available to receive a conversation that is transferred from the bot. To transfer a conversation to a live agent, call this method before using `vaSystem.connectToAgent()`.

</td></tr><tr><td>

vaSystem.isLiveAgentConfigured\(\)

</td><td>

Returns whether live chat is enabled.

</td></tr><tr><td>

vaSystem.resetAllEntities\(\)

</td><td>

Resets all entities logged in the conversation.

</td></tr><tr><td>

vaSystem.sendBatchedMessages\(\)

</td><td>

Immediately sends queued messages.

</td></tr><tr><td>

vaSystem.sendSeparatorMessage\(\)

</td><td>

Sends a separator message line and returns the closing message from `getClosingMessage()`.

</td></tr><tr><td>

vaSystem.sendSystemMessage\(String message, Boolean showAvatar\)

</td><td>

Sends a system message and returns greetings message from `getGreetingMessage()`.

</td></tr><tr><td>

vaSystem.sendTopicPickerControl\(String topicSelectionMessage, String topicPickerButtonLabel\)

</td><td>

Sends a topic picker control with associated values for the message and "Show me everything" button label.

</td></tr><tr><td>

vaSystem.sendSkillPickerControl\(skillSelectionMessage, args\)

</td><td>

Sends the skill picker control to the user.

 The `skillSelectionMessage` is the message displayed before showing the picker.The `args` parameter allows additional configuration options:

 -   `hideSkillDetails` hides the skill selection message. It defaults to `false`.
-   `hidePromotedTopics` hides promoted topics from the skill picker. It defaults to `false`.
-   `hideShowMeEverything` removes the "Show Me Everything" button from the skill picker. It defaults to `false`.
-   `showNoSkillsConfigured` displays a "No Skills Configured" message if there are no applicable skills. It defaults to `false`.
-   `appendPromotedSkillsToMsg` appends a bulleted list of promoted skills to the skill selection message. It defaults to `true`.

</td></tr><tr><td>

vaSystem.switchTopicByName\(\)

</td><td>

Enables the user to jump from the current conversation topic to the specified topic name. The **X** button is available, so that the user can end the conversation. After the topic ends, the user resumes the global topic. When the conversation ends, the user can select **Click here to start a new conversation** at the bottom of the chat window to restart the topic.The optional **resumeBehavior** parameter specifies how the conversation flow resumes, as follows:

-   If **resumeBehavior=resume**, Virtual Agent resumes the calling topic.
-   If **resumeBehavior=skip**, Virtual Agent skips the calling topic.

 If **resumeBehavior** is not specified, the default behavior for the instance is used.

</td></tr><tr><td>

vaSystem.switchTopicById\(sysid\)

</td><td>

This method is the sysid of **sys\_cb\_topic**, and enables the user to jump from the current conversation topic to the specified topic ID. The **X** button is available, so that the user can end the conversation. After the topic ends, the user resumes the global topic. When the conversation ends, the user can select **Click here to start a new conversation** at the bottom of the chat window to restart the topic.The optional **resumeBehavior** parameter specifies how the conversation flow resumes, as follows:

-   If **resumeBehavior=resume**, Virtual Agent resumes the calling topic.
-   If **resumeBehavior=skip**, Virtual Agent skips the calling topic.

 If **resumeBehavior** is not specified, the default behavior for the instance is used.

</td></tr><tr><td>

vaSystem.topicDiscovery\(String searchTextOverride, Boolean keywordImpl\)

</td><td>

Performs topic discovery based on term in the **searchTextOverride** parameter. The method uses the following parameters:-   `searchTextOverride`: A string on which to run topic discovery.
-   `keywordImpl`: A Boolean that determines whether to use keywords.

</td></tr></tbody>
</table><table id="table_mqd_wqp_1jb"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_cs.VASystemObject.getTranscriptById\(&lt;conversation sysId&gt;\)

</td><td>

Gets the transcript for the current Virtual Agent conversation.

</td></tr></tbody>
</table>**Parent Topic:**[Virtual Agent technical reference](va-advanced-technical-reference.md)

**Related topics**  


[Domain separation and Virtual Agent](domain-separation-virtual-agent.md)

[Virtual Agent interaction records](va-interactions.md)

[Input data types in Virtual Agent topics](../reference/va-data-types.md)

[NLU system entities](../reference/nlu-system-entities.md)

[Virtual Agent URL parameters](../reference/va-sysparm.md)

[Latency feedback in Virtual Agent](../reference/latency-feedback.md)

