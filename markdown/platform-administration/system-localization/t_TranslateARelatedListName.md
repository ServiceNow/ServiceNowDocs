---
title: Translate a related list name
description: Related lists appear at the bottom of forms. You can translate a related list name by configuring the list control.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translating individual UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translate a related list name

Related lists appear at the bottom of forms. You can translate a related list name by configuring the list control.

## Before you begin

Role required: personalize\_control

## Procedure

1.  Use the language picker to switch to the desired language.

2.  Navigate to the related list on the form.

3.  Open the list control for the related list by performing the appropriate action for the list version.

    |Version|Action|
    |-------|------|
    |**List v2**|Right-click any column heading and select **Configure** &gt; **List Control**.|
    |**List v3**|Open the list title menu and select **List Control**.|

4.  On the List Control form, replace the existing Label with the text of the target language.

5.  Select **Submit** or **Update**.

    The system creates a new entry in the Translated Name / Field \[sys\_translated\] table or updates the existing entry for this language. For more information about this table, see [Translated Name / Field table](../reference/r_TranslatedNameFieldTable.md).


