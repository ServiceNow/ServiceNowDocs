---
title: Create a language choice for users
description: Allow users to select the language as a valid option in the language picker or a user record.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translating to an unsupported language, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a language choice for users

Allow users to select the language as a valid option in the language picker or a user record.

## Before you begin

Role required: admin

## About this task

You must create a choice record for a new translation in the Choice \[sys\_choice\] table. For more information about this table, see [Choice table](../reference/r_ChoicesTable.md).

## Procedure

1.  Navigate to **All** &gt; **System Localization** &gt; **Choices**.

2.  Select **New**.

3.  Enter the following fields.

    |Field|What to enter|
    |-----|-------------|
    |Table|`sys_user`|
    |Element|`preferred_language`|
    |Language|Enter an identifier that complies with [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry). The identifier can contain a language code or language code followed by a country or region code. For example, tr for Turkish or es-MX for Spanish Mexico.|
    |Label|Enter the name of the new language selection as you want it to appear in the language picker. For example, Mongolian.|
    |Value|Enter an identifier that complies with [BCP 47](http://www.iana.org/assignments/language-subtag-registry/language-subtag-registry). The identifier can contain a language code or language code followed by a country or region code. For example, tr for Turkish or es-MX for Spanish Mexico.|
    |Sequence|Enter a number to determine what order the option appears in the choice list if you do not want to list choices alphabetically. For example, 5.|

    The following record allows a user who is using the Dutch localization of their instance to change languages to Mongolian:

    -   **Table:** User \[sys\_user\]
    -   **Element:** preferred\_language
    -   **Language:** nl
    -   **Label:** Mongoolse
    -   **Value:** mn
4.  Select **Submit**.


**Related topics**  


[Choice table](../reference/r_ChoicesTable.md)

