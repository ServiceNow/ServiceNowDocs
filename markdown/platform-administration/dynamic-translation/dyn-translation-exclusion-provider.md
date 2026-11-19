---
title: Add an Exclusion Provider Pattern
description: As part of the configuration of Exclusion Framework in Dynamic Translation, enter the tags used by your translation provider to mark text that should not be machine translated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/dynamic-translation/dyn-translation-exclusion-provider.html
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exclusion Framework in Dynamic Translation, Configuring Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Add an Exclusion Provider Pattern

As part of the configuration of Exclusion Framework in Dynamic Translation, enter the tags used by your translation provider to mark text that should not be machine translated.

## Before you begin

Consult your machine translator provider's documentation or account portal to obtain the tags it uses to mark text strings for exclusion from translation.

Role required: admin

## About this task

The Exclusion Provider Pattern \[sn\_dt\_provider\_exclusion\_pattern\] table stores the exclusion tags used by machine translation providers. From this table's list view, select the value in the Active column to view a record. \(Selecting the value in the Translator Configuration column opens the corresponding Translator Configuration table entry in Dynamic Translation\).

\[Omitted image "dyn-translation-exclusion-provider3X.png"\] Alt text: To open a record, use the value in the Active column on the list view of Exclusion Provider Pattern.

By default Exclusion Framework provides an Exclusion Provider Pattern record for Microsoft. If you have a different machine translation service, use the following procedure to add its exclusion pattern.

## Procedure

1.  Ensure that you are in the application scope that you want for your record, then navigate to **All** &gt; **Dynamic Translation** &gt; **Exclusion Framework** &gt; **Exclusion Provider Pattern**.

2.  Select **New** to open **Exclusion Provider Pattern New record**.

    \[Omitted image "dyn-translation-exclusion-provider2X.png"\] Alt text: The New record form on the Exclusion Provider Pattern table.

3.  On the form, configure the fields according to the following guidance.

    |Field|Value|
    |-----|-----|
    |Translator Configuration|Select your third-party translation provider. You can use the look-up icon \(\[Omitted image "icon-lookup-using-list.png"\] Alt text: Lookup using list icon.\), or start typing the name into the field. The available records are pulled from Dynamic Translation's Translator Configurations table.|
    |Prefix pattern|The start or opening tag to mark a text string for exclusion.|
    |Suffix pattern|The end or closing tag of an excluded text string.|
    |Application|Displays the application scope in which this record was created. This value can't be edited.|
    |Active|Select this check box to activate, or clear the check box to deactivate.|

4.  Select **Submit** to save the record.


**Parent Topic:**[Exclusion Framework in Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/dynamic-translation/dyn-translation-exclusion-framework.md)

