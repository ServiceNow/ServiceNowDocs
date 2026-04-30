---
title: Integration with Localization Framework
description: Language translation fulfillers can provide translations faster and more efficiently by integrating with Localization Framework.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring translation for Content Publishing after upgrade, Reference, Employee Center, Employee Service Management]
---

# Integration with Localization Framework

Language translation fulfillers can provide translations faster and more efficiently by integrating with Localization Framework.

Content creators can initiate a translation workflow to request their content to be translated from Content Publishing and includes portal, block, notification, and to-do content.

**Note:** Only existing translatable content types are supported. Calendar is not supported.

Supported Content Publishing tables are able to communicate to Localization Framework via artifact records and scripts. This allows you to set up how you want your content to be translated.

For more information on Localization Framework, see [Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **Language plugin**

    Content Experiences and Content Publishing uses UTF-8 for international characters when at least one language plugin has been activated.

    Localization Framework should install automatically when a language plugin is installed.

    For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **Enable Localization Framework**

    To use Localization Framework with Content Publishing, enable the sn\_cd.enable\_localization\_framework\_integration system property. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

    When you activate the sn\_cd.enable\_localization\_framework\_integration system property, created content from the Content Library displays the **Translate content** button. This allows you to request translation for the content to the language you selected.

    **Note:** If you do not see the sn\_cd.enable\_localization\_framework\_integration system property, ensure Localization Framework is installed and you have the Content Admin \(sn\_cd.content\_admin\) role.

-   **Workflows in the Localization Framework**

    You can configure how translations are handled using the workflows provided in Localization Framework. You can configure how translations are processed using workflows. This ranges from a manual process to an automatic translation and automatic publication.

    For more information, see [Workflows in the Localization Framework](https://www.servicenow.com/docs/access?context=workflow-localization-framework&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **Translation modes**

    There are various translation modes you can use, like machine translations, send to a translation management system, send via email, or export/import. For more information, see [Translation modes](https://www.servicenow.com/docs/access?context=translation-modes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

-   **Translate content**

    Content creators can initiate a translation workflow to request their content to be translated from Content Publishing.

    **Note:** The translation workflow your company has chosen determines how translations are performed. The following provides instructions on how the base system process works.

    -   Create or select existing content from the Content Library or **Block Content** under **Re-usable Components**. For more information, see [Content Library](ec-streamline-content.md) or [Add or modify block content](../task/ecpro-manage-block-content.md)

        From the **Design** tab of **Content Preview**, select the **Translate content** button to initiate the translation workflow your company has configured.

    -   Or, from **Content Categories**, select a category.
        -   Create or select existing content you want translated from the list.
        -   Select the **Translate content** button to initiate the translation workflow your company has configured.
    -   You can also select **Link Content** or **Block Content** from **Re-usable Components**.
        -   For **Link Content**, select the content under the **Portal Content** tab.
        -   Select the **Translate content** button to initiate the translation workflow your company has configured.
        -   For more information, see [Reusable components](ec-re-usable-components.md).
    -   Select the language you want your content translated to from the **Translate content** modal that appears.
    -   Select **Submit** and a translation request is sent.
    -   Translation requests appear in the **Localization Requested Items** list under **My Requested Items** under Localization Framework.
        -   There is one localization request item \(LRITM with a sequential number\) for each language selected.
        -   You can find assigned localization request items from **My Requested Items** under **Localization Framework**.
        -   To see a list of all localization request items from **My Requested Items** under **Localization Framework**, change the filter to **All**.
    -   Each localization request item also has an associated localization task \(LFTASK is the prefix with a sequential number\).
        -   You can find all localization tasks from **My Tasks** under **Localization Framework**. To see a list of all localization tasks, change the filter to **All**.
        -   Localization tasks can be assigned to individuals with the localization\_fulfiller role or a group that has this role.
        -   Individuals or groups assigned to localization tasks, can provide translations from the **Localization Task** form and selecting the **Translate button**.
        -   After providing the translation, select the **Publish Translations** button.

            **Note:** Selecting **Publish Translations** does not publish the content, but creates the translation for the content. To publish your content with the published translations, you must schedule and publish your content. For more information, see [Create a publish plan for your content](../task/ec-content-library-publish2.md).

        -   For more information, see [Fulfill a localization task](https://www.servicenow.com/docs/access?context=fulfill-localization-task&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

**Parent Topic:**[Configuring translation for Content Publishing after upgrade](ec-multiple-language-support.md)

