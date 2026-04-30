---
title: Publish the virtual agent topics for callback
description: Publish the Virtual Agent topics for callback to help your customers request a callback from agents when there’s a long wait time to reach a live agent or agents are unavailable.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Omnichannel Callback for Customer Service Management, Enable communication channels, Configuring Customer Service Management, Customer Service Management]
---

# Publish the virtual agent topics for callback

Publish the Virtual Agent topics for callback to help your customers request a callback from agents when there’s a long wait time to reach a live agent or agents are unavailable.

## Before you begin

Ensure that the Conversational appointment booking application is installed.

Role required: virtual\_agent\_admin or admin

## About this task

Deploy the inactive topic to save it and make it available to users on Virtual Agent clients.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  In the Topics page, publish the following topics.

    -   Request a callback
    -   Reschedule a callback
    -   Cancel a callback
3.  In the Header bar for the topic, select **Publish**.

    If you're using NLU discovery, the Choose what to publish dialog box appears. Select the available items to publish with the topic, such as the NLU model and language mappings, and then click **Publish**.

    **Note:** If the **Publish Model** option is unavailable, the model may need some work. For example, the model may not have enough intents or may need more utterances for some intents. Fix these issues before proceeding. Also, if a model language is unavailable, the language-specific model has never been published. Publish it from NLU Workbench. For more information, see [Model management](https://www.servicenow.com/docs/access?context=model-management-phases&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

    For topics, the topic state is Active and the Published state changes to **just now**.

4.  If you published a conversation topic, verify that your keywords or NLU utterances for the topic work as expected.

    1.  Return to the Topics page, and then click **Test Active Topics**.

    2.  In the conversation window, enter keywords or NLU utterances that correspond to the topic intent to verify that the topic opens.

        For the pre-built Virtual Agent topics, the bot returns a list of topics that match the entered keyword or utterance.


## Result

The topics are published and are available for use in calling topics.

