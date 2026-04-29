---
title: Translatable fields in dashboard elements
description: For fields that show the Translatable turned on badge, you can add translations of the field value in the Messages \[sys\_ui\_message\] table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Translatable fields in dashboard elements

For fields that show the **Translatable turned on** badge, you can add translations of the field value in the Messages \[sys\_ui\_message\] table.

Translations of ServiceNow AI Platform® User interface \(UI\) elements are stored in one of five tables, as described in [Translation tables](https://www.servicenow.com/docs/access?context=r_TranslationTables&version=australia&pubname=australia-platform-administration&ft:locale=en-US). When you see a field in the configuration panel of a dashboard element, and this field has the badge **Translatable turned on**, you can add translations of the field value in the Messages \[sys\_ui\_message\] table.

In the Messages table, records have a key, a language, and a message field. You set the key value equal to the original text. Then you select a language, and enter the translation in that language into the Message field. Only ServiceNow AI Platform admins can create and edit these records. For more information, see [Translate a client script message](https://www.servicenow.com/docs/access?context=t_TranslateAClientScriptMessage&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** For more information about how keys are stored for translatable fields, see this [ServiceNow Community blog post](https://www.servicenow.com/community/international-localization/need-to-translate-a-configurable-workspace-check-this/ta-p/2376015?nobounce). This post also includes a prototype Localization Framework artifact that finds all translatable fields in all UI Builder components on an instance, including dashboard components.

**Parent Topic:**[Dashboard reference](../../par-for-workspace/concept/dashboard-reference-page.md)

