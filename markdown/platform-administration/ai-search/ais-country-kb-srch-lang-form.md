---
title: AI Search Country To Search Language form
description: The AI Search form contains information about relationships between user countries and knowledge article search languages. Use this form when defining knowledge article search languages for a country.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search Country To Search Language form

The AI Search form contains information about relationships between user countries and knowledge article search languages. Use this form when defining knowledge article search languages for a country.

For details on defining knowledge article search languages for a country, see [Assign Knowledge article search languages by country](../task/assign-kb-srch-langs-country-ais.md).

|Field|Description|
|-----|-----------|
|Country|Reference to the country from the Country \[core\_country\] table that you want to define an additional knowledge article search language for.|
|Search language|Reference to a language from the Language \[sys\_language\] table that you want AI Search to use for knowledge article searches by users in the selected country.|

**Note:** You can define multiple AI Search Country To Search Language records for the same country, as long as each one has a different knowledge article search language. If you attempt to create multiple records with the same country and the same knowledge article search language, the system displays a warning message and the record insert operation fails.

**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

