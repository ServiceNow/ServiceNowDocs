---
title: Virtual Agent action scripts
description: You need to write a set of mandatory Workflow Studio action and subflow scripts to pass the user data to VACS, apply transformations and send the response back to your chat interface endpoint.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-03-03"
reading_time_minutes: 9
breadcrumb: [Supported Virtual Agent and Agent Chat features for custom chat integrations, Creating conversational custom chat integrations in Virtual Agent, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent action scripts

You need to write a set of mandatory Workflow Studio action and subflow scripts to pass the user data to VACS, apply transformations and send the response back to your chat interface endpoint.

## Provider and inbound/outbound scripts

A provider, such as Twilio, provides the chat capability. User action scripts perform provider actions, as well as conversational custom chat integration configuration for inbound and outbound transformer actions for your chatbot or custom conversations. Examples of each script are provided. They include a description of what each script does, as well as the action input and action output. You also see examples of the script JSON.

You use Workflow Studio to build these scripts to transform server and client messages. The provider, sender, and inbound/outbound transformer scripts are required. You can use the additional scripts to add more functionality to your chat.

<table id="table_qnf_xdb_xlb"><thead><tr><th>

Script name

</th><th>

Purpose

</th><th>

Required \(Y/N\)

</th></tr></thead><tbody><tr><td>

Provider attribute

</td><td>

Contains a Provider Auth token, a user identifier, user input, and context variables.

</td><td>

Y

</td></tr><tr><td>

Sender action

</td><td>

Bundles the request, and sends a response asynchronously via Workflow Studio or Integration Hub.

</td><td>

Y

</td></tr><tr><td>

Response processor

</td><td>

Performs platform actions, such as an update message status, that's based on a response received for an outbound message.​

</td><td>

N

</td></tr><tr><td>

Contextual action

</td><td>

Supports contextual actions.

</td><td>

N

</td></tr><tr><td>

Link account action

</td><td>

Provides a callback about whether account linking was successful or not​.

</td><td>

N

</td></tr><tr><td>

Outbound transformer

</td><td>

Transforms a chat server's supported control to chat interface-specific rendering.

</td><td>

Y

</td></tr><tr><td>

Inbound transformer

</td><td>

Optional. You can use the default rich controls if they apply to your chat provider. You do not need to provide a separate inbound transform for each input control. If a default behavior does not work, you can override the default with your own inbound transform for a specific Virtual Agent server control.

</td><td>

Y

</td></tr></tbody>
</table>## Provider attributes action script

The provider attributes action script extracts data from the incoming message. The script knows about the conversational custom chat integration protocol and outputs the content of the incoming message, the user ID of the sender, and an optional authentication token.

**Note:** If your provider attributes action script has a contextual action, your script must have both the request\_context.contextual\_action and request\_context.typed\_value so that the user input \(which is matched to a contextual action\) is included in the transcript. If you do not set the request\_context.typed\_value, that message content does not appear in the transcript.

<table id="table_dtk_5fb_xlb"><thead><tr><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

-   Headers \(JSON\) - Request headers
-   Payload \(JSON\) - Request body​

</td><td>

-   Token \(String\) - Authentication token.
-   provider\_user\_id \(String\) - Name of the sender, for example, a user name in a Slack message.
-   request\_context \(JSON\) - Actual content received.
    -   typed\_value - Typed content such as an answer to a question.
    -   attachment\_value.url - URL of the attachment.
    -   attachment\_value.content\_type - Content type of the attachment.
    -   attachment\_value.name - File name of the attachment.
    -   contextual action - Action to perform, such as END\_CONVERSATION, START\_CONVERSATION, AGENT. This script looks at the incoming message. If there is a recognized keyword, then one of the actions can be set, such as outputs.request\_context.contextual\_action = "END\_CONVERSATION";. The framework recognizes this keyword and invokes the contextual action script.
    -   context\_vars - Contextual variables to pass into a conversation, such as \`outputs.request\_context.context\_vars = \{language: "en"\};\`.

</td></tr></tbody>
</table>![An Action Input in Workflow Studio with Headers and Payload set to use JSON.](../images/va-flowdesigner-action-inputs.png "Example: Workflow Studio provider attributes action script input, including headers and payload")

![An Action Output in Workflow Studio specifies the token, request_context, and provider_user_id values.](../images/va-flowdesigner-action-output.png "Example: Workflow Studio provider attributes action script output, including token, request_context, and provider_user_id")

Example: Provider attributes action script.

```
(function execute(inputs, outputs) {
    var headers = (inputs.headers);
    var payload = (inputs.payload);

    // check if an authentication token was included. this is optional.
    var smsUtil = new VASMSTwilioUtil();
    outputs.token = JSON.stringify(smsUtil.getToken(headers, payload));

    var data = payload.data;
    var request_context = {}; 
    // inspect the actual message. it could be an MMS (attachment) or raw text
    if (data['MediaUrl0']) {
        var attachment_value = {};
        attachment_value.url = data['MediaUrl0'];
        attachment_value.content_type = data['MediaContentType0'];
        attachment_value.name = smsUtil.getFileName(attachment_value.url , attachment_value.content_type);
        request_context.attachment_value = attachment_value;
    } else {
       request_context.typed_value = data['Body'];
    }

    // set the mandatory outputs
    outputs.request_context = request_context;
    outputs.provider_user_id = data.From;
})(inputs, outputs);
```

## Sender subflow

Instead of a script, the sender subflow handles the process of sending a message to a provider. The message is contained in a **payload** string as part of the subflow. The sender has a **service\_url** and **origin\_service\_url**, while the outbound URL varies depending on the provider. For example, a message sent through MS Teams uses the value **tenant\_id**. When the Virtual Agent sends the message containing options, the recipient selects an option. The subflow updates the message display based on their choice and removes the options. The conversation continues based on the user’s selected option. The Virtual Agent is freed to continue processing messages rather than trying to send external requests. When creating a subflow do not have an action call an action within the subflow. For more information on subflows, see .

## Contextual action script

The contextual action script performs special keyword actions such as typing `agent` while inside a Virtual Agent topic to get immediately handed off to a live agent.

<table id="table_bvl_hkb_xlb"><thead><tr><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

-   conversation\_id \(String\) - The conversation ID.
-   request\_context \(JSON\) - Request passed from the provider attribute script that contains the action to perform, such as \(END\_CONVERSATION, START\_CONVERSATION, AGENT\).

</td><td>

None

</td></tr></tbody>
</table>Example: Contextual action script.

```
(function execute(inputs, outputs) {
  var contextual_action = inputs.request_context.contextual_action;
  if (contextual_action === "END_CONVERSATION") {
    sn_cs.VASystemObject.endConversation(inputs.conversation_id);
  } else if (contextual_action === "AGENT") {
    sn_cs.VASystemObject.switchToLiveAgent(inputs.conversation_id);
  } else if (contextual_action === "START_CONVERSATION") {
    sn_cs.VASystemObject.startConversation(inputs.conversation_id);
  }
})(inputs, outputs);
```

## Link account action script

The link account action script contains identifiers for the user who is linking. The script also contains the account that it is linked to.

<table id="table_nvv_skb_xlb"><thead><tr><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

-   provider\_user\_id \(String\) - Identifier of the user who is linking, such as a phone number in an SMS case.
-   status \(String\) - Success/failure.
-   user\_id \(String\) - ServiceNow user\_sys\_id for the account that was linked to.

</td><td>

None

</td></tr></tbody>
</table>Example: Link account action script.

```
(function execute(inputs, outputs) {
  
  var richControl = (inputs.rich_control);
  var value = richControl.value;
  outputs.result = richControl.header + ': ' + value.action;
  
})(inputs, outputs);
```

## Response processor action script

The response processor action script performs specialty actions that are based on the response to a send message request. The framework already does basic message status tracking.

<table id="table_mwm_dlb_xlb"><thead><tr><th>

Input

</th><th>

Output

</th></tr></thead><tbody><tr><td>

-   message\_id \(String\) - Identifier of sys\_cs\_message record that is associated with this response.
-   headers \(JSON\) - Headers that are received.
-   body \(String\) - Body that is received.
-   status code \(Integer\) - The HTTP status code that is received.

</td><td>

None

</td></tr></tbody>
</table>Example: Response processor action script.

```
(function execute(inputs, outputs) {
    gs.debug("Response from provider: message_id = " + inputs.message_id + ", status_code = " +
      inputs.status_code + ", headers = " + JSON.stringify(inputs.headers) + ", body = " + inputs.body);
})(inputs, outputs);
```

## Outbound transformer scripts

The outbound transformer scripts convert outgoing Virtual Agent messages to a protocol that is related to the conversational custom chat integration.

Input.

-   rich\_control \(JSON\) - Virtual Agent server rich control component that must be transformed.
-   payload \(JSON\) - Last response that was received from a requester.

Output.

result \(String\) - Provider-appropriate component message to send.

<table id="table_tjb_qlb_xlb"><thead><tr><th>

Outbound transformer name

</th><th>

Script example

</th></tr></thead><tbody><tr><td>

Virtual Agent - SMS Twilio Adapter Default Text Outbound Transformer

</td><td>

```
(function execute(inputs, outputs) {
  var rich_control = inputs.rich_control;
  outputs.result = rich_control['label'];
})(inputs, outputs);
```

</td></tr><tr><td>

Virtual Agent - SMS Twilio Adapter Default Link Outbound Transformer

</td><td>

```
(function execute(inputs, outputs) {
  var richControl = (inputs.rich_control);
  var value = richControl.value;
  outputs.result = richControl.header + ': ' + value.action;
})(inputs, outputs);
```

</td></tr><tr><td>

Virtual Agent - SMS Twilio Adapter Default Picker Outbound Transformer

</td><td>

```
(function execute(inputs, outputs) {
  var rich_control = inputs.rich_control;
  var options = rich_control['options'];
  if (options && options.length > 0) {
      var optionsLength = options.length;
      var picker = rich_control['label'] || "";
      for (var x = 0; x < optionsLength; x++) {
          picker += "\n" + (x+1) +  ": " + options[x].label;
      }
  }
  outputs.text_message = picker;
})(inputs, outputs);
```

</td></tr><tr><td>

Virtual Agent - SMS Twilio Adapter Default Multi Link Outbound Transformer

</td><td>

```
(function execute(inputs, outputs) {
  var rich_control = inputs.rich_control;
  var linkResult = rich_control['header'];
  var totalValues = rich_control['values'].length;
  for (var i = 0; i < totalValues; i++) {
    linkResult = linkResult + '\n';
    var linkValue = rich_control['values'][i];
    linkResult = linkResult + '\n' + linkValue['description'] + ': ' + linkValue['action'];
  }
  outputs.result  = linkResult;
})(inputs, outputs);
```

</td></tr><tr><td>

Virtual Agent - SMS Twilio Adapter Default Card Outbound Transformer

</td><td>

```
(function execute(inputs, outputs) {
  var richControl = (inputs.rich_control);
  var data = JSON.parse(richControl.data);    
  var tableTitle = data.title;
  var fields = data.fields;
  var subtitle = data.subtitle;
  var url = data.url;    
  var message = subtitle ? getCardLine(tableTitle, subtitle) : tableTitle + "\n";
  for (var i= 0; i<fields.length; i++) {
     message += getCardLine(fields[i].fieldLabel, fields[i].fieldValue);
  }
  message += url;
  outputs.result = message;

  function getCardLine(key, value) {
      if (value == '' || value == null || key == '' || key == null)
          return;
      return key + ": " + value + "\n";
  }
})(inputs, outputs);
```

</td></tr></tbody>
</table>## Inbound transformer scripts

The inbound transformer scripts convert incoming conversational custom chat integration messages to a protocol that the Virtual Agent recognizes. It determines the required value to be injected into the rich control that is presented to the user.

Input.

-   request\_context \(JSON\) - The request passed from the Provider Attribute script.
-   rich\_control \(JSON\) - The last rich control sent to the requester that contains the original "question".

Output.

result \(JSON\) - The result expected by the Virtual Agent server. If the requester is responding to a topic picker, it is the sys\_id of the topic. If the requester is responding to an input text, it is the text response.

-   value - sys\_id or text value.
-   search\_text - Text that is used if the requester selected something that was unexpected. For example, a user typed something that the NLU could assist with, such as, "None of these options match what I want" in response to a topic picker component.

<table id="table_k2g_cmb_xlb"><thead><tr><th>

Inbound transformer name

</th><th>

Script example

</th></tr></thead><tbody><tr><td>

Virtual Agent - SMS Twilio Adapter Default Text Inbound TransformerPurpose: Find the text response to the InputText question posed

</td><td>

```
(function execute(inputs, outputs) {
  var requestContext = inputs.request_context;
  var richControl = inputs.rich_control;
  var typedValue = requestContext['typed_value'];
  var attachmentValue = requestContext['attachment_value'];
  var smsUtil = new VASMSTwilioUtil();
  var result = {};
  if(richControl['itemType'] == 'image' || richControl['itemType'] == 'file')	{
    if (attachmentValue && attachmentValue.content_type.includes('image')) {
      result.url = attachmentValue.url;
      result.content_type = attachmentValue.content_type;
      result.name = attachmentValue.name;
      result.headers = attachmentValue.headers;
    } else if (typedValue) {
      result.url = typedValue;
      var contentType = smsUtil.getContentType(typedValue);
      if (typeof contentType === 'undefined')
        gs.error('Please enter a valid image link. Inbound image link: {0}', typedValue);
      else
        result.content_type = contentType;
    } else {
      gs.error('Please upload an image or enter a valid image link.');
    }
  }
  result['value'] = typedValue;
  result['search_text'] = '';
  outputs.result = result;
})(inputs, outputs);
```

</td></tr><tr><td>

Virtual Agent - SMS Twilio Adapter Default Picker Inbound TransformerPurpose: Find the sys\_id of the option that the user selected for this picker question. This script uses the same algorithm of the outbound transformer. If no options are selected, and the user typed something instead, then the "search\_text" is set and fed into NLU if it is enabled on this instance.

</td><td>

```
(function execute(inputs, outputs) {
  var request_context = inputs.request_context;
  var rich_control = inputs.rich_control;
  var selectedValue = request_context["typed_value"];
  var result = {};
  result["value"] = "";
  result["search_text"] = "";
  if (rich_control['options']) {
    var options = rich_control['options'];
    var optionsLength = options.length;
    selectedValue === Number(selectedValue)
    if (selectedValue > 0 && selectedValue <= optionsLength) {
        var selectedOption = options[selectedValue - 1];
        result["value"] = selectedOption.value;
    } else {
        result["search_text"] = request_context["typed_value"];
    }
  }
  outputs.result = result;
})(inputs, outputs);
```

</td></tr></tbody>
</table>**Parent Topic:**[Supported Virtual Agent and Agent Chat features for custom chat integrations](../concept/va-features-custom-chat-integrations.md)

