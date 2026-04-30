---
title: Assign Knowledge article search languages by country
description: Improve multilingual search recall by defining a set of Knowledge article search languages for each user country. User searches can match Knowledge articles in any of the search languages specified for their country as well as in the language associated with their ServiceNow AI Platform session.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-02-04"
reading_time_minutes: 2
breadcrumb: [Internationalization support, Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Assign Knowledge article search languages by country

Improve multilingual search recall by defining a set of Knowledge article search languages for each user country. User searches can match Knowledge articles in any of the search languages specified for their country as well as in the language associated with their ServiceNow AI Platform® session.

## Before you begin

Role required: ais\_admin

## About this task

By default, user searches only match Knowledge articles in the language associated with the user's ServiceNow AI Platform session. As an example, a user searching from a Japanese session only sees search results for Japanese-language Knowledge articles.

Search administrators can expand the recall of Knowledge article searches for a country's users by specifying additional Knowledge article search languages for that country. For example, suppose you specify the Knowledge article search languages English and French for the country of Japan. With these country-to-language mappings in place, a user searching from a Japanese session can see search results for Knowledge articles in English and French as well as for articles in Japanese.

## Procedure

1.  Navigate to the AI Search Country To Search Language \[ais\_country\_to\_search\_language\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `ais_country_to_search_language.list`.

    3.  Press Enter.

2.  For each Knowledge article search language that you want to map to a country, create a new record in the table.

    1.  Select **New**.

    2.  On the AI Search Country To Search Language form, fill in the fields.

        For a description of the field values, see [AI Search Country To Search Language form](../reference/ais-country-kb-srch-lang-form.md).

    3.  Select **Submit**.

        **Note:** You can define multiple AI Search Country To Search Language records for the same country, as long as each one has a different Knowledge article search language. If you attempt to create multiple records with the same country and the same Knowledge article search language, the system displays a warning message and the record insert operation fails.


## Result

When users in a country with one or more Knowledge article search languages defined perform a search, they can match Knowledge articles in those search languages as well in the language associated with their ServiceNow AI Platform session.

**Parent Topic:**[Internationalization support for AI Search](../concept/international-language-support-ais.md)

