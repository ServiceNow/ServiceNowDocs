---
title: Configuring translation for Content Publishing after upgrade
description: Content Publishing supports multi-lingual content creation by enabling content managers to easily change the interface language and request content translation through the Localization Framework.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Localization Framework for Content Publishing, Setup employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configuring translation for Content Publishing after upgrade

Content Publishing supports multi-lingual content creation by enabling content managers to easily change the interface language and request content translation through the Localization Framework.

For more information on multiple language support in the Content Library, see [Multilingual support in the Content Library](ec-switch-language.md).

For information on translating custom widgets, see [Translate a client script message](https://www.servicenow.com/docs/access?context=t_TranslateAClientScriptMessage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

-   Translation is available through Content Publishing versions 21.0.15 and later.
-   When upgrading your version of Content Publishing, you will not automatically receive translations support for all fields. The following tables are not updated to use translated text instead of the original type field:

    -   Portal Content \(sn\_cd\_content\_portal\)
    -   Block Content \(sn\_cd\_block\)
    -   To-Do Content \(sn\_cd\_content\_todo\)
    -   News Content \(sn\_cd\_content\_article\)
    -   Notification Content \(contains emails \) \(sn\_cd\_content\_notification\)
    Admins can manually enable the changes to the tables to use translations. Go into the table definitions \(sys\_db\_object\) for each table and change the field types to Translated Text or Translated HTML.

    **Warning:** Before you change the field types for a table, ensure you perform a back up your data into another column or by exporting the data first. This is a safe guard against losing any data.


The tables and fields that require changing are:

|Table|Field|Original type|New type|
|-----|-----|-------------|--------|
|Portal Content \(sn\_cd\_content\_portal\)|button\_text|String|Translated Text|
|Portal Content \(sn\_cd\_content\_portal\)|link\_text|String|Translated Text|
|Portal Content \(sn\_cd\_content\_portal\)|rich\_text|HTML Script|Translated HTML|
|Rich Content HTML \(sn\_cd\_content\_portal\)|headline|HTML|Translated HTML|
|Rich Content HTML \(sn\_cd\_content\_portal\)|heading\_text|String|Translated Text|
|Block Content \(sn\_cd\_block\)|rich\_text|HTML|Translated HTML|
|Block Content \(sn\_cd\_block\)|rich\_text\_user\_specific|HTML Script|Translated HTML|
|To-do Content \(sn\_cd\_content\_todo\)|button\_text|String|Translated Text|
|News Content \(sn\_cd\_content\_article\)|headline|String|Translated Text|
|News Content \(sn\_cd\_content\_article\)|rich\_content\_html|HTML|Translated HTML|
|News Content \(sn\_cd\_content\_article\)|title|String|Translated Text|
|Notification Content \(sn\_cd\_content\_notification\)|rich\_text\_plain\_html|HTML|Translated HTML|
|Notification Content \(sn\_cd\_content\_notification\)|subject|String|Translated Text|
|Notification Content \(sn\_cd\_content\_notification\)|description|String|Translated Text|

