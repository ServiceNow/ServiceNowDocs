---
title: Enable dynamic translation for a field
description: Translate the dynamically generated text for a field on Platform forms by enabling the field-level dynamic translation. You can translate the text based on the preferred language of a user​.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Dynamic translation on forms and activity streams, Translating with Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Enable dynamic translation for a field

Translate the dynamically generated text for a field on Platform forms by enabling the field-level dynamic translation. You can translate the text based on the preferred language of a user​.

## Before you begin

Role required: admin

Activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\).

## About this task

Dynamic Translation supports only the following field types:

-   String
-   String \(Full UTF-8\)
-   Multi Line Small Text Area
-   Wide Text
-   HTML

**Note:**

-   The following are the length limitations for translation service providers:

    -   For Google, the recommended maximum length of each request is 5,000 characters. The maximum size of the input text cannot exceed 30,000 code points. For more information, see the [Google Documentation](https://cloud.google.com/translate/quotas).
    -   For Microsoft, the input text for translation cannot have more than 50,000 characters including spaces. The input text for detection also has a maximum of limit of 50,000 characters. For more information, see the [Microsoft Documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/request-limits#character-and-array-limits-per-request).
-   You cannot translate a field on Agent Workspace forms.

## Procedure

1.  Navigate to any form, for example, an Incident form.

2.  Right-click the required field and select **Configure Dictionary**.

3.  In the Attributes related list, click **New**.

4.  In the Dictionary Attribute form, fill the fields.

    |Field|Value|
    |-----|-----|
    |Attribute|Dynamic Translation Enabled|
    |Value|true|

5.  Click **Submit**.

6.  Click **Update**.

    ![Image for dynamic translation for a field](../image/Dynamic-translation-orlando.gif "Dynamic translation for a field")

    A translate icon ![translate icon](../image/Translation.png) appears next to the field. The logged-in user can click this icon ![translate icon](../image/Translation.png) to translate the text to the user's preferred language using the default translation service provider specified in the translator configurations. For information about error messages during translation, see [Error messages in Dynamic Translation](../reference/error-messages-field-translation.md).

    **Note:** If you do not have any default translator configuration, you cannot view the translate icon ![translate icon](../image/Translation.png).


