---
title: Assistant Designer controls
description: A Virtual Agent topic consists of a collection of controls within a topic flow. Use these controls to collect, process, and present information to your users. Controls can also read, create, and update records on your instance.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Virtual Agent, Designer, controls, topic flow, read, create, update, records]
breadcrumb: [Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Assistant Designer controls

A Virtual Agent topic consists of a collection of controls within a topic flow. Use these controls to collect, process, and present information to your users. Controls can also read, create, and update records on your instance.

Each set of controls performs specific functions in a conversation flow.

|Category|Description|
|--------|-----------|
|Start segment|Appears automatically in a topic flow and cannot be added to or removed from a conversation. This control can be configured with a greeting response that appears when a conversation begins.|
|End segment|Appears automatically in a topic flow and cannot be added to or removed from a conversation. This control can be configured with a final confirmation message before the end of a conversation. Ensure that all branches of your topic eventually connect to this control.|
|[User Input](../reference/va-user-inputs.md)|Prompts and captures information from the user in a conversation.|
|[Bot Response](../reference/va-bot-responses.md)|Displays bot responses in a conversation.|
|[Utilities](../reference/va-utilities.md)|Handles actions and logic within a topic, such as running a script or adding different conversation paths \(branches\) in a topic. You can also use them to call automated Workflow Studio workflows.|

For controls that have prompts, messages, default values, or confirmation messages, you can enter any of the following input values:

-   Text strings
-   Data pills
-   Strings with embedded data pills
-   Scripts that return strings

## Data pills

Use data pills to quickly and easily add dynamic information to your controls without using a script. Select the data pill icon ![](../images/variable-reference-picker.png) to open the data pill picker interface. In this interface, you can select data from script variables and from input variables set by your User Input controls.

Using data pills enables you to quickly and easily access the data in your variables. In contrast, scripting provides more complex options, like handling translation. The following examples illustrate how to use a text bot response that includes the name of the customer, handled both as a data pill and a script.

|Method|Result|
|------|------|
|Data pill|![Data pill selector, showing Input Variables and Script Variables options.](../images/va-data-pill-selector.png)|
|![Data pill selector showing a text control.](../images/va-data-pill-result.png)|
|Script|![An example text control showing a dynamic scripted entry.](../images/va-script-entry.png)|
|![A text control showing a dynamic scripted response message.](../images/va-script-result.png)|

The first example uses the data pill selector to choose **Get Name**, an input variable that contains the name of the customer. The second example accomplishes the same thing using a script. The script example also uses `gs.getMessage` to handle translating the message.

## Hide or skip this node \(condition property\)

Almost all controls have a condition property. The exceptions are the Decision utility and the Start and End nodes.

In user input controls, the condition property determines whether the control is used or skipped in a conversation. To always use the control, leave the condition field empty. To determine the conditions under which the control is used, do one of the following:

-   Create a condition using the condition builder interface, which lets you add data pills to specify conditions built using this interface.
-   Provide a script for the condition property that returns a value of true or false. If the return value is false, the control is not used and the conversation will continue to the next control along that branch of the topic.

Use conditions to make your conversations more dynamic based on context, data, or scripted logic.

<table id="table_xgn_qy5_bgb"><thead><tr><th>

Scripted condition

</th><th>

Condition builder condition

</th></tr></thead><tbody><tr><td>

Sample script for conditionally showing the node:

```
(function execute() {
   var gr = new GlideRecord('incident');
   return gr.canCreate();
})()
```

</td><td>

![Sample condition builder defining User with data pill selector set to Input Variables for User.](../images/va-condition-builder.png)

</td></tr></tbody>
</table>In this example, a condition script returns a value of true if the current user is able to create incident records. This condition prevents a utilities control from creating an incident when the user does not have permission to do so.

**Parent Topic:**[Assistant Designer interface reference](vad-reference.md)

