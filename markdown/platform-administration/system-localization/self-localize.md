---
title: Translating to an unsupported language
description: Translate the interface of an instance to a language for which ServiceNow does not provide an internationalization \(I18N\) plugin.
locale: en-US
release: yokohama
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 1
breadcrumb: [System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translating to an unsupported language

Translate the interface of an instance to a language for which ServiceNow does not provide an internationalization \(I18N\) plugin.

## Before you begin

You can download a file containing translatable strings from the [Translate an unsupported language - File Containing strings in the English Language \[KB0860203\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0860203) article in the Now Support Knowledge Base.

Role required: admin

## About this task

All interface items are stored as translatable strings in the translation tables. By default, these translation tables contain only English strings. To populate these tables with translated strings in an unsupported language, use the following workflow.

There is a very large number of translatable strings on the platform. Exporting all of them and translating them manually is probably not a realistic possibility. Consider exporting filtered subsets of the strings from each table and then translating them. To download a file of translatable strings, see [KB0860203](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0860203).

You can use the Localization Framework application to translate to an unsupported language or to translate large amounts of custom UI string content in a supported language. For more information, see [Localization Framework](../../localization-framework/concept/localization-framework-landing.md).

## Procedure

1.  [Create a language record](t_CreateANewLanguageRecord.md) for the unsupported language.

2.  Export and translate the strings that you want to translate, as described in [Export and edit translation records](t_TranslateTheInterface.md#).

3.  Import the translated document back into the instance as an import set, as described in [Import a translation from an Excel spreadsheet](t_TranslateTheInterface.md#).

4.  [Create a language choice for users](t_CreateANewChoiceRecord.md) to select the new language.


**Related topics**  


[Translation tables](../reference/r_TranslationTables.md)

