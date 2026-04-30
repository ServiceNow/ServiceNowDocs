---
title: Map a topic to a secondary NLU model
description: Map a Virtual Agent topic to a secondary model in the model group or to a standalone, single-language NLU model for each supported language.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Localize Virtual Agent topics that use NLU topic discovery, Localizing Virtual Agent conversations, Localization options for Virtual Agent, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Map a topic to a secondary NLU model

Map a Virtual Agent topic to a secondary model in the model group or to a standalone, single-language NLU model for each supported language.

## Before you begin

**Note:** An updated Virtual Agent Designer user interface is available when you install Now Assist in Virtual Agent and turn on the Now Assist Topics skill. This content assumes that you have activated this skill and can see the list view. If this skill is not enabled, you will see the legacy UI and topics page. For more information, see [Virtual Agent Designer legacy topics page](../reference/vad-prev-topics-page.md).

If you're using ServiceNow NLU, review [NLU model mapping in Virtual Agent Designer](../concept/nlu-model-binding-vad.md) for an understanding of NLU model groups.

If necessary, add secondary languages to the model group in NLU Workbench to create language-specific versions of the model. For more information, see [Multilingual model management](https://www.servicenow.com/docs/access?context=multilingual-model-managent&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

Role required: virtual\_agent\_admin or admin

## About this task

If you select a secondary model for a language that is part of a different model group, the mapping changes for the entire topic. Secondary models must be part of the same model group as the primary language. You can select a different model and intent for a secondary language when it is the only language in the model \(and therefore the primary language\).

![A mapping change alert says, "We updated mappings for these languages: English, French, German, Spanish."](../images/updated-language-bindings-message.png "Updated model group mappings message")

![On the Intent mapping tab, a topic is mapped to a model group with an English primary language model and a German secondary language model.](../images/intent-mapping-primary-secondary-models.png "Topic mapped to a model group with primary and secondary languages")

For more information, see [NLU model mapping in Virtual Agent Designer](../concept/nlu-model-binding-vad.md).

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer** and open a topic.

2.  Slide the discovery type toggle switch to **NLU/keyword** toggle, and open a topic.

3.  Open the **Languages** tab, and then select the **NLU language mapping** tab.

    The first column is the NLU mapping that is based on your current session language. For example, if you're using English, the first column is **English**.

4.  In the **Language to edit** list, select the language to map.

    The languages listed are based on the NLU languages that you enabled in Virtual Agent settings. After you select a language, a column displays in the Intent mapping section and, if applicable, in the Entity mapping section. For example, if you select **Français**, a French language column displays.

    ![The NLU Language Mapping tab displays a column for English and a column for French language mappings. The English model and intent are mapped to a French model and intent.](../images/nlu-lang-mapping.png)

5.  Update the Intent mapping section.

    1.  In the Model row, select an NLU model for the language that you selected.

    2.  In the Intent row, select an NLU intent for the language that you selected.

6.  If applicable, update the Entity mapping section.

    For each language, map an entity from the model to an input node in the topic. In a conversation, these nodes are populated automatically with the entity value.

7.  Click **Save**.


## What to do next

[Test topic and NLU model translations](test-nlu-language-model.md)

**Parent Topic:**[Localize Virtual Agent topics that use NLU topic discovery](use-lf-translate-va-nlu.md)

