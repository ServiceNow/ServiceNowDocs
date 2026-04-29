---
title: Translation modes
description: Localization Framework offers several translation modes for completing localization tasks. As a localization admin, you can select one or more of these modes when configuring the procedures for localization tasks.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2026-03-20"
reading_time_minutes: 4
breadcrumb: [Localization Framework reference, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Translation modes

Localization Framework offers several translation modes for completing localization tasks. As a localization admin, you can select one or more of these modes when configuring the procedures for localization tasks.

## Overview of translation modes in Localization Framework

Translation modes available to localization tasks include machine translation, translation management systems \(TMS\), send via email, and export/import. These modes apply to localization tasks that are not fulfilled manually, so they are described as Auto Translation.

As a localization admin, you can configure these modes when configuring localization tasks in the [Settings](localization-settings.md) \[sn\_lf\_setting\] table's web form. The modes that you enable and configure in the **Translation Preferences** tab become options for selection in the **Workflow Preferences** tab, under **Auto translation mode**.

-   Before starting configuration of Translation Preferences in Settings, finish any applicable prerequisites such as setting up a machine translator service or TMS, enabling file formats for email, and so forth.
-   Complete Translation Preferences in Settings before configuring the next tab, **Workflow Preferences**.

These translation modes also constrain the methods available to translation requests in [Localization Workspace](../../localization-workspace/concept/localization-workspace.md). Translation modes must be enabled in Localization Framework before they are available in the translation request wizard of Localization Workspace.

## Machine Translation

Machine translation in Localization Framework is powered by [Dynamic Translation](../../dynamic-translation/concept/dynamic-translation-overview.md).

Activate the required translation service provider in the instance to machine translate the content. For information, see [Integration with other translation services](../../dynamic-translation/concept/integration-with-other-translation-services.md).

## Translation Management System

Localization Framework integrates with third-party Translation Management Systems \(TMS\) to localize the content.

RWS and XTM Translation Management Systems are supported by default and require configuration. For more information see, [Configure RWS TMS in the Localization Framework](../task/configure-sdl-tms.md) and [Configure XTM TMS in the Localization Framework](../task/configure-xtm-tms.md).

Alternatively, you can configure a custom TMS of your choice. For more information, see [Create a custom translation management system](../task/create-custom-tms.md).

When the Localization Framework Hub and Spoke architecture is installed, the TMS must be configured accordingly. For more information, see [Localization Framework Hub and Spoke architecture](localization-framework-hub-spoke-architecture.md).

Zip attachments must be supported on the instance. For details on attachment configuration, see [Configure system attachment properties](../../form-administration/task/t_DisablingTheDragAndDropFeature.md#).

## Send via Email

Localization Framework provides **Send via Email** as a translation mode that can be used to send content for translation.

If you have more than one requested item in a task, then the requested CSV or XLIFF items are compressed into one ZIP file and attached to the email. Either the CSV or XLIFF attachment format must be supported on the instance. For details on attachment configuration, see [Configure system attachment properties](../../form-administration/task/t_DisablingTheDragAndDropFeature.md#).

## Export/Import

Localization Framework supports the following translation modes:

-   **Export**: Export the translatable content for translation to a TMS service. If you have more than one requested item in a task, the individual CSV or XLIFF files are compressed and downloaded as one zip file.
-   **Import**: Import the translated content from a TMS service. If you have more than one requested item in the task, you can import individual CSV or XLIFF files or in a ZIP format. Any files unrelated to the task are skipped.

Either the CSV or the XLIFF attachment format must be supported on the instance. For details on attachment configuration, see [Configure system attachment properties](../../form-administration/task/t_DisablingTheDragAndDropFeature.md#).

**Parent Topic:**[Localization Framework reference](reference-localization-framework.md)

**Related topics**  


[Requesting translations in Localization Workspace](../../localization-workspace/concept/requesting-translations-localization-workspace.md)

[Translation Management System configurations](tms-configuration.md)

