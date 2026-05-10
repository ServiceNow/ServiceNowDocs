---
title: Configure Dynamic translation for Universal Request
description: Activate and configure the Dynamic Translation plugin to translate the text on a Universal Request record.
locale: en-US
release: australia
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Configure Dynamic translation for Universal Request

Activate and configure the Dynamic Translation plugin to translate the text on a Universal Request record.

## Before you begin

Role required: admin

## About this task

After activating the Dynamic Translation plugin, you can configure one of the translator service spokes available by default. You can also configure a custom translator service provider. For more information on translation service providers, see [Integration with other translation services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/integration-with-other-translation-services.md).

## Procedure

1.  Activate the Dynamic Translation plugin.

    For more information, see [Activate Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/activate-dynamic-translation.md).

2.  Configure and activate the translator configuration for the spoke you are using.

    Available spokes include the following.

    -   [Configure Microsoft Azure Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/microsoft-translation-spoke.md)
    -   [Configure Google Cloud Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/google-translator-spoke.md)
3.  Activate the I18N plugin for the specific language you want to translate to.

    For a list of available languages, see [Activate a Language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/t_ActivateALanguage.md).


**Parent Topic:**[Configuring Universal Request](../concept/configure-ur.md)

