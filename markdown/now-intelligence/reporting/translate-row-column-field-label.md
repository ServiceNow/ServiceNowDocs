---
title: Translate a report’s grouping labels
description: When executing reports that group results by a Translated Text field, to ensure that individual field labels and values display as translated, use the translated\_text type.
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Translate a report’s grouping labels

When executing reports that group results by a Translated Text field, to ensure that individual field labels and values display as translated, use the translated\_text type.

**Note:** Reporting only supports columns of type translated\_text.

When executing reports, for example multi-level pivot or bar reports, that group results by a Translated Text field, the labels may not all display as translated when the instance language is changed from English to another language. These field labels are entries from the [Translated Name / Field Table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslatedNameFieldTable.md).

Translation errors can occur when translating more than the first row or column of a report, or when creating a custom field for grouping. Use the translated\_text type to [Translate individual field labels and values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/c_TranslateIndFieldLabelsAndValues.md). See [Report types](../reference/report-types-creation-details-rd.md) for grouping options available from the Configure tab for the specific report type.

If you create a custom field for a report, the label is not added automatically. You need to add the label in the [Field Label table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_FieldLabelTable.md) and manually [Translate a field label](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_TranslateAFieldLabel.md).

**Parent Topic:**[Administering reports](c_AdminsteringReports.md)

**Related topics**  


[Translation tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/r_TranslationTables.md)

[Translating text fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/c_UseTranslatedText.md)

[Internationalization support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/c_LangInternationalizationSupport.md)

