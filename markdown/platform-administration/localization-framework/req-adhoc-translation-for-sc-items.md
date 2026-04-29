---
title: Request adhoc translation for Service Catalog items
description: Request adhoc translations for Service Catalog items to localize them from English into one or more languages using the edit translations option. After you make the changes, you can publish the translations.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Request translations, Request translations, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Request adhoc translation for Service Catalog items

Request adhoc translations for Service Catalog items to localize them from English into one or more languages using the edit translations option. After you make the changes, you can publish the translations.

## Before you begin

The Localization Framework for Service Catalog plugin \[com.glide.localization\_framework.service\_catalog\] must be installed for the Edit Translations button to appear on the service catalog form.

Roles required:

-   localization\_editor: To request translations
-   catalog\_admin: To access the Service Catalog items \[sc\_cat\_item\] table.
-   catalog\_editor \(or catalog\_manager\) if you are the editor or manager of the item that is being translated: To access the Service Catalog items \[sc\_cat\_item\] table.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Maintain Items**.

2.  Select the item for which you want to request adhoc translations.

3.  Click **Edit Translations**.

    The adhoc comparison UI of Localization Framework is displayed.

4.  On the adhoc comparison UI of Localization Framework, you can use the followings options.

    |Option|Description|
    |------|-----------|
    |**Machine Translations**|Translate the catalog items using machine translations. You must configure machine translations in Localization Framework settings to use this option. For more information about machine translation, see [Create a translator configuration](../../dynamic-translation/task/create-custom-translator.md).|
    |**Export Source File**|Option to export files for translation. To export files, click **Export Source File**, choose the file type, and then click **Export File**.|
    |**Import Source File**|Option to import translated files to update the translation. To import files, from the **Export Source File** list, select **Import Translated File**.|

    **Note:**

    The options displayed on the adhoc comparison UI of Localization Framework are based on the Localization Framework **Settings**.

5.  After your changes are completed, click **Publish Translations**.


**Parent Topic:**[Request translations](../concept/language-picker-ui.md)

