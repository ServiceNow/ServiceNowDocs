---
title: Activate country choices for users
description: Select from additional countries in the Next Experience language and region preferences or a user record.Create additional country choices to select from in the Next Experience language and region preferences or a user record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/system-localization/activate-country-choices.html
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring System Localization, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate country choices for users

Select from additional countries in the Next Experience language and region preferences or a user record.

## Before you begin

Role required: admin

## About this task

By default, you can select from only a limited list of countries in the Next Experience language and region preferences or in a User record. To allow users to select from additional countries, administrators can activate choices for the Country code \[country\] field on the User \[sys\_user\] table. For more information about the Country user preference, see [Configure Next Experience language and region preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-language-preferences.md).

## Procedure

1.  In the navigation filter, enter `sys_choice.list`.

2.  From the Choices list, use the condition builder to enter the following condition statement: **\[Table\] \[is\] \[sys\_user\] AND \[Element\] \[is\] \[country\] AND \[Inactive\] \[is\] \[true\]**.

3.  Select **Run**.

4.  Select the Choice record for the country that you want to activate.

5.  From the Choice record, clear the **Inactive** option.

6.  Select **Update**.


**Related topics**  


[Choice table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_ChoicesTable.md)

[User administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/c_UserAdministration.md)

## Create country choices

Create additional country choices to select from in the Next Experience language and region preferences or a user record.

### Before you begin

Role required: admin

### About this task

By default, you can select from only a limited list of countries in the Next Experience language and region preferences or in a User record. Beginning with the Australia release, administrators can activate additional choices for the Country code \[country\] field on the User \[sys\_user\] table. However, if the base system country choices were previously customized, the additional choices aren't available to activate after upgrading. Follow this procedure to create additional choices for countries that aren't available.

### Procedure

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

    For more information about this table, see [Choice table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_ChoicesTable.md).

    The following choice lets users select Canada as their country when the user or instance language is English.

    -   **Table**: User \[sys\_user\]
    -   **Element**: country
    -   **Language**: en
    -   **Label**: Canada
    -   **Value**: CA
4.  Select **Submit**.


