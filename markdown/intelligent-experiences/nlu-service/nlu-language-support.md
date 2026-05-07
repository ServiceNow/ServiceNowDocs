---
title: NLU language support
description: The NLU Workbench application provides support for creating NLU models in different languages for use in other applications, such as Virtual Agent.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 1
breadcrumb: [Exploring Natural Language Understanding, Natural Language Understanding, Enable AI experiences]
---

# NLU language support

The NLU Workbench application provides support for creating NLU models in different languages for use in other applications, such as Virtual Agent.

The platform supports NLU for 17 languages. Ten of these languages available to your models have both intent and entity support; the remaining 7 languages have intent-only support. \(Japanese entity support includes character annotation.\)

**Note:** Install the language plugins for languages you want to use in NLU. Installing and activating language plugins ensures that the languages are available in your instance. For more information see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

With intent and entity support, NLU can understand sophisticated utterances such as intent-entity relationships, system entities, and user-defined entities. NLU relays this information to Virtual Agent, and the user is usually taken directly to the conversation topic that offers resolution.

With intent-only support, the focus is on intent recognition. With Virtual Agent using NLU, users are directed to the desired conversation topic, where qualifying follow-up questions may be asked before being taken to a topic that offers resolution.

Utterances for all languages are case insensitive during intent prediction.

The following table lists the currently available NLU languages and the features supported for each language.

All languages support intents, vocabulary, batch testing, NLU performance, fast training, and Virtual Agent model use.

|Language|NLU feature supported|
|--------|---------------------|
|English|System-defined entities, user-defined entities, vocabulary sources, pre-built vocabulary, intent discovery, conflict review, expert feedback loop, Search model use.|
|French|System-defined entities, user-defined entities, vocabulary sources, intent discovery, conflict review, Search model use.|
|Spanish|System-defined entities, user-defined entities, vocabulary sources, intent discovery, conflict review, Search model use.|
|German|System-defined entities, user-defined entities, vocabulary sources, intent discovery, conflict review, Search model use.|
|Japanese|System-defined entities, user-defined entities, vocabulary sources, intent discovery, conflict review, Search model use.|
|Portuguese|System-defined entities, user-defined entities, vocabulary sources.|
|Swedish|Virtual Agent model use.|
|Italian|User-defined entities, vocabulary sources.|
|Chinese \(simplified\)|Virtual Agent model use.|
|Brazilian Portuguese|System-defined entities, user-defined entities, vocabulary sources.|
|Dutch|User-defined entities, vocabulary sources.|
|French Canadian|User-defined entities, vocabulary sources.|
|Polish|Virtual Agent model use.|
|Korean|Virtual Agent model use.|
|Danish|Virtual Agent model use.|
|Finnish|Virtual Agent model use.|
|Norwegian|Virtual Agent model use.|

