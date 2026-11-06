---
title: Designing a Virtual Agent topic
description: Walk through the design of an example Virtual Agent topic that enables users to view incidents they submitted. The example highlights the design controls that you can use to build the conversation flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/design-va-topic.html
release: brazil
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-09-21"
reading_time_minutes: 10
keywords: [Virtual Agent, designer, design, topic, control, node, ServiceNow Otto, NLU, LLM, conversation]
breadcrumb: [Build conversations, Virtual Agent, Conversational Interfaces]
---

# Designing a Virtual Agent topic

Walk through the design of an example Virtual Agent topic that enables users to view incidents they submitted. The example highlights the design controls that you can use to build the conversation flow.

Using Virtual Agent tools and features, you can develop conversations that address many issues that can be resolved without human intervention. After you become familiar with the product and its capabilities, your creativity is an important tool for developing conversations.

Create natural-language–based conversations with ServiceNow Otto. Virtual Agent uses large language models \(LLMs\) to improve conversation experience and self-service workflow success by using generative AI skills.

## Getting started with conversation design

Use Assistant Designer topic creation controls and reusable conversational elements to create the dialogue for your conversations between Virtual Agent and the end user. Before you begin, make sure you do the following:

-   **Identify the use case for a conversation.**

    Determine who uses a conversation topic and the goal, such as solving a user problem or assisting with a self-service task. Besides gathering key requirements for your topic, identify the information that you need from the user to complete the goal.

    For example, you can review your support requests over time and other available metrics to determine common issues, use cases, and customer requests or goals. You can predict recurring requests or issues that a virtual agent could help with.

-   **Determine the structure of a conversation.**

    As you think about your conversation flow, identify the direct path to resolution. Then consider alternative paths where the conversation might branch, depending on the information supplied by the user. Consider how to handle each branch and whether users might loop back to an earlier point in the conversation.

    Conversations have a beginning \(the greeting\), a middle, and an end, which may include a survey or an incident number to follow up on. In the middle, consider how the user might need to switch topics, depending on the issue.

    Consider whether to add or restrict any data collection from the user through means such as additional instructions to the LLM or customized slot-filling.

    Consider setting small talk filters to redirect user statements in LLM conversations. For details on configuring small talk filters, see [Configure small talk filters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-small-talk-filters.md).

-   **Understand the design process in Assistant Designer.**

    When you create a topic in Assistant Designer Asset library, the design process involves these basic steps:

    1.  Decide what use case the topic will address.
    2.  Create the topic and set properties that define the scope, the portal it will be published in, and the assistant to use. Add a detailed topic description to support discovery.
    3.  Build the conversation flow in Assistant Designer's Asset library topic flow tab.
    4.  Test and fine-tune the conversation flow.
    5.  Publish your topic.
    The topic properties determine the different ways in which a topic is designed and used. For example, you can control who uses the topic and any conditions that affect how or when the topic is used. You can associate your topic with an LLM assistant to make the topic available to that assistant. You can also improve topic discovery for your LLM topic by using as much relevant detail as possible in the topic's description.

    For details on the properties that you define for various assets, see [Creating a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md), [Create a reusable topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-topic-blocks.md), and [Create a custom control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/create-custom-control.md).

-   **Have knowledge in the following areas.**
    -   General knowledge of the ServiceNow platform and application table structures.
    -   If you're using scripts in conversation design, an understanding of HTML, JavaScript, and REST integrations.

## Plan the structure and purpose of a conversation

The first step in implementing a Virtual Agent topic is to decide what the topic covers. Consider the intended audience and what you want the audience to accomplish when using the conversation. The goal of this example topic is to create a flow that enables end users to see the status of incidents they submitted. The topic includes an option for the user to add a comment to the incident.

With this goal in mind, the topic requires the following elements:

-   A prompt for the user to select an incident
-   An output showing the status of the incident
-   A prompt to ask if the user wants to leave a comment
-   A utility control to branch the conversation on that answer
-   A prompt for the user to enter a comment
-   A utility control to add the user input as a comment in the incident

There are extra considerations when creating topics for LLM conversations. For guidelines on writing LLM instructions, see [LLM description and instruction guidelines for Virtual Agent topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/va-llm-instruction-guidelines.md) and [General guidelines for writing instructions for generative AI large language models \(LLMs\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/llm-instruction-guidelines.md).

## Build the conversation flow with Virtual Agent controls

The conversation looks similar to the following dialogue flow.

**Important:** This flow is intended to give you a general idea of how a completed flow looks. Keep in mind that you build your topic incrementally and test it frequently, so it's not necessary to build the entire layout first. Make sure to consider both functionality and user experience in your testing.

\[Omitted image "va-sample-conversation.png"\] Alt text: Conversation flow that starts with Choose an incident, followed by Boolean "Leave Comment?" and an incident card. A decision tree lets the user choose Yes or No.

## Configure controls within the conversation

This example begins with defining the conversation flow in Assistant Designer Asset library, after you set the topic properties. The conversation begins with a **Start** node and finishes with an **End** node.

1.  In your Virtual Agent topic, add a **Dynamic Choice** control node to the conversation flow. Use this control to select the incident.
    1.  Enter `Choose an incident` for the **Node name** property. The variable name `choose_an_incident` is automatically generated for the control.
    2.  In the **Prompt** property, enter the text the user sees before selecting an incident. For example, `Please choose an incident record`.
    3.  In the **Populate choices by** property, select Record.
    4.  In the **Table** property, select Incident \[incident\].
    5.  In the **Filter choices** property, select the **Condition** option, and create a condition:

        -   Active is true AND Assignment group is Hardware AND Category is Database
        -   AND
        -   State is New OR State is In Progress
        \[Omitted image "va-sample-condition.png"\] Alt text: A sample condition displaying the configured controls within a conversation for your choice value expression.

2.  Add a **Card** control to the flow. This control shows information from the record selected by the **Dynamic Choice** in the previous step.
    1.  Enter `Status Card` for the **Node name** property.
    2.  In the **Card type** property, select Record.
    3.  In the **Record** property, select Choose an Incident. This choice refers to the Dynamic Choice control created in the previous step, so the data displayed comes from the record chosen there.
    4.  In the **fields** control, select a field. The choices are the fields on the chosen record. In this case, you can see the fields on the incident table.
    5.  After you select a field, select the Add Field option to add more fields to the card. To delete fields from the card, select the delete icon for the field.
3.  Add a Boolean control to the flow. Use this control to prompt the customer with a yes or no question. In this case, the control checks whether the user wants to leave a comment on the selected incident record.
    1.  Enter `Leave Comment?` for the **Node name** property. The variable name `leave_comment_` is automatically generated for the control.
    2.  In the **Prompt** property, enter the text the user sees before the prompt. For example, `Do you want to leave a comment for this incident?`
4.  Add a Decision control to the flow. This control branches the conversation into two possible paths. The path the conversation follows depends on the choice the user made in the previous step.
    1.  There are no properties on the decision control; however, there are properties on the branches below the decision. By default, there is a single branch labeled Always. Select the plus icon at the bottom of the decision control. A second branch appears that is also labeled Always.
    2.  Select one of the branches to access the properties for this branch.
    3.  Change the name to `Leave Comment`.
    4.  In the condition property, select the **Condition** option and select the **Add Condition** button. Use the condition builder to create a condition as shown in the following screenshot.

        \[Omitted image "va-condition-2.png"\] Alt text: In the first field, specify "Leave Comment?" In the second field, specify "is." Select the box to denote that it is true.

        If the value of the **Leave Comment?** variable is true, this condition is met. This variable comes from the Boolean control in the previous step. If the user selects Yes at that prompt, the conversation follows this branch.

    5.  Select the other branch of the decision to access the properties for this branch.
    6.  Change the name to `No Comment`.
    7.  In the condition property, select the **Condition** option and select the **Add Condition** button. Use the condition builder to create a condition as shown in the following screenshot.

        \[Omitted image "va-condition-3.png"\] Alt text: In the first field, specify "Leave Comment?" In the second field, specify "is." Clear the box to denote that it is not true.

        If the value of the **Leave Comment?** variable is false, this condition is met. This variable comes from the Boolean control in the previous step. If the user selects No at that prompt, the conversation follows this branch.

    8.  One of the two branches you have created points to the **End** node of the conversation. The second branch should also lead to this node. Select the arrow at the bottom of that branch and drag it to the **End** node.
5.  Add a **Text Input** control to the Leave Comment branch of the conversation. Use this control to request text input from the user.
    1.  Enter `Get Comment` for the **Node name** property. The variable name `get_comment` is automatically generated for the control.
    2.  In the **Prompt** property, enter the text the user sees before the prompt. For example, `Please enter your comment.`
    3.  Optionally, you can enter a value in the **Advanced** &gt; **Confirmation messages** &gt; **Input completion confirmation** property. This value appears after the user enters a comment.
6.  Add a **Record Action** control to the conversation below the Get Comment control. Use this control to add the text entered in the previous control as a comment on the selected incident.
    1.  Enter `Update Incident` for the **Node name** property.
    2.  In the **Action Type** property, select Update a Record.
    3.  In the **Record** property, select Choose an Incident. This choice refers to the Dynamic Choice control created in the previous step, so the record chosen there is the one that this Record Action control updates.
    4.  In the **Field** property, select Add Field. You can select and give values to fields from this record in the pop-up window that appears.

        \[Omitted image "va-field-values-popup.png"\] Alt text: In the Field values pop-up window, select Additional comments. In the next field, use dot-walking to select Input Variables &gt; Get Comment.

    5.  Select the Additional Comments field from the list.
    6.  Select the data pill picker icon \[Omitted image "variable-reference-picker.png"\] Alt text: Data pill picker icon., and then select the Get Comment input variable from the list. This option refers to the value entered by the user in the **Text Input** control in the previous step.
    7.  Select **Save**.

## Test the conversation

Use the **Test** button to test the flow of the conversation. Preview topics often throughout the design process to find errors or unexpected behavior quickly. For further information on identifying and resolving issues with topics, see [Debug a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/virtual-agent-troubleshooting-guide.md).

**Parent Topic:**[Build conversations in the Asset library in Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/conversation-designer-virtual-agent.md)

