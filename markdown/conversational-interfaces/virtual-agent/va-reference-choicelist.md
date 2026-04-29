---
title: Dynamic Choice user input control
description: Use the Dynamic Choice user input control in a Virtual Agent topic to dynamically create a list of available choices for your users. Create these choices by querying a table or by using a script to dynamically create them.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 18
breadcrumb: [Assistant Designer user input controls, Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Dynamic Choice user input control

Use the Dynamic Choice user input control in a Virtual Agent topic to dynamically create a list of available choices for your users. Create these choices by querying a table or by using a script to dynamically create them.

## Choice list display

The Dynamic Choice list contains up to 10 items per page. When more than 10 items exist in an NLU conversation, you have the option to show the additional items and also filter the search results. The choice list prompt contains a search icon ![Search icon.](../images/icon-search.png) that users can select to filter the results. When more than 10 items exist in an LLM conversation, a scroll bar appears. When more than 16 items exist in an LLM conversation, a search bar appears.

**Tip:** If you want to change the default number of listed items per page for NLU conversations, you can modify the **com.glide.cs.picker\_page\_limit** system property. The default value is 10.

If selecting multiple choices is turned on, you can search within the **Search for options** field for filtering search results. Select or type all choices that apply, and then select the send icon ![Send icon.](../images/icon-arrow-submit-send.png). When you send your choices through an LLM topic, the LLM responds with whether your choices meet the validation criteria.

You can also select a choice or choices from a list in an LLM conversation by entering an utterance in the chat window. If there is no match for your input, the Virtual Agent informs you that it is not a valid choice, and prompts you to try a different input.

The Dynamic Choice control also provides the option to add a header card that displays above the choice list. Header cards are supported in web and mobile channels.

-   The header card can contain a large or small image or a YouTube video card, along with descriptive text. The choice list contains up to five items by default, but the search feature is suppressed. If there are more than five items, users can choose to show the additional items.

-   To control the number of items displayed below a header card, add the **com.glide.cs.web\_header\_picker\_page\_limit** system property. Use the **Value** to specify the number of items in the choice list. For details about creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).


**Note:**

If you populate a Dynamic Choice list node with only one choice, when testing or using the node, you receive a message reading `“We have [choice] as [node name], is this correct?”`. Use multiple choices in the Dynamic Choice list node to avoid receiving this message.  

You can also alter the message content by navigating to **ALL** &gt; **sys\_properties.list** and editing the **glide.cs.retry\_question\_message** system property. This message value is by default a string `We have {0} as {1}, is this correct?` and is used for slot-filling in multiple cases outside the Dynamic Choice list. Any changes you make are reflected in every use of this property.

## Dynamic Choice user input control properties for LLM topic discovery

<table id="table_nff_y1b_3db"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this node in the topic flow.

</td></tr><tr><td>

Variable name

</td><td>

Name of the variable that stores the user response to this prompt. The variable name is automatically created from the **Node name** property.

</td></tr><tr><td>

Prompt

</td><td>

Prompt or question for the user. The prompt can be either a text string or a script that returns text. This value is used only when the default value is not specified. For example: `What's your name?`

 You can create rich text to alter the styling of the prompt:

-   Use single asterisks or underscores for italic text. For example, `*text*` or `_text_`.
-   Use double asterisks or underscores for bold text. For example, `**text**` or `__text__`.
-   Use triple asterisks or underscores for italic and bold text. For example, `***text***` or `___text___`.
-   Use a spaced hyphen to add a bullet point to a line. For example, `- text`.
-   Use a spaced right angle bracket to create a block quote. For example, `> text`.
-   Use between one and six hash marks to create headers. For example, `#text#` or `######text######`
-   Use brackets and parentheses to create a hyperlink. For example, `[Link text](url)`. Add an exclamation point to a hyperlink to display an image. For example, `![alt text](image url)`

</td></tr><tr><td>

NLU entity

</td><td>

Option to associate an NLU entity with the node. If an NLU entity is associated with the input variable for this node, Virtual Agent can slot-fill the specified value based on the user's utterance. Select an entity from the list of entities associated with the topic intent.

 When you specify an entity for the node, the Do not ask users to confirm recognized entity toggle switch is displayed. When enabled, users are not prompted to confirm the extracted entity.

 This field is available only when NLU discovery is enabled on the instance.

</td></tr><tr><td class="sub-head" colspan="2">

Choices

</td></tr><tr><td>

Populate choices by

</td><td>

Type of dynamic variable to be used. Select one of the following options:

-   **Record**: Returns records from the table selected. The values for these options are GlideRecord objects.
-   **Script**: Expression that returns an array of options.

**Note:**

For more efficient pagination return results for a large data set when using a script expression, review the following script and determine whether you want to use this script:

    ```
(function execute() {
 
var pagingUtil = new global.VirtualAgentChoicePagingUtil(null, "sys_user", null, "user_name,name",
"active=true", null, vaVars);
 
var gr = pagingUtil.getPagingGlideRecordSecure("name", false);

var options = pagingUtil.getSecureOptions(gr, null,'user_name', ['user_name','name']);

return options;
})()

    ```

For more information about the preceding scripting details, review information about [GlideRecords](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) and the additional information:

    -   **fieldName**: Field name is optional information. Pass with `null`.
    -   **table**: Table name to query for displaying the available options.
    -   **pageSize**: Page size is optional information. Pass with `null`.
    -   **searchColumns**: Table columns in a comma-delimited list that applies to any searchText.
    -   **encodedQuery**: Initial query to apply to table rows. For example, `active=true`.
    -   **searchText**: Search text is optional information. Pass with `null`.
    -   **vaVars**: Reference to virtual agent context variables \(`vaVars`\).
    -   **orderByColumn**: Table column used to order the options.
    -   **orderDescending**: Options appear in descending order. Only `true` or `false` values accepted.
    -   **gr**: Glide record name.
    -   **startRow**: Starting row is optional information. Pass with `null`.
    -   **valueColumn**: Table column name to use as the value of each option.
    -   **labelColumns**: Array of table columns to use for each option display.

</td></tr><tr><td>

Table

</td><td>

Table to be searched, available only if you selected **Record** as the method to populate choices.

</td></tr><tr><td>

Filter choices

</td><td>

Option to use the Virtual Agent Designer condition builder or provide a script. Select one of the following:

-   **Condition Builder**: Creates a filter used to select a subset of records from the table.
-   **Script**: Defines the enumeration list for the options \(choice list\) to be displayed. The name-value pair is stored as a string object.

This field is available only when the **Record** option is selected.

</td></tr><tr><td>

Allow the user to select more than one choice

</td><td>

Option to allow users to choose multiple choices from the choice list.

</td></tr><tr><td>

No records response message

</td><td>

Message displayed to the user when the table search doesn’t return any records. The message can be either a text string or a script that returns text.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td>

Header card

</td><td>

Toggle to open a field to add cards which may include images or YouTube videos. For more information, see [Insert a header card in a Static Choice or Dynamic Choice control](../task/insert-header-card-user-input-control.md)

</td></tr><tr><td class="sub-head" colspan="2">

Default value

</td></tr><tr><td>

Default Value

</td><td>

Predefined value for the user response to the question or prompt. The response defined in the **Default value confirmation** field asks the user to confirm the default value. If the user responds with `no`, the value becomes null. The default value can be either a text string or a script that returns text. For example, if you're using dot-walking, the default value might be: `Script Variables > Last username`. Or if you're using a script, the default value might be: `{{vaScripts.lastUsername}}`.

</td></tr><tr><td class="sub-head" colspan="2">

Confirmation messages

</td></tr><tr><td>

Input completion confirmation

</td><td>

Bot response shown to the user when the node interaction is complete. The message can be either a text string or a script that returns text. For example, if you're using dot-walking: `Thanks, (Input Variables > Username)!` Or if you're using a script, the acknowledgement might be: `Thanks, {{vaInputs.username}}!`

</td></tr><tr><td>

Default value confirmation

</td><td>

Message that asks the user to verify that the value in the **Default value** field is correct. This message is used instead of a value in the **Prompt** field. It can contain either a text string or a script that returns text. For example, if you're using dot-walking: `Are you (Input Variables > Username)?` Or if you're using a script, the confirmation message might be: `Are you {{vaScripts.lastUsername}}?`.

</td></tr><tr><td class="sub-head" colspan="2">

Conversation switching

</td></tr><tr><td class="sub-head" colspan="2">

This section is available only when NLU discovery is enabled on the instance.

</td></tr><tr><td>

Turn on to let users change the subject

</td><td>

Option to enable NLU prediction for this node. If enabled, users can enter text to answer questions, regardless of the type of input control being used. Virtual Agent uses this utterance to match another existing intent, letting the user switch topics.

</td></tr><tr><td class="sub-head" colspan="2">

Hide or skip this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr><tr><td>

Allow user to skip this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip this node in the conversation. The condition must evaluate to true. You can set this field using either the condition builder or a script.

</td></tr><tr><td>

Skip reprompting if

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip reprompting in the conversation. When a preceding node is revisited through a topic loopback or Dialog Act, the Virtual Agent bypasses this node and automatically retain its original value.

</td></tr></tbody>
</table>## Example Dynamic Choice user input control for LLM topic discovery

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

<table id="table_uby_wtv_zzb"><thead><tr><th>

Input properties

</th><th>

List user prompt

</th></tr></thead><tbody><tr><td>

![All basic Dynamic Choice user input fields are openly available. Select any of the advanced options to toggle them open individually.](../images/va-dynamic-choice-llm-3.png)

</td><td>

![A choice list returns a list to select from.](../../now-assist-in-va/image/nass-dynamic-choice-user-prompt-zp4.png "Dynamic Choice list prompt example")

</td></tr></tbody>
</table>## Dynamic Choice user input control properties for NLU topic discovery

<table id="table_qwc_d5h_xcc"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Node name

</td><td>

Name that identifies this node in the topic flow.

</td></tr><tr><td>

Variable name

</td><td>

Name of the variable that stores the user response to this prompt. The variable name is automatically created from the **Node name** property.

</td></tr><tr><td>

Prompt

</td><td>

Prompt or question for the user. The prompt can be either a text string or a script that returns text. This value is used only when the default value is not specified. For example: `What's your name?`

 You can create rich text to alter the styling of the prompt:

-   Use single asterisks or underscores for italic text. For example, `*text*` or `_text_`.
-   Use double asterisks or underscores for bold text. For example, `**text**` or `__text__`.
-   Use triple asterisks or underscores for italic and bold text. For example, `***text***` or `___text___`.
-   Use a spaced hyphen to add a bullet point to a line. For example, `- text`.
-   Use a spaced right angle bracket to create a block quote. For example, `> text`.
-   Use between one and six hash marks to create headers. For example, `#text#` or `######text######`
-   Use brackets and parentheses to create a hyperlink. For example, `[Link text](url)`. Add an exclamation point to a hyperlink to display an image. For example, `![alt text](image url)`

</td></tr><tr><td>

NLU entity

</td><td>

Option to associate an NLU entity with the node. If an NLU entity is associated with the input variable for this node, Virtual Agent can slot-fill the specified value based on the user's utterance. Select an entity from the list of entities associated with the topic intent.

 When you specify an entity for the node, the Do not ask users to confirm recognized entity toggle switch is displayed. When enabled, users are not prompted to confirm the extracted entity.

 This field is available only when NLU discovery is enabled on the instance.

</td></tr><tr><td class="sub-head" colspan="2">

Choices

</td></tr><tr><td>

Populate choices by

</td><td>

Type of dynamic variable to be used. Select one of the following options:

-   **Record**: Returns records from the table selected. The values for these options are GlideRecord objects.
-   **Script**: Expression that returns an array of options.

**Note:**

For more efficient pagination return results for a large data set when using a script expression, review the following script and determine whether you want to use this script:

    ```
(function execute() {
 
var pagingUtil = new global.VirtualAgentChoicePagingUtil(null, "sys_user", null, "user_name,name",
"active=true", null, vaVars);
 
var gr = pagingUtil.getPagingGlideRecordSecure("name", false);

var options = pagingUtil.getSecureOptions(gr, null,'user_name', ['user_name','name']);

return options;
})()

    ```

For more information about the preceding scripting details, review information about [GlideRecords](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US) and the additional information:

    -   **fieldName**: Field name is optional information. Pass with `null`.
    -   **table**: Table name to query for displaying the available options.
    -   **pageSize**: Page size is optional information. Pass with `null`.
    -   **searchColumns**: Table columns in a comma-delimited list that applies to any searchText.
    -   **encodedQuery**: Initial query to apply to table rows. For example, `active=true`.
    -   **searchText**: Search text is optional information. Pass with `null`.
    -   **vaVars**: Reference to virtual agent context variables \(`vaVars`\).
    -   **orderByColumn**: Table column used to order the options.
    -   **orderDescending**: Options appear in descending order. Only `true` or `false` values accepted.
    -   **gr**: Glide record name.
    -   **startRow**: Starting row is optional information. Pass with `null`.
    -   **valueColumn**: Table column name to use as the value of each option.
    -   **labelColumns**: Array of table columns to use for each option display.

</td></tr><tr><td>

Table

</td><td>

Table to be searched, available only if you selected **Record** as the method to populate choices.

</td></tr><tr><td>

Filter choices

</td><td>

Option to use the Virtual Agent Designer condition builder or provide a script. Select one of the following:

-   **Condition Builder**: Creates a filter used to select a subset of records from the table.
-   **Script**: Defines the enumeration list for the options \(choice list\) to be displayed. The name-value pair is stored as a string object.

This field is available only when the **Record** option is selected.

</td></tr><tr><td>

Allow the user to select more than one choice

</td><td>

Option to allow users to choose multiple choices from the choice list.

</td></tr><tr><td>

No records response message

</td><td>

Message displayed to the user when the table search doesn’t return any records. The message can be either a text string or a script that returns text.

</td></tr><tr><td class="sub-head" colspan="2">

Advanced

</td></tr><tr><td>

Header card

</td><td>

Toggle to open a field to add cards which may include images or YouTube videos. For more information, see [Insert a header card in a Static Choice or Dynamic Choice control](../task/insert-header-card-user-input-control.md)

</td></tr><tr><td class="sub-head" colspan="2">

Default value

</td></tr><tr><td>

Default Value

</td><td>

Predefined value for the user response to the question or prompt. The response defined in the **Default value confirmation** field asks the user to confirm the default value. If the user responds with `no`, the value becomes null. The default value can be either a text string or a script that returns text. For example, if you're using dot-walking, the default value might be: `Script Variables > Last username`. Or if you're using a script, the default value might be: `{{vaScripts.lastUsername}}`.

</td></tr><tr><td class="sub-head" colspan="2">

Confirmation messages

</td></tr><tr><td>

Input completion confirmation

</td><td>

Bot response shown to the user when the node interaction is complete. The message can be either a text string or a script that returns text. For example, if you're using dot-walking: `Thanks, (Input Variables > Username)!` Or if you're using a script, the acknowledgement might be: `Thanks, {{vaInputs.username}}!`

</td></tr><tr><td>

Default value confirmation

</td><td>

Message that asks the user to verify that the value in the **Default value** field is correct. This message is used instead of a value in the **Prompt** field. It can contain either a text string or a script that returns text. For example, if you're using dot-walking: `Are you (Input Variables > Username)?` Or if you're using a script, the confirmation message might be: `Are you {{vaScripts.lastUsername}}?`.

</td></tr><tr><td class="sub-head" colspan="2">

Conversation switching

</td></tr><tr><td class="sub-head" colspan="2">

This section is available only when NLU discovery is enabled on the instance.

</td></tr><tr><td>

Turn on to let users change the subject

</td><td>

Option to enable NLU prediction for this node. If enabled, users can enter text to answer questions, regardless of the type of input control being used. Virtual Agent uses this utterance to match another existing intent, letting the user switch topics.

</td></tr><tr><td class="sub-head" colspan="2">

Hide or skip this node

</td></tr><tr><td>

Conditionally show this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for presenting this node in the conversation. The condition must evaluate to true.

</td></tr><tr><td>

Allow user to skip this node if

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip this node in the conversation. The condition must evaluate to true. You can set this field using either the condition builder or a script.

</td></tr><tr><td>

Skip reprompting if

</td><td>

No-code condition statement or low-code script that specifies a condition for letting users skip reprompting in the conversation. When a preceding node is revisited through a topic loopback or Dialog Act, the Virtual Agent bypasses this node and automatically retain its original value.

</td></tr></tbody>
</table>## Example Dynamic Choice user input control for NLU topic discovery

**Note:** Virtual Agent Designer controls may display and function differently in other channels.

The dynamic choice list displays 10 items per page. When 10 or more results are returned:

-   The list includes a link at the end of the list to show more results.
-   A search icon \(![Search icon.](../images/icon-search.png)\) displays in the prompt for filtering search results. Users select the icon to open a search box and enter the filter.
-   When selecting multiple choices, you can search within the **Search for options** field for filtering search results. If you input the script to enable secondary fields found in this topic, the search filter results apply to the secondary fields, too. Select or enter all choices that apply, and then select the send icon ![Send arrow icon](../images/icon-arrow-submit-send.png).

When a header card is used, the choice list contains five items per page. When five or more results are returned, the list provides an option to show more results.

**Note:** The search feature is suppressed when a header card is used.

## Dynamic Choice script examples

The following script example can be used in the **Define choices** field only if the value for **Populate choice by** is set to **Script**. This script enables requesters to see their previously selected choices if they choose to edit their choices later in the conversation. This script also displays secondary fields to requesters, such as an email address, gender marker, or both, to help them further differentiate their available choices. Displaying the secondary field to requesters can be especially helpful when dealing with similar values, such as selecting the correct employee name when working with the same or similar names \(that is, Christopher Smith or Chris Smith\).

```
(function execute() {
    var pagingUtil = new global.VirtualAgentChoicePagingUtil(null, "sys_user", 10, "user_name,name",
      "active=true", null, vaVars);
    var selectedOptions = pagingUtil.getSavedSelectedOptions("user", vaSystem);
    if (!selectedOptions || selectedOptions.length == 0) {
      // Secondary labels can be passed to selected options
       selectedOptions.push({ "value": "abel.tuter", "label": "Abel Tuter"
        ,"secondary_label": ["abel.tuter@example.com", "male"]
        });
       selectedOptions.push({ "value": "Beth.anglin", "label": "Beth Anglin"
        ,"secondary_label": ["beth.anglin@example.com", "female"] 
        });
    }
    vaSystem.setSelectedOptions(selectedOptions, "user", false);
    // Topic authors have the ability to define which values should go in the 
    // secondary labels by adding secondary label functions
    pagingUtil.addSecondaryLabelFunction(function (gr) {
      return gr.getValue("email");
    });
    pagingUtil.addSecondaryLabelFunction(function (gr) {
      return gr.getValue("gender");
    });
    var gr = pagingUtil.getPagingGlideRecordSecure("name", false);
    var options = pagingUtil.getSecureOptions(gr, null,'user_name', ['user_name']);
    return options;
})()
```

## Example Dynamic Choice list value expression

```
(function execute(table) {
        var options = [];
        var gr = new GlideRecordSecure(table);
        gr.addEncodedQuery('active=true');
        gr.setLimit(5);
        gr.query();
        while(gr.next()) {
            options.push({ 'value': gr.getUniqueValue(), 'label': gr.getValue('short_description') });
        }
        return options;
})(table)

```

The script in the Choice Value Expression property defines and returns an array of choices. In the example, the script creates an array called `options`, and adds each record found in a GlideRecord query to this array. Each element in the array is given a value in the `value` and `label` keys using data from that GlideRecord. The Table property of the control defines the table used by the script. This example script uses `gr.setLimit(5)` to limit the number of records returned to 5. Using this method helps prevent returned records from creating an overly large choice list.

|Key|Description|
|---|-----------|
|value|The value for the choice. When a user selects a choice from the control, this value is stored in the variable named in the Variable name property.|
|label|The label that appears for this choice in the choice list.|

## Channel support

|Channel|LLM support|NLU/keyword support|Constraints|
|-------|-----------|-------------------|-----------|
|Web UI|Not supported|Supported|None|
|Mobile UI|Not supported|Supported|None|
|Now Assist panel|Not supported|Supported|None|
|Microsoft Teams|Supported|Supported|None|
|Slack|Not supported|Supported|Header cards aren’t supported.|
|Workplace|Not supported|Supported|Header cards aren’t supported.|
|Facebook Messenger|Not supported|Not supported|Not applicable|
|SMS Twilio|Not supported|Supported|Header cards aren’t supported.|
|LINE|Not supported|Not supported|Not applicable|
|WhatsApp|Supported|Supported|None|
|Apple Messages for Business|Not supported|Supported|None|
|Alexa \(Voice\)|Not supported|Supported|For screen devices, use touch scroll; clicking links not supported. For nonscreen devices, use voice pagination.|

**Parent Topic:**[Assistant Designer user input controls](va-user-inputs.md)

