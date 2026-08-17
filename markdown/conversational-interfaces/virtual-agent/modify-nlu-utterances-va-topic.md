---
title: Modify NLU utterances and entities for a Virtual Agent topic
description: View, test, and modify NLU utterances for a Virtual Agent topic on the NLU Intent tab in Assistant Designer Asset library.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/modify-nlu-utterances-va-topic.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 1
keywords: [NLU, Utterances, entities, Virtual Agent, Designer, topic, intent]
breadcrumb: [Creating a Virtual Agent topic, Getting started with the Asset library in Assistant Designer, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Modify NLU utterances and entities for a Virtual Agent topic

View, test, and modify NLU utterances for a Virtual Agent topic on the **NLU Intent** tab in Assistant Designer Asset library.

## Before you begin

If the topic is not currently mapped to a model and intent, the NLU tab is not available. Specify a model and intent on the **Properties** tab in Assistant Designer Asset library.

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistant Designer**.

2.  Select the **Asset library** tab.

3.  Set the topic discovery type toggle switch to **NLU/Keyword**.

4.  Open a topic and view the **NLU Intent** tab.

5.  On the **Utterances** tab, you can do the following:

    -   Enter a new utterance in the box, and then select **Add**.
    -   Select the pencil icon to edit an utterance.

        When you are done making changes, select **Save**.

6.  Associate entities with words in utterances.

    Entities represent the context for the action. For example, common industry terms can be defined as entities to clarify the context. Universal system entities may include known elements like date and time or currency. NLU can match defined entities with user input to slot-fill the values. There are five types of entities you can define. For detailed information, see [NLU entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/entities.md).

7.  Select **Save** in the header bar.


## What to do next

After making changes, you can [train, test, and publish the model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/train-test-publish-nlu-model-vad.md) from this tab.

**Parent Topic:**[Creating a Virtual Agent topic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/create-virtual-agent-topic.md)

