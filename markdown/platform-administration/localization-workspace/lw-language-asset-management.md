---
title: Language Asset Management
description: Enhance localization in your instance with Language Asset Management in Localization Workspace. You can upload glossaries to Language Asset Management for editing and storage.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Language Asset Management

Enhance localization in your instance with Language Asset Management in Localization Workspace. You can upload glossaries to Language Asset Management for editing and storage.

## Glossaries in Language Asset Management

From version 3.0.0, the Language Asset Management area of Localization Workspace enables you to upload glossaries, which are lists of terms with translations that you provide. Each source term in a glossary can have translations into multiple languages. You can create multiple glossaries. In the Australia release, glossaries are available for storage and editing only.

When planning your glossary assets, consider the following points.

-   You can have more than one glossary in Language Asset Management, so you can organize your glossaries according to business unit, function, or locale.
-   Each glossary can be subdivided or filtered using the Product/Service category.
-   One source term can be listed under different Product/Service or Part of Speech categories. A source term repeated in two different categories is considered to be two different records, so different translations can be assigned to each occurrence of the term per category. This enables a term to be translated differently depending on the context.
-   Translations assigned to source terms can be provided for any language listed in the sys\_language table, including self-localized languages.
-   The included spreadsheet template \(ServiceNow\_Glossary\_Template.xlsx\) must be used when creating a glossary. For details see [Upload glossaries to Language Asset Management](../task/lw-lam-upload-glossaries.md).
-   Any editing or modification to the contents of existing glossaries can be done in the UI. For details see [Edit a glossary in Language Asset Management](../task/lw-lam-edit-glossary.md).
-   There is no upper limit to the number of rows in a glossary, but the general guideline is for each glossary to have between 50 and 1500 rows.

In the spreadsheet template, columns are provided for all languages supported by ServiceNow AI Platform in the sys\_language table. You don't need to provide translations for all languages. Clear out \(leave blank\) all values for any languages you don't plan to use. You can upload glossary translations for languages that are active = false in sys\_language, but inactive languages are not available for translation workflows.

You can include self-localized languages when uploading glossaries with the spreadsheet template. Create additional columns in the spreadsheet template for self-localized languages. For the label in the header row of the spreadsheet, use codes from the ID column of the sys\_language table for the corresponding languages.

**Note:** With the following supported languages, the import transform handles mapping of the spreadsheet's language code to the ID code in sys\_language. Do not modify or update the header row of the spreadsheet template for these languages.

-   Brazilian Portuguese
-   French - Canada
-   Traditional Chinese

To activate languages in sys\_language, [install language plugins](../../localization/task/t_ActivateALanguage.md). To self-localize an unsupported language, see [Create a language record](../../localization/task/t_CreateANewLanguageRecord.md).

-   **[Upload glossaries to Language Asset Management](../task/lw-lam-upload-glossaries.md)**  
Upload glossaries to the Language Asset Management area of Localization Workspace. Create a glossary by entering source terms and translations in the provided spreadsheet template, then uploading the completed spreadsheet to Language Asset Management.
-   **[Edit a glossary in Language Asset Management](../task/lw-lam-edit-glossary.md)**  
Edit the contents of your glossary in Language Asset Management. Modify existing terms and translations, and add new ones.

**Parent Topic:**[Configuring Localization Workspace](configuring-localization-workspace.md)

