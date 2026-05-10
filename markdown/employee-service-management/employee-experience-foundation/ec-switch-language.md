---
title: Multilingual support in the Content Library
description: The Content Library includes two features for multilingual content creation: Translate content \(content translation workflow\) and Switch language \(changes the interface language\).
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Creating employee communications, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Multilingual support in the Content Library

The Content Library includes two features for multilingual content creation: Translate content \(content translation workflow\) and Switch language \(changes the interface language\).

## Switch language vs Translate content

When the Translations and Language switching properties are enabled, the Content Library has two language settings options:

-   **Switch language**

    The Switch language option enables content creators to change the language of the Content Library interface \(similar to changing the system language setting\).

-   **Translate content**

    The Translate content option sends the content for translation in the specified language.


For more information on the properties, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

## Translating content in the Content Library

After you are done creating content, you can initiate the translation workflow to request translation for your portal, block \(re-usable components\), notification, or to-do content.

**Note:** At this time, translation is not available for the Calendar content type.

The following provides an overview of the base translation workflow. The admin for your company may configure additional translation modes, such as an integration with a third-party service to automate translation.

![Translate content workflow sends a request to the localization user to perform the translation](../images/ec-translation-workflow.png)

1.  The Content manager requests content translation from the Content Library or Block content interface and specifies the languages.
2.  The system creates a localization request item \(prefix LRITM\) for each language selected. Each localization request item has an associated localization task \(prefix LFTASK\), which is assigned to the user or group with the localization\_fulfiller role.

    The Content manager can view the status of the localization request item from the **Localization Framework** &gt; **My Requested Items** list.

3.  The user with the localization\_fulfiller role performs the translation. For more details, see [Fulfill a localization task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-framework/fulfill-localization-task.md).
4.  When the localization request item has a `Closed complete` state, the Content manager can schedule the content for publishing, see [Create a publish plan for your content](../task/ec-content-library-publish2.md). The system uses the same content schedule for the original and translated content.

## Changing the Content Library interface language

The Switch language window displays available languages, each appended by one of three possible statuses:

-   **Base language**

    The default language based on system settings.

-   **Translated**

    Indicates that translations are available for the content. This occurs when the content has been translated through the Localization Framework or manually translated in the New Content form fields.

    Selecting this option will translate both the interface and the values entered in the New Content form to the chosen language.

-   **Not translated**

    Translation for the field values is not available. In this case, only the interface language is translated, while the values entered in the form remain unchanged.


![Switching to French-translated option will change the interface text and the user-input values to French](../images/ec-switch-language.png)

**Note:** Remember to switch back to your original language before leaving the page, otherwise the ServiceNow interface will continue to appear in the translated language.

## Content versioning and translation

When content versioning is enabled, the **Switch Language** button appears only for the first draft version and published content.

Customers who create content in a non-English language should use of the the following workarounds:

-   Turn off Content versioning, then click the **Switch Language** button to enter the content in a non-English language.
-   Enter the content in English, then use the **Translate Content** button to initiate the translation workflow.

For more information, see [Content versioning](ec-content-versioning.md).

