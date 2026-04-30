---
title: Add NLU to an existing keyword topic
description: Create and map an NLU model group and intent for the topic from Virtual Agent Designer.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Create a Virtual Agent topic, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Add NLU to an existing keyword topic

Create and map an NLU model group and intent for the topic from Virtual Agent Designer.

## Before you begin

[Configure NLU on the instance in Virtual Agent General Settings](configure-nlu-settings.md).

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Open an existing topic.

3.  Select the **Properties** tab.

4.  In the **NLU Model** field, do one of the following:

    **Note:** If the **NLU model** field does not appear and you have Now Assist enabled, ensure that you haven't selected an LLM topic. Navigate back to the Topics page and select a topic that has the **Model Type** set to **NLU/Keywords**.

    -   Choose an existing model.
    -   Select **Create Model** to create a new model group.

        1.  In the **Model Name** field, enter a name for the new model group.
        2.  In the **Intent name** field, accept the default value or enter a name for the new intent.
        **Note:** New models are created in **Draft** state.

5.  In the **Associated Intent** field, do one of the following:

    -   Choose an existing intent.
    -   Select **Create intent** to create a new intent.

        In the **Intent Name** field, accept the default value or enter a name for the new intent.

6.  In the **Keywords** field, enter key phrases or terms that users enter to initiate the conversation with the Virtual Agent.

    Press **Enter** after each phrase. Keywords are also used for languages that are currently not available in NLU.

7.  Select the **NLU Intent** tab, and then add utterances and associate entities with them.

    For more information about adding utterances, see [Create an NLU intent](https://www.servicenow.com/docs/access?context=create-nlu-intent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information about defining entities, see [Entities](https://www.servicenow.com/docs/access?context=entities&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

8.  Make any other changes on the **Flow** tab, such as associating entities with a node or adding entities as input variables for the topic.

9.  When you're finished with the topic, select **Save** in the topic header bar.


## Result

The modified topic is in the inactive state until you publish it.

**Parent Topic:**[Create a Virtual Agent topic](create-virtual-agent-topic.md)

