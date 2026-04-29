---
title: NLU language support
description: The NLU Workbench application provides support for creating NLU models in different languages for use in other applications, such as Virtual Agent.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Exploring Natural Language Understanding, Natural Language Understanding, Enable AI experiences]
---

# NLU language support

The NLU Workbench application provides support for creating NLU models in different languages for use in other applications, such as Virtual Agent.

The platform supports NLU for 17 languages. Ten of these languages available to your models have both intent and entity support; the remaining 7 languages have intent-only support. \(Japanese entity support includes character annotation.\)

**Note:** Install the language plugins for languages you want to use in NLU. Installing and activating language plugins ensures that the languages are available in your instance. For more information see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

<table id="table_wdv_ymx_z4b"><thead><tr><th>

Available in Tokyo, Utah, and Vancouver

</th><th>

Intent and entity support \(in Utah and Vancouver\)

</th><th>

Intent-only support \(in Utah and Vancouver\)

</th></tr></thead><tbody><tr><td>

-   Brazilian Portuguese
-   Chinese \(simplified\)
-   Danish
-   Dutch
-   English
-   Finnish
-   French
-   French Canadian
-   German
-   Italian
-   Japanese
-   Korean
-   Norwegian
-   Polish
-   Portuguese
-   Spanish
-   Swedish

</td><td>

-   Brazilian Portuguese
-   Dutch
-   English
-   French
-   French Canadian
-   German
-   Italian
-   Japanese
-   Portuguese
-   Spanish

</td><td>

-   Chinese \(simplified\)
-   Danish
-   Finnish
-   Korean
-   Norwegian
-   Polish
-   Swedish

</td></tr></tbody>
</table>With intent and entity support, NLU can understand sophisticated utterances such as intent-entity relationships, system entities, and user-defined entities. NLU relays this information to Virtual Agent, and the user is usually taken directly to the conversation topic that offers resolution.

With intent-only support, the focus is on intent recognition. With Virtual Agent using NLU, users are directed to the desired conversation topic, where qualifying follow-up questions may be asked before being taken to a topic that offers resolution.

Utterances for all languages are case insensitive during intent prediction.

Below is a detailed list of the currently available NLU languages and the intents, entities, vocabulary, features, and applications they support.

![A chart of NLU'scurrently available languages and the intents, entities, vocabulary, and features they support](../images/nlu-capabilities.png "Supported languages and features")

**Parent Topic:**[Exploring Natural Language Understanding](nlu-explore.md)

