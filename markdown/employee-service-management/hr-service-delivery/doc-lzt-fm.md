---
title: Use Localization Framework for Document Templates
description: Translate content in Document Templates and document blocks Localization Framework.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Document blocks in Document Templates, Document Templates of type HTML, Configuring Document Templates, Document Templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Use Localization Framework for Document Templates

Translate content in Document Templates and document blocks Localization Framework.

## Before you begin

-   Role required: sn\_doc.admin
-   Install the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\).
-   Configure Localization Framework with the required artifacts. See [Artifact Configurations](https://www.servicenow.com/docs/access?context=framework-configuration&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) for more information.
-   Activate the required languages and configure them with Localization Framework. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).
-   If you want to use machine translators, activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\). Configure the Dynamic Translation framework for the translation service provider. For more information, see [Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Procedure

1.  Select a document template or a document block.

2.  Click **Translate**.

    **Note:** If the Dynamic Translation application is installed, the **Machine Translate** button appears. The configured machine translator converts only the content \(in the document template or document block\) to the required language, but not the token values.

3.  Select a target language and start to manually translate the text in the space given.

    ![Translate content in Document Blocks or Document Templates](doc-lzt-fm.png)

4.  Click **Publish Translations**.

    A copy of the source template is created and moved to Draft state.


