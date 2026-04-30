---
title: NLU vocabulary
description: Use NLU vocabulary items to help the system recognize the various ways your users express their requests. Use vocabulary sources to help the system recognize objects in tables or lists, such as names of conference rooms or catalog items.
locale: en-US
release: yokohama
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# NLU vocabulary

Use NLU vocabulary items to help the system recognize the various ways your users express their requests. Use vocabulary sources to help the system recognize objects in tables or lists, such as names of conference rooms or catalog items.

![This image shows a robot serving a platter of linked molecules. The robot and everything else is saying 'NLU Vocabulary' in 6 different languages.](../images/using-nlu-vocabulary-parent-topic.png)

## Vocabulary usage and context

Vocabulary helps your model with the various words and phrases that it may encounter from your users. Since humans are not computers, they may come up with different ways to say the same thing. For example, if one user inputs an acronym rather than the full phrase, the system might be able to predict the correct intent by using the context in the utterance. However, by defining the acronym with a vocabulary item, you raise the model's confidence level and capability to predict intents correctly.

![The Build and train your model phase with the Vocabulary tab highlighted.](../images/using-nlu-vocabularyU2.png)

Vocabulary items cover the varying words or phrases that might appear in utterances. The vocabulary items are mapped to the synonyms that you provide, for intent prediction. This helps the system recognize the various ways your users express their requests, while at the same time ensuring the consistency, confidence, and accuracy of predictions.

## Vocabulary item types

NLU provides the following vocabulary types that you can use to create and configure a vocabulary item.

<table id="table_k3t_dzw_h5b"><thead><tr><th>

Type

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Regular

</td><td>

A word or phrase that is not commonly known, such as a business or industry specific term or acronym. Regular vocabulary is case insensitive, so all case variations will be captured by the vocabulary you create.

 See [Create a regular vocabulary item](../task/create-regular-vocabulary-item.md).

</td></tr><tr><td>

Pattern

</td><td>

A regular expression \(regex\) that can capture specific formats such as email addresses and phone numbers.

 See [Create a pattern vocabulary item](../task/create-pattern-vocabulary-item.md).

</td></tr></tbody>
</table>## Vocabulary sources

You can also use vocabulary sources to cover various objects that your users might request. Vocabulary items and vocabulary sources differ in their usage:

-   Use a vocabulary item for an individual word, phrase, or pattern that can easily be mapped to a single synonym for the model to use.
-   Use a vocabulary source to reference a ServiceNow table or list so that the values can all be replaced by the single synonym you define. Vocabulary sources can be reused across all your NLU models.

Use vocabulary sources when your user utterances refer to objects in a set. The sources can be referenced from a list of values from a ServiceNow table or a static list that you define, such as a list of catalog items or conference rooms. Once you create and save these sources, you can use the @ symbol to specify them in training utterances. You can also use these sources as entity values.

For example, say you already have a list of all the conference rooms for your office. You can create a vocabulary source to reference that list rather than typing each conference room name into your intent's training utterances.

To create vocabulary sources, refer to [Create a table vocabulary source](../task/create-table-lookup-source.md) and [Create a list vocabulary source](../task/create-static-list-source.md).

## Vocabulary usage in relation to an intent

Here's an example of how an intent can interact with the vocabulary in its utterance examples.

**Note:** In NLU vocabulary, the synonym replaces the vocabulary that appears in the utterance.

<table id="table_rn1_r4s_pwb"><thead><tr><th>

Utterance

</th><th>

Issue and Solution

</th></tr></thead><tbody><tr><td>

"I need to access sfcrm"

</td><td>

-   Issue: the system doesn't recognize the acronym sfcrm, so can't accurately predict the intent.
-   Solution: Add sfcrm as a regular vocabulary item, and provide a synonym such as CRM software.

</td></tr><tr><td>

"I need to install Word"

</td><td>

-   Issue: The term word is very common and does not necessarily indicate a software product. The term install may provide helpful context, but the confidence score may be too low to predict the OrderSoftware intent.
-   Solution: Create a pattern vocabulary item with a regex for capitalized Word, so that the system can recognize it as a software product. This added constraint makes it more likely that the OrderSoftware intent will be predicted.

**Note:** To extract the specific software name to use in a Virtual Agent conversation topic, annotate it as an entity in the utterance.


</td></tr></tbody>
</table>Use a single word or short phrase as a synonym for best results. You can map multiple vocabulary items to one synonym. Do not map one vocabulary item to multiple synonyms.

For more context and examples, see [Create an NLU intent](../task/create-nlu-intent.md).

## A Regex example for a pattern vocabulary item

Let's say that you want to use a vocabulary item to identify the acronym IT, and map it to the synonym information technology.

Regular vocabulary items are case-insensitive by default. This means that a regular vocabulary item would match both the acronym IT and the common word it. So you decide to use a pattern vocabulary item.

The regex pattern that you can use is `\bIT\b`. The `\b` is a word boundary marker. This ensures that the pattern would not match ITSM or JIT, for example. The default case sensitivity of pattern vocabulary items means that `\bIT\b` would not match the common word it.

Regex details: You can turn off case sensitivity in a pattern by using `(?i)`. You can end that mode by using a minus sign as in `(?-i)`. For example, `(?i)te(?-i)st` should match both test and TEst, but not teST or TEST.

For more information, see [Using regular expressions in entities](using-regular-expressions-nlu.md).

-   **[Create a regular vocabulary item](../task/create-regular-vocabulary-item.md)**  
Add a word or phrase that your users might use, and match that vocabulary item to a synonym. Your model uses the synonym during intent prediction.
-   **[Create a pattern vocabulary item](../task/create-pattern-vocabulary-item.md)**  
Use regular expression \(regex\) encoding to establish a pattern format for vocabulary items such as email addresses, phone numbers, and record naming conventions. You can create your own patterns for the vocabulary data in your instance.
-   **[Create a list vocabulary source](../task/create-static-list-source.md)**  
Create a list of words or phrases to act as a vocabulary source. The values in the list source are replaced by the synonym if they are detected in a user utterance.
-   **[Create a table vocabulary source](../task/create-table-lookup-source.md)**  
Use the values from a ServiceNow table as a vocabulary source. Your Natural Language Understanding \(NLU\) models use your provided synonym to interpret utterances that contain values from the chosen source fields of the table.
-   **[Sync a table vocabulary source](../task/sync-table-vocabulary-source.md)**  
Synchronize your table vocabulary sources to obtain the latest changes to the ServiceNow source table. Synchronizing your vocabulary sources ensures your NLU models have the latest values when predicting intents.
-   **[Pre-built vocabulary](prebuilt-vocabulary.md)**  
Use ServiceNow® pre-built vocabulary for software and hardware terms so the system recognizes their multiple variations in utterances.

**Parent Topic:**[Build and train your model](managing-model-content.md)

**Related topics**  


[Create an NLU intent](../task/create-nlu-intent.md)

