---
title: Authoring Virtual Agent conversations for localization
description: Use localization methods in your Virtual Agent scripts to ensure that the content can be translated. Localization methods are designed to show the original text when no translation is found. These methods can be applied to your code before you have created translations.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Localizing Virtual Agent conversations, Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Authoring Virtual Agent conversations for localization

Use localization methods in your Virtual Agent scripts to ensure that the content can be translated. Localization methods are designed to show the original text when no translation is found. These methods can be applied to your code before you have created translations.

## Localization method for message content

The `gs.getMessageLang` method checks the Message table \[sys\_ui\_message\] for a translated version of the text in the language selected for the current user. If a translated version isn't found, the default language \(English\) is returned.

This code provides a greeting that dynamically adds the value of the `first_name` variable.

```
(function execute() {
        return 'Hi there ' + vaInputs.first_name;
})()
```

The following example shows that same code rewritten for localization.

```
(function execute() {
         return gs.getMessageLang('Hi there {0}', vaContext.getRequesterLang()), [vaInputs.first_name]);
})()
```

The second example uses the `gs.getMessageLang` method. The text is the same as the previous example, but the format is changed. The number in brackets acts as a placeholder for the variable, which is then listed in an array after the comma: `[vaInputs.first_name]`. The `gs.getMessageLang` method searches for a record on the Message table with a key value matching `Hi there {0}` and a language value matching the requester's language. The method returns the translated version of the text, which is stored in the **Message** field of the record.

**Note:** Language values use ISO standard two-character language codes. For more information, see [ISO 639.1 language codes](http://www.loc.gov/standards/iso639-2/php/code_list.php).

![A translation record in the Message table displays the Key column, language, translated Message, and the date the record was updated.](../images/message-table-example.png "Example translation record in the Message table")

**Note:** Content is translated only for published topics. Content does not appear translated when previewing unpublished topics.

**Parent Topic:**[Localizing Virtual Agent conversations](localize-va-topic.md)

