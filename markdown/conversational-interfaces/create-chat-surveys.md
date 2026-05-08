---
title: Create chat surveys
description: Use Survey Designer to build conversational questionnaires for gathering pre-chat information and post-chat feedback from end users. These questionnaires run in the chat client for Virtual Agent and Agent Chat.
locale: en-US
release: australia
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Survey Designer, Virtual Agent, Agent Chat, surveys, questionnaires, pre-chat, post-chat]
breadcrumb: [General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Create chat surveys

Use Survey Designer to build conversational questionnaires for gathering pre-chat information and post-chat feedback from end users. These questionnaires run in the chat client for Virtual Agent and Agent Chat.

## Before you begin

Identify the information that you want from your requesters, such as their name or email address. If you're collecting pre-chat information, determine whether certain survey responses should be stored as chat context variables so that you can use that information for topic discovery or routing chats to certain work item queues. Before you build your survey, [configure the context variables](ac-configure-context-variables.md) for storing responses to certain survey questions. You will map these chat context variables to the appropriate questions in your survey.

**Note:** When enhanced chat is turned on, post-chat surveys only appear after a live agent conversation has ended.

Role required: survey\_admin or admin

## About this task

You define, configure, and publish conversational questionnaires \(surveys\) using Survey Designer. You can use various survey controls to define the content of your questionnaires. For details on the survey controls available, see Survey designer elements to see how the controls are rendered in the survey. For example, the Choice control provides a multiple choice selection to your users.

The survey controls map to corresponding Virtual Agent Designer input controls that render the survey as a conversation in the chat client. For examples on how Virtual Agent Designer input controls are rendered in run-time conversations, see [Virtual Agent Designer user input controls](../../virtual-agent/reference/va-user-inputs.md). The following table identifies the survey controls supported in Virtual Agent Designer.

|Survey Designer controls|Comparable Virtual Agent Designer user input controls|
|------------------------|-----------------------------------------------------|
|Attachment|Image|
|Boolean|Boolean|
|Choice|Static Choice|
|Date|Date Time|
|Date/Time|Date Time|
|Number|Text input|
|Percentage|Text input|
|Scale|Static Choice|
|Numeric scale|Static Choice|
|String|Text|
|Image scale|Carousel|
|Reference|Not supported|
|Multiple selection|Not supported|
|Ranking|Not supported|
|Template|Not supported|

## Procedure

1.  Navigate to **All** &gt; **Survey** &gt; **Survey Designer**.

2.  Select the **Configuration** tab and configure the survey.

    As you configure your survey, remember the following:

    -   If you want an introduction note and end note to begin and end your survey, enter your content in the **Introduction** and **End note** fields.
    -   Select the **Chat Survey** option to enable conversational questionnaires. This option also enables the display of the **Context** option in the Properties form for each survey control.
    -   Select **Save**.
    For details, see Configure a survey in the survey designer.

3.  Select the **Design** tab and give your survey a **Name**.

    As you design your survey questions, remember the following:

    -   To create a question, drag a data type icon from the Controls palette and drop it into the category container. Give each question a **Name** and select the gear icon to open the Properties form for the control.
    -   In the Properties form, complete the fields as needed to define the control.
        -   If you enable the **Mandatory** option, users are required to answer the survey question. If you leave this field blank, users can skip the question in the survey.
        -   If you want to store the user response to this question, enter the chat context variable in the **Context** field.
    -   Select **Save**.
    For details, see Create a question in the survey.

4.  When you are finished defining the questions in your survey, select **Preview** to review your survey.

5.  When you are satisfied with the survey, select **Save and Publish**.

    Your survey is listed in the Assessment Metric Types \[asmt\_metric\_type\] table.


## What to do next

Define the pre-chat and post-chat survey configurations that control the surveys to be presented to your requesters.

**Parent Topic:**[General chat settings](../concept/ci-configuring-chat-features.md)

