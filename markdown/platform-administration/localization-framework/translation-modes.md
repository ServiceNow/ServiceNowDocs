---
title: Translation modes
description: The Localization Framework offers various translation modes for content translation. Localization fulfillers can use one of the translation modes to translate content and fulfill localization requests.
locale: en-US
release: yokohama
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Localization Framework reference, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translation modes

The Localization Framework offers various translation modes for content translation. Localization fulfillers can use one of the translation modes to translate content and fulfill localization requests.

## Machine Translate

Machine translation in the Localization Framework is powered by Dynamic Translation.

Activate the required translation service provider in the instance to machine translate the content. For information, see [Create a custom translator configuration](../../dynamic-translation/task/create-custom-translator.md).

## Send to Translation Management Systems

The Localization Framework integrates with third-party Translation Management Systems \(TMS\) to localize the content.

RWS and XTM Translation Management Systems are supported by default and requires configuration. For more information see, [Configure RWS TMS in the Localization Framework](../task/configure-sdl-tms.md) and [Configure XTM TMS in the Localization Framework](../task/configure-xtm-tms.md).

You can configure a custom Translation Management System of your choice. For more information, see [Create a custom translation management system](../task/create-custom-tms.md).

When the Localization Framework Hub and Spoke architecture is installed, the TMS must be configured accordingly. For more information, see [Localization Framework Hub and Spoke architecture](localization-framework-hub-spoke-architecture.md).

Zip attachment should be supported on the instance. For more details on attachment configuration, see [Configure system attachment properties](../../form-administration/task/t_DisablingTheDragAndDropFeature.md#)

## Send via Email

The Localization Framework provides **Send via Email** as a translation mode that can be used to send the translatable content for translation to a TMS service via email.

If you have more than one requested item in a task, then the requested CSV or XLIFF items are compressed into one ZIP file and attached to the email. Either CSV or XLIFF attachment should be supported on the instance. For more details on attachment configuration, see [Configure system attachment properties](../../form-administration/task/t_DisablingTheDragAndDropFeature.md#)

You can configure the **Send via Email** mode as a translation preference for one or more activated languages. For more information see, [Configure Localization Framework settings](../task/define-translation-preferences.md).

## Export/Import

Localization Framework supports the following translation modes:

-   **Export**: Export the translatable content for translation to a TMS service. If you have more than one requested item in a task, the individual CSV or XLIFF files are compressed and downloaded as one zip file.
-   **Import**: Import the translated content from a TMS service. If you have more than one requested item in the task, you can import individual CSV or XLIFF files or in a ZIP format. Any files unrelated to the task are skipped.

Either CSV or XLIFF attachment should be supported on the instance. For more details on attachment configuration, see [Configure system attachment properties](../../form-administration/task/t_DisablingTheDragAndDropFeature.md#)

**Parent Topic:**[Localization Framework reference](reference-localization-framework.md)

