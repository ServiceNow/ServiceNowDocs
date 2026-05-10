---
title: Debug translations
description: Show which UI strings are translatable and their translation table to debug translations.
locale: en-US
release: australia
product: System Localization
classification: system-localization
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Locating translatable UI strings, Translating custom content, System Localization, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Debug translations

Show which UI strings are translatable and their translation table to debug translations.

## Before you begin

Role required: admin

## About this task

You can set translation prefixes to appear only in the current user session or to appear in all sessions.

Translation prefixes map to translation tables as follows.

|Prefix|Table|Navigation|
|------|-----|----------|
|TRF|Translated Name / Fields \[sys\_translated\]|**System Localization** &gt; **Translated Names / Fields**|
|MSG|Messages \[sys\_ui\_message\]|**System Localization** &gt; **Messages**|
|GMLD|Field Label \[sys\_documentation\]|**System Localization** &gt; **Field Labels**|
|TRT|Translated Text \[sys\_translated\_text\]|**System Localization** &gt; **Translated Text**|
|CHC|Choice \[sys\_choice\]|**System Localization** &gt; **Choices**|

**Note:** A few strings may not display translatable prefixes. In this case, the string is not stored on any of these tables. Examples of this behavior include:

-   Text embedded in images, such as the buttons in the Service Catalog.
-   Text defined by properties, such as the text which follows the banner.

## Procedure

1.  Enable translation prefixes on field labels.

    -   To enable prefixes for the current user session, navigate to **All** &gt; **System Localization** &gt; **Enable I18N Debugging**.
    -   To enable prefixes for all sessions, navigate to **All** &gt; **System Properties** &gt; **System Localization** and set **Display translation prefix on translatable strings** to **Yes**.

        ![Translation property.](../image/TranslationProperty.png)

2.  Refresh the page or change your user language to one of the non-English languages installed on your instance to see the prefixes.


## Result

When enabled, translation prefixes appear before translatable UI strings.

![The application navigator with MSG and TRF prefixes for the navigator and application strings.](../image/translation-prefix.png)

## What to do next

When you are done debugging, disable the translation prefixes.

-   To disable prefixes for the current user session, either log out of the session or navigate to **All** &gt; **System Localization** &gt; **Disable I18N Debugging**.
-   To disable prefixes for all sessions, navigate to **All** &gt; **System Properties** &gt; **System Localization** and set **Display translation prefix on translatable strings** to **No**.

**Related topics**  


[System Localization properties](../reference/set-localization-props.md)

