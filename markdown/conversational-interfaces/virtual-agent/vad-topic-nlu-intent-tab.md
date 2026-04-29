---
title: Topic NLU Intent tab
description: You can edit and refine ServiceNow NLU models from within Assistant Designer. When a conversation topic is bound to an associated NLU model and intent, use the NLU Intent tab to review and edit utterances and associated entities.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Virtual Agent, topic, NLU, natural language understanding, intent, tab, utterances, entities, conflicts]
breadcrumb: [Assistant Designer interface reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Topic NLU Intent tab

You can edit and refine ServiceNow NLU models from within Assistant Designer. When a conversation topic is bound to an associated NLU model and intent, use the **NLU Intent** tab to review and edit utterances and associated entities.

**Note:** An updated Assistant Designer Asset library user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not activated, you see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](vad-prev-topics-page.md).

If your topic uses NLU discovery, the topic **NLU Intent** tab appears on the Assistant Designer interface. Test your topic to see the prediction results for topic discovery and the corresponding confidence scores for the results. Depending on the results, you can modify the associated utterances and entities in the NLU model for your topic intent.

## Utterances tab

Use the **Utterances** tab to perform the following tasks.

<table id="table_ikh_vgz_rzb"><thead><tr><th>

I want to...

</th><th>

Do this

</th></tr></thead><tbody><tr><td>

Add an utterance

</td><td>

Use the **Add** field to enter an utterance for an intent. Each utterance must be unique and contain fewer than 200 characters.

</td></tr><tr><td>

Edit an utterance

</td><td>

Select the Edit icon ![](../images/edit-icon.png) next to the utterance.

</td></tr><tr><td>

Duplicate an utterance

</td><td>

Select the Copy icon ![](../images/copy-utterance-icon.png) next to the utterance.

</td></tr><tr><td>

Move an utterance to another intent

</td><td>

Select the Menu icon ![](../images/manage-bot-icon.png), and then select **Move this utterance to another intent**.

</td></tr><tr><td>

Delete an utterance

</td><td>

Select the Menu icon ![](../images/manage-bot-icon.png), and then select **Delete this utterance**.

</td></tr><tr><td>

Define a new entity

</td><td>

1.  Select a word in an utterance to use as an entity.
2.  In the Create New Entity picker, select the type of entity to be created, such as a simple or system-derived entity.

For information about the types of entities that you can define, see [NLU entities](https://www.servicenow.com/docs/access?context=entities&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). For information about system entities, see [NLU system entities](nlu-system-entities.md). When you add an entity, it is also displayed in the **Associated Entities** tab.


</td></tr></tbody>
</table>![The Check IT Ticket Status topic displays 24 utterances. There are two associated entities. You can add more utterances, or train and test your model.](../images/NLU-intent-tab-utterances-2.png "Example utterances on the NLU Intent tab")

![Select a word or phrase in an utterance, then use the Create New Entity picker to add an entity related to it.](../images/NLU-intent-create-entities-2.png "Adding entities on the Utterances tab")

## Associated Entities tab

Use the **Associated Entities** tab to view the entities defined for the intent. Select the name to view the utterances that the entity is associated with.

![The Associated Entities sub-tab lists the entities associated with the intent.](../images/associated-entities-tab.png "Entities defined for an intent named UpdatePhoneNumber")

You can also associate system entities, such as date and time, with an intent. For more information about supported system entities, see [NLU system entities](nlu-system-entities.md).

## Conflicts tab

Use the **Conflicts** tab to view conflicts among your intents. For example, if two different intents use the same utterance, this will appear as a conflict in both Assistant Designer and NLU Workbench. Identifying and resolving conflicts improves the effectiveness of NLU topic discovery.

![The Conflicts tab shows problems that may interfere with topic discovery. In this example, two separate intents contain the same utterance.](../images/nlu-intent-tab-conflicts-2.png "Utterance conflict between two intents")

**Parent Topic:**[Assistant Designer interface reference](../concept/vad-reference.md)

