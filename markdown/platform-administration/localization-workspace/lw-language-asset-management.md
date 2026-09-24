---
title: Language Asset Management
description: Enhance localization in your instance with Language Asset Management in Localization Workspace. You can upload glossaries to Language Asset Management for editing and storage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-workspace/lw-language-asset-management.html
release: brazil
product: Localization Workspace
classification: localization-workspace
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Language Asset Management

Enhance localization in your instance with Language Asset Management in Localization Workspace. You can upload glossaries to Language Asset Management for editing and storage.

## Glossaries in Language Asset Management

From version 3.0.0, the Language Asset Management area of Localization Workspace enables you to upload glossaries, which are lists of terms with translations that you provide. Each source term in a glossary can have translations into multiple languages. You can create multiple glossaries. In the Australia release, glossaries are available for storage and editing only.

From version 4.0, you can use an AI skill to generate a glossary of terms derived from Knowledge Base articles. For information see [Globalization Terminology Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-terminology-agent.md).

When planning your glossary assets, consider the following points.

-   You can have more than one glossary in Language Asset Management, so you can organize your glossaries according to business unit, function, or locale.
-   Each glossary can be subdivided or filtered using the Product/Service category.
-   One source term can be listed under different Product/Service or Part of Speech categories. A source term repeated in two different categories is considered to be two different records. Different translations can be assigned to each occurrence of the term per category. This enables a term to be translated differently depending on the context.
-   Translations assigned to source terms can be provided for any language listed in the sys\_language table, including self-localized languages.
-   The included spreadsheet template \(ServiceNow\_Glossary\_Template.xlsx\) must be used with the upload method for creating glossaries. For details see [Upload glossaries to Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-lam-upload-glossaries.md).
-   Any editing or modification to the contents of existing glossaries can be done in the UI. For details see [Edit a glossary in Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-lam-edit-glossary.md).
-   You can download your glossaries from version 3.1.0. For more information, see [Export a glossary from Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-lam-export-glossary.md).
-   There is no upper limit to the number of rows in a glossary, but the general guideline is for each glossary to have between 50 and 1500 rows.

In the spreadsheet template for the upload method, columns are provided for all languages supported by ServiceNow AI Platform in the sys\_language table. You don't need to provide translations for all languages. Clear out \(leave blank\) all values for any languages you don't plan to use. You can upload glossary translations for languages that are active = false in sys\_language, but inactive languages are not available for translation workflows.

You can include self-localized languages when uploading glossaries with the spreadsheet template. Create additional columns in the spreadsheet template for self-localized languages. For the label in the header row of the spreadsheet, use codes from the ID column of the sys\_language table for the corresponding languages.

**Note:** With the following supported languages, the import transform handles mapping of the spreadsheet's language code to the ID code in sys\_language. Do not modify or update the header row of the spreadsheet template for these languages.

-   Brazilian Portuguese
-   French - Canada
-   Traditional Chinese

To activate languages in sys\_language, [install language plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/system-localization/t_ActivateALanguage.md). To self-localize an unsupported language, see [Create a language record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/system-localization/t_CreateANewLanguageRecord.md).

-   **[Globalization Terminology Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-terminology-agent.md)**  
Generate a glossary of terms based on your English-language Knowledge Base articles. Use the glossary of terms to enhance language governance, quality, and consistency across the platform. Available from version 4.0 of Localization Workspace.
-   **[Upload glossaries to Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-lam-upload-glossaries.md)**  
Upload glossaries to the Language Asset Management area of Localization Workspace. Create a glossary by entering source terms and translations in the provided spreadsheet template, then uploading the completed spreadsheet to Language Asset Management.
-   **[Edit a glossary in Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-lam-edit-glossary.md)**  
Edit the contents of your glossary in Language Asset Management. Modify existing terms and translations or add more.
-   **[Export a glossary from Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/lw-lam-export-glossary.md)**  
Download your glossary as a CSV or spreadsheet file to share with stakeholders, reviewers, or third-party translation service providers.

**Parent Topic:**[Configuring Localization Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-workspace/configuring-localization-workspace.md)

