---
title: Create country choices
description: Create additional country choices to select from in the Next Experience language and region preferences or a user record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/system-localization/create-country-choices.html
release: zurich
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-05-13"
reading_time_minutes: 1
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer]
---

# Create country choices

Create additional country choices to select from in the Next Experience language and region preferences or a user record.

## Before you begin

Role required: admin

## About this task

By default, you can select from only a limited list of countries in the Next Experience language and region preferences or in a User record. To allow users to select from additional countries, administrators can create additional choices for the Country code \[country\] field on the User \[sys\_user\] table.

## Procedure

1.  In the navigation filter, enter `sys_choice.list`.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Table|User \[sys\_user\]|
    |Element|country|
    |Language|Enter a [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry) language identifier. This field can contain a language code or a language code followed by a country or region code. For example, tr for Turkish or es-MX for Mexican Spanish.|
    |Label|Enter the name of the country in the specified language as you want it to appear in choice lists.|
    |Value|Enter the two-letter [ISO 3166-1 alpha-2](https://www.iso.org/obp/ui/#search) code for the country. For example, BR for Brazil.|
    |Sequence|Enter a number to determine what order the option appears in the list if you don't want to list choices alphabetically.|
    |Inactive|Leave cleared for the country choice to appear in the Next Experience language and region preferences or in a User record.|

    For more information about this table, see [Choice table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/system-localization/r_ChoicesTable.md).

    The following choice lets users select Canada as their country when the user or instance language is English.

    -   **Table**: User \[sys\_user\]
    -   **Element**: country
    -   **Language**: en
    -   **Label**: Canada
    -   **Value**: CA
4.  Select **Submit**.


