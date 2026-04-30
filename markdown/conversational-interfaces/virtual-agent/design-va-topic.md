---
title: Designing a Virtual Agent topic
description: Walk through the design of an example Virtual Agent topic that enables users to view incidents they submitted. The example highlights various design controls that can be used to build the conversation flow.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 13
keywords: [Virtual Agent, designer, design, topic, control, node, Now Assist, NLU, LLM, conversation]
breadcrumb: [Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Designing a Virtual Agent topic

Walk through the design of an example Virtual Agent topic that enables users to view incidents they submitted. The example highlights various design controls that can be used to build the conversation flow.

Using Virtual Agent tools and features, you can develop conversations that address many issues that can be resolved without human intervention. Once you become familiar with the product and its capabilities, your creativity is one of the most important tools for developing conversations.

To get started more quickly, the following resources are available for Virtual Agent:

-   **[Now Assist in Virtual Agent](../../now-assist-in-va/concept/now-assist-in-va-landing.md)**

    Create natural-language–based conversations with Now Assist. Virtual Agent uses large language models \(LLMs\) to improve conversation experience and self-service workflow success by way of generative AI skills.

-   **[Pre-built Virtual Agent topics, topic blocks, and ServiceNow NLU models](../reference/prebuilt-topics-ITSM.md)**

    These pre-defined conversations help users with common self-service tasks in each business area, such as creating or updating cases or providing answers to frequently asked questions. [Duplicate the pre-built topics](../task/duplicate-virtual-agent-topic.md) you want to use, and then customize them for your organization.

-   **[Virtual Agent Topic Recommendations](va-topic-recommendations.md)**

    Use the Topic Recommendations app to identify pre-built Virtual Agent topics that can be quickly implemented in your organization. Topic Recommendations uses Intent Discovery to analyze data from your organization and to find relevant pre-built topics that your organization can benefit from, and new topics that would be useful to create.


## Getting started with conversation design

Use Virtual Agent Designer controls and reusable conversational elements to create the dialogue for your conversations between Virtual Agent and the end user. Before you begin, make sure you do the following:

-   **Identify the use case for a conversation.**

    Determine who will use a conversation topic and the goal, such as solving a user problem or assisting with a self-service task. Besides gathering key requirements for your topic, identify the information that you need from the user to complete the goal.

    For example, you can review your support requests over time and other available metrics to determine common issues, use cases, and customer requests or goals. From there, you can predict recurring requests or issues that a virtual agent could help with.

-   **Determine the structure of a conversation.**

    As you think about your conversation flow, identify the direct path to resolution. Then consider alternate paths where the conversation might branch, depending on the information supplied by the user. Consider how to handle each branch and whether users might loop back to an earlier point in the conversation.

    Conversations have a beginning \(the greeting\), a middle, and an end, which may include a survey or an incident number to follow up on. In the middle, consider how the user might need to switch topics, depending on the issue.

    If you're using LLM, consider whether you want to add or restrict any data collection from the user through means such as additional instructions to the LLM or customized slot-filling.

    If you're using Natural Language Understanding \(NLU\), consider scenarios where a user might want to switch topics during a conversation session. For example, a user might want to change topics entirely. Or a user might get sidetracked and ask a question that seems out of context, maybe to engage in "small talk" with the virtual agent. Determine whether you want to let the user resume the original conversation after switching topics during the conversation.

    Consider setting small talk filters to redirect user statements in LLM conversations, or creating small talk topics in both LLM and NLU/keyword conversations. For more information, see [Configure small talk filters](https://www.servicenow.com/docs/access?context=configure-small-talk-filters&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) and [Create a small talk topic](../task/create-small-talk.md).

    You can also review the pre-built setup topics, conversation topics, and topic blocks \(reusable subflows that perform certain design steps and logic\). Determine whether you can use these pre-built items and consider customizing them as needed.

-   **Understand the design process in Virtual Agent Designer.**

    When you create a topic in Virtual Agent Designer, the design process involves these basic steps:

    ![Choose the topic type and set topic properties, build the conversation flow, test and fine-tune the flow, and then publish your topic.](../images/va-design-process-steps.png "Topic design process")

    The topic properties determine the different ways in which a topic is designed and used. For example, you can control who uses the topic and any conditions that affect how or when the topic is used.

    If you're using Now Assist in Virtual Agent, you can associate your topic with an LLM assistant to make the topic available to that assistant. You can also improve topic discovery for your LLM topic by using as much relevant detail as possible in the topic's description.

    If you're using ServiceNow Natural Language Understanding \(NLU\), you can associate an NLU model and intent with your topic.

    For details on the properties that you define for various assets, see [Create a Virtual Agent topic](../task/create-virtual-agent-topic.md), [Create a reusable topic block](../task/create-topic-blocks.md), and [Create a custom control](../task/create-custom-control.md).

-   **Have knowledge in the following areas \(what to know before you begin\)**
    -   General knowledge of the ServiceNow platform and application table structures.
    -   If you're using LLM, an understanding of how large language models and LLM assistants work.
    -   If you're using NLU, an understanding of how intents, entities, and utterances are used in your NLU models.
    -   If you're using scripts in conversation design, an understanding of HTML, JavaScript, and REST integrations.

## Plan the structure and purpose of a conversation

The first step in implementing a Virtual Agent topic is to decide what the topic covers. Consider the intended audience and what you want the audience to accomplish when using the conversation. For this example, the goal of this example topic is to create a flow that enables end users to see the status of incidents they submitted. The topic includes an option for the user to add a comment to the incident.

With this goal in mind, the topic needs the following elements:

-   A prompt for the user to select an incident
-   An output showing the status of the incident
-   A prompt to ask if the user wants to leave a comment
-   A utility control to branch the conversation on that answer
-   A prompt for the user to enter a comment
-   A utility control to add the user input as a comment in the incident

There are extra considerations when creating topics for LLM conversations. For more information, see [LLM description and instruction guidelines for Virtual Agent topics](va-llm-instruction-guidelines.md) and [General guidelines for writing instructions for generative AI large language models \(LLMs\)](https://www.servicenow.com/docs/access?context=capabilities-bundle-landingpage&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Build the conversation flow with Virtual Agent controls

The conversation will look similar to the following dialogue flow.

**Important:** This flow is intended to give you a general idea of how a completed flow looks. Keep in mind that you will be building your topic incrementally and testing your topic frequently, so it's not necessary to build the entire layout first. Make sure to consider both functionality and user experience in your testing.

![Conversation flow that starts with Choose an incident, followed by Boolean "Leave Comment?" and an incident card. A decision tree lets the user choose Yes or No.](../images/va-sample-conversation.png "A completed conversation flow")

## Configure controls within the conversation

This example begins with defining the conversation flow in Virtual Agent Designer, after the topic properties have been set. The conversation begins with a Start node and finishes with an End node.

1.  In your Virtual Agent Designer topic, add a **Dynamic Choice** control node to the conversation flow. This control is used to select the incident.
    1.  Enter `Choose an incident` for the **Node name** property. The variable name `choose_an_incident` is automatically generated for the control.
    2.  In the **Prompt** property, enter the text the user sees before selecting an incident. For example, `Please choose an incident record`.
    3.  In the **Populate choices by** property, select Record.
    4.  In the **Table** property, select Incident \[incident\].
    5.  In the **Filter choices** property, select the **Condition** option, and create a condition:

        -   Active is true AND Assignment group is Hardware AND Category is Database
        -   AND
        -   State is New OR State is In Progress
        ![A sample condition displaying the configured controls within a conversation for your choice value expression.](../images/va-sample-condition.png "An example condition builder")

2.  Add a **Card** control to the flow. This control shows information from the record selected by the **Dynamic Choice** in the previous step.
    1.  Enter `Status Card` for the **Node name** property.
    2.  In the **Card type** property, select Record.
    3.  In the **Record** property, select Choose an Incident. This choice refers to the Dynamic Choice control created in the previous step, so the data displayed comes from the record chosen there.
    4.  In the **fields** control, select a field. The choices available are the available fields on the chosen record. In this case, you can see the fields on the incident table.
    5.  After a field has been selected, select the Add Field option to add additional fields to the card. To delete fields from the card, select the delete icon to the right of the field.
3.  Add a Boolean control to the flow. This control is used to prompt the customer with a yes/no question. In this case, the control checks whether the user wants to leave a comment on the selected incident record.
    1.  Enter `Leave Comment?` for the **Node name** property. The variable name `leave_comment_` is automatically generated for the control.
    2.  In the **Prompt** property, enter the text the user sees before the prompt. For example, `Do you want to leave a comment for this incident?`
4.  Add a Decision control to the flow. This control branches the conversation into two possible paths. The path the conversation follows depends on the choice the user made in the previous step.
    1.  There are no properties on the decision control; however, there are properties on the branches below the decision. By default, there is a single branch labeled Always. Select the blue plus icon at the bottom of the decision control. A second branch appears that is also labeled Always.
    2.  Select one of the branches to access the properties for this branch.
    3.  Change the name to `Leave Comment`.
    4.  In the condition property, select the **Condition** option and select the **Add Condition** button. Use the condition builder to create a condition as shown in the following screen shot.

        ![In the first field, specify "Leave Comment?" In the second field, specify "is." Select the box to denote that it is true.](../images/va-condition-2.png)

        If the value of the **Leave Comment?** is true, this condition is met. This variable is the variable from the Boolean control in the previous step. If the user chose Yes at that prompt, the conversation follows this branch.

    5.  Select the other branch of the decision to access the properties for this branch.
    6.  Change the name to `No Comment`.
    7.  In the condition property, select the **Condition** option and select the **Add Condition** button. Use the condition builder to create a condition as shown in the following screen shot.

        ![In the first field, specify "Leave Comment?" In the second field, specify "is." Clear the box to denote that it is not true.](../images/va-condition-3.png)

        If the value of the **Leave Comment?** is false, this condition is met. This variable is the variable from the Boolean control in the previous step. If the user chose No at that prompt, the conversation follows this branch.

    8.  One of the two branches you have created points to the **End** node of the conversation. The second branch should also lead to this node. Select the arrow at the bottom of that branch and drag it to the **End** node.
5.  Add a **Text Input** control to the Leave Comment branch of the conversation. This control is used to request text input from the user.
    1.  Enter `Get Comment` for the **Node name** property. The variable name `get_comment` is automatically generated for the control.
    2.  In the **Prompt** property, enter the text the user sees before the prompt. For example, `Please enter your comment.`
    3.  Optionally, you can enter a value in the **Advanced** &gt; **Confirmation messages** &gt; **Input completion confirmation** property. This value appears after the user enters a comment.
6.  Add a **Record Action** control to the conversation below the Get Comment control. This control is used to add the text entered into the previous control as a comment on the selected incident.
    1.  Enter `Update Incident` for the **Node name** property.
    2.  In the **Action Type** property, select Update a Record.
    3.  In the **Record** property, select Choose an Incident. This choice refers to the Dynamic Choice control created in the previous step, so the record chosen there is the one that this Record Action control updates.
    4.  In the **Field** property, select Add Field. You can select and give values to fields from this record in the pop-up window that appears.

        ![In the Field values pop-up window, select Additional comments. In the next field, use dot-walking to select Input Variables > Get Comment.](../images/va-field-values-popup.png)

    5.  Select the Additional Comments field from the list.
    6.  Select the data pill picker icon ![Data pill picker icon.](../images/variable-reference-picker.png), and then select the Get Comment input variable from the list. This option refers to the value entered by the user in the **Text Input** control in the previous step.
    7.  Select **Save**.

## Test the conversation

Use the **Test** button to test the flow of the conversation. Preview topics often throughout the design process to find errors or unexpected behavior quickly. For further information on identifying and resolving issues with topics, see [Debug a Virtual Agent topic](../reference/virtual-agent-troubleshooting-guide.md).

**Parent Topic:**[Getting started with Virtual Agent Designer](../reference/conversation-designer-virtual-agent.md)

