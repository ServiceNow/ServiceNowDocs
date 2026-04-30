---
title: Topic mapping to a multilingual NLU model group
description: When you map a topic to a multilingual model group in Virtual Agent Designer, the topic mappings for enabled languages are set up automatically.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Create a Virtual Agent topic, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Topic mapping to a multilingual NLU model group

When you map a topic to a multilingual model group in Virtual Agent Designer, the topic mappings for enabled languages are set up automatically.

Model groups contain a primary language model, such as English, and secondary language models. Secondary models are translated copies of the primary model, where each secondary model uses a different language. Any supported language can be the primary language for a primary model or the secondary language for a secondary model. The language is reflected in the model name. For example, `FR` for French, `DE` for German, `JA` for Japanese, and `ES` for Spanish.

![A multilingual model group contains English as its primary language model. Secondary language models include French, German, Spanish, or any additional languages you might add.](../images/nlu-model-group-org.png "Multilingual model groups contain one primary language model and multiple secondary language models")

You can view or change the model and intent mappings on the topic **Properties** tab. You can review secondary language mapping on the topic **Languages** tab.

Because secondary model content is only a translated copy of its primary model content, the secondary language mappings must always point to the same model group as the primary language. For this reason, if you map a language in a topic to a model that is part of a multilingual model group, then all of the topic mappings are updated to use the language models in that group. Virtual Agent Designer informs you of the change.

![A mapping change alert says, "We updated mappings for these languages: English, French, German, Spanish."](../images/updated-language-bindings-message.png "Updated NLU mappings message")

**Note:** You can map single-language models to a topic as long as there is no conflict with the corresponding language models in the group.

If you create a model group in NLU Workbench, you can specify the primary language. If you create a model from within Virtual Agent Designer, the primary language is determined by the user session language. For example, if you create a new model in a German user session, the primary language of the model group will be German.

Model groups make it easier to maintain your topics. For more information about NLU model groups, see [Multilingual model management](https://www.servicenow.com/docs/access?context=multilingual-model-managent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

**Note:** If a model contains only a single language, that language is considered to be the primary language. The topic is mapped to the model and specified intent only. If more than one language has been activated in NLU Settings, those languages are not mapped to the model. To use the topic in other languages, map them to other models manually on the **Languages** tab. For more information, see [Map a topic to a secondary NLU model](../task/map-nlu-language-model.md).

## Handling disabled intents within a model

If an intent for the primary language within the model group is disabled, the primary intent displays as disabled in Virtual Agent Designer. When the primary language is disabled, the intent is still mapped to the topic, but all secondary intents are also shown as disabled. This is because the secondary languages are always dependent on the primary language within a model. If an intent for one or more secondary languages is disabled, the other languages remain active. Virtual Agent Designer displays messaging to indicate that some intents are currently disabled.

![The NLU Intent mapping area on the Languages tab indicates that the mapped French intent is not available because it was disabled in NLU Workbench.](../images/nlu-languages-disabled-intent.png "Topic with a disabled French intent on the Languages tab")

To allow topic discovery for the language, enable the intent in NLU Workbench. For more information, see [Enable or disable a secondary model intent](https://www.servicenow.com/docs/access?context=enable-disable-secondary-model-intent&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Avoiding model conflicts

In order to avoid conflicts, Virtual Agent Designer may not display all of the existing models when you create or modify topics. Virtual Agent Designer does the following:

-   Only displays model groups that contain language models that reflect the user's current session.
-   Shows a warning if the selected model group has language mappings that will change existing language mappings, whether in another model group or in a single-language model.
-   Automatically maps intents in each language model in the group to the topic.
-   Ensures that duplicate model names or intent names are not used.
-   If a topic is mapped to a multilingual model group, hides single-language model groups on the **NLU Language Mapping** tab.

If languages in a topic are mapped to intents in more than one model group, conflicts may occur. An intent can only be mapped to one topic. If this situation occurs when you attempt to publish a topic, Virtual Agent Designer displays an error message.

**Parent Topic:**[Create a Virtual Agent topic](../task/create-virtual-agent-topic.md)

