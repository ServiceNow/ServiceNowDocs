---
title: Use Localization Framework for Document Templates
description: Translate content in Document Templates and document blocks Localization Framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/hr-service-delivery/doc-lzt-fm.html
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Document blocks in Document Templates, Document Templates of type HTML, Configure, Document Templates, HR Documents, HR Service Delivery, Employee Service Management]
---

# Use Localization Framework for Document Templates

Translate content in Document Templates and document blocks Localization Framework.

## Before you begin

-   Role required: sn\_doc.admin
-   Install the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\).
-   Configure Localization Framework with the required artifacts. See [Artifact Configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/localization-framework/framework-configuration.md) for more information.
-   Activate the required languages and configure them with Localization Framework. For more information, see [Activate a language](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/system-localization/t_ActivateALanguage.md).
-   If you want to use machine translators, activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\). Configure the Dynamic Translation framework for the translation service provider. For more information, see [Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/dynamic-translation/dynamic-translation-overview.md).

## Procedure

1.  Select a document template or a document block.

2.  Click **Translate**.

    **Note:** If the Dynamic Translation application is installed, the **Machine Translate** button appears. The configured machine translator converts only the content \(in the document template or document block\) to the required language, but not the token values.

3.  Select a target language and start to manually translate the text in the space given.

    \[Omitted image "doc-lzt-fm.png"\] Alt text: Translate content in Document Blocks or Document Templates

4.  Click **Publish Translations**.

    A copy of the source template is created and moved to Draft state.


