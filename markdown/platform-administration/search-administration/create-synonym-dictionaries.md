---
title: Create synonym dictionaries
description: You can create synonym dictionaries to expand Zing text searches with additional search keywords.
locale: en-US
release: xanadu
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Zing can expand search results with synonyms, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create synonym dictionaries

You can create synonym dictionaries to expand Zing text searches with additional search keywords.

## Before you begin

Role required: ts\_admin or admin

## About this task

By default, the system provides a sample Zing synonym dictionary called **Example synonym dictionary**. You can add synonyms to this dictionary or create your own synonym dictionaries.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Text Index Synonym Dictionaries**.

2.  Select **New**.

3.  On the Synonym Dictionary form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Unique name for the synonym dictionary.|
    |Active|Option to make the synonym dictionary active. Zing only uses active synonym dictionaries when expanding searches.|
    |Global|Option to use the synonym dictionary for searches against all tables that have not been individually configured.|
    |State|Publication state for the synonym dictionary. This field is read-only.|
    |Order|Order of evaluation for the synonym dictionary. Zing evaluates synonym dictionaries with lower **Order** values before dictionaries with higher values.|
    |Description|Description of the synonym dictionary.|

4.  For each set of synonyms you want to add to the synonym dictionary, insert a new Synonym Set row and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Synset|Comma-separated set of synonym expansions. Zing expands searches containing any one of these terms to include all of these terms. As an example, if you define the synonym set `medicalise,médicalisé` and search for `medicalise`, Zing expands your search to match records containing either `medicalise` or `médicalisé`.|
    |Active|Option to make this synonym set active. Zing only uses active synonym sets when expanding searches.|
    |Description|Description of the synonym set.|

5.  Select **Submit**.

6.  Select the **Publish All Dictionaries** related link.

    A message indicates that publication of your synonym dictionaries has been scheduled. Refresh the page to see whether publication is complete. The dictionary is published when its state changes from **Draft** to **Published**.


**Parent Topic:**[Zing can expand search results with synonyms](../concept/search-synonyms-expand-results.md)

**Related topics**  


[Enable search synonyms](enable-text-index-synonyms.md)

[Select synonym dictionaries for a table](select-synonym-dictionaries.md)

[Disable synonyms for a table](disable-synonyms-for-a-table.md)

[Debug synonym searches](debug-synonym-searches.md)

