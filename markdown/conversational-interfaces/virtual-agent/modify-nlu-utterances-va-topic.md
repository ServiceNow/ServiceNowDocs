---
title: Modify NLU utterances and entities for a Virtual Agent topic
description: View, test, and modify NLU utterances for a Virtual Agent topic on the NLU Intent tab in Virtual Agent Designer.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-11-05"
reading_time_minutes: 1
keywords: [NLU, Utterances, entities, Virtual Agent, Designer, topic, intent]
breadcrumb: [Create a Virtual Agent topic, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Modify NLU utterances and entities for a Virtual Agent topic

View, test, and modify NLU utterances for a Virtual Agent topic on the **NLU Intent** tab in Virtual Agent Designer.

## Before you begin

If the topic is not currently mapped to a model and intent, the NLU Tab is not available. Specify a model and intent on the **Properties** tab in Virtual Agent Designer.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

2.  Open a topic and view the **NLU Intent** tab.

3.  On the **Utterances** tab, you can do the following:

    -   Type a new utterance in the box, and then select **Add**.
    -   Select the pencil icon to edit an utterance.

        When you are done making changes, select **Save**.

4.  Associate entities with words in utterances.

    Entities represent the context for the action. For example, common industry terms can be defined as entities to clarify the context. Universal system entities may include known elements like date and time or currency. NLU can match defined entities with user input to slot-fill the values. There are five types of entities you can define. For detailed information, see [NLU entities](https://www.servicenow.com/docs/access?context=entities&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

5.  Select **Save** in the header bar.


## What to do next

After making changes, you can [train, test, and publish the model](train-test-publish-nlu-model-vad.md) from this tab.

**Parent Topic:**[Create a Virtual Agent topic](create-virtual-agent-topic.md)

