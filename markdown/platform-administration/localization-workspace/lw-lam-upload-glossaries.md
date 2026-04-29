---
title: Upload glossaries to Language Asset Management
description: Upload glossaries to the Language Asset Management area of Localization Workspace. Create a glossary by entering source terms and translations in the provided spreadsheet template, then uploading the completed spreadsheet to Language Asset Management.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-03-13"
reading_time_minutes: 5
breadcrumb: [Language Asset Management, Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Upload glossaries to Language Asset Management

Upload glossaries to the Language Asset Management area of Localization Workspace. Create a glossary by entering source terms and translations in the provided spreadsheet template, then uploading the completed spreadsheet to Language Asset Management.

## Before you begin

-   Confirm that the Languages \[sys\_language\] table in your instance contains an ID for every language that you plan to include in your glossary. Language IDs should be compliant with BCP 47. For more information and links see [Language Asset Management](../concept/lw-language-asset-management.md).
-   You must be able to work with and save files in the Excel Workbook \(.xlsx\) file format. This file format supports the UTF-8 encoding that is needed for special characters and non-alphabetic writing systems.
-   Role required: sn\_lw.user

## About this task

From version 3.0.0, the Language Asset Management area of Localization Workspace enables you to upload glossaries for editing and storage.

-   Glossaries consist of source terms and their translations. Each source term can have translations into one or more languages.
-   After you initially create a glossary by uploading a spreadsheet, you can make updates or add new terms in the product UI. See [Edit a glossary in Language Asset Management](lw-lam-edit-glossary.md).

The following procedure involves downloading an Excel Workbook \(.xlsx\) spreadsheet template, filling it out, and uploading the completed file to your instance. Some of the columns have drop-down selections, as noted in the table in the procedure. For these columns, you must choose a value from the drop-down selection.

## Procedure

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Language Asset Management**.

2.  Select **Import Glossary**.

    ![In the Language Asset Management area, the Import Glossary button is highlighted.](../image/lw-lam-import-glossary-button-a.png)

    **Note:** If you have a completed spreadsheet ready to upload, skip to the next **Import glossary** step in this procedure.

3.  In the **Import existing glossary** modal window, select the **ServiceNow\_Glossary\_template.xlsx** attachment and download it.

    ![On the modal window titled Import existing glossary, the template download area is highlighted. The template filename is ServiceNow_Glossary_Template.xlsx](../image/lw-lam-upload-glossaries-dl-template-a.png)

4.  Using one row for a source term and its translations, and using drop-down selections where applicable, fill in the spreadsheet according to the following guidance.

<table id="choicetable_i4m_5rp_g3c"><thead><tr><th align="left" id="d308096e168">

Column

</th><th align="left" id="d308096e171">

Value

</th></tr></thead><tbody><tr><td id="d308096e177">

**glossary\_name**

</td><td>

This is displayed as **Glossary Name** in the UI. Each row should have a value in the glossary\_name column.

</td></tr><tr><td id="d308096e189">

**glossary\_description**

</td><td>

\(Optional\). Enter a description of the glossary. This value is displayed as **Glossary Description** in the UI.

</td></tr><tr><td id="d308096e201">

**product\_service**

</td><td>

This is displayed as **Product/Service** in the UI, and is a way to filter or subdivide a glossary. Use this if a source term has different translations depending on the Product/Service. **Note:** The same source term can be listed multiple times in one glossary when associated to different product\_service values.

</td></tr><tr><td id="d308096e215">

**term**

</td><td>

Enter the source term \(the original word or phrase\). Terms can contain spaces, special characters, and punctuation marks. Source terms can be written in languages other than English. However, translation requests in Localization Workspace must be from English to non-English languages.

You can enter the same source term multiple times, but each variation must be assigned to either a different Part of Speech or a different Product/Service category.

</td></tr><tr><td id="d308096e232">

**definition**

</td><td>

The definition for the source term.

</td></tr><tr><td id="d308096e241">

**part\_of\_speech**

</td><td>

This is a drop-down selection in the template. Choose from noun, verb, and so forth.**Note:** The same source term can be listed multiple times in one glossary when associated to different part\_of\_speech values.

</td></tr><tr><td id="d308096e252">

**do\_not\_translate**

</td><td>

This is a boolean drop-down selection in the template. Choose TRUE when terms shouldn't be translated.

</td></tr><tr><td id="d308096e261">

**source\_language**

</td><td>

This is a drop-down selection in the template. Choose the language ID of the source term.

</td></tr><tr><td id="d308096e270">

**\(language ID codes\)**

</td><td>

Enter the translations in the same row as the source term. The template contains columns for each language supported in the platform. The column headers are BCP 47 language ID codes.-   You can enter non-alphabetic terms and special characters.
-   You can leave values blank.
-   Clear the cell contents for any values you don't want applied to your glossary. This includes placeholder values such as "Translation1".
You can add you own columns for self-localized languages. If you create a column, use only language ID codes that exist in your sys\_language table as the column headers.

</td></tr></tbody>
</table>5.  Save your completed spreadsheet in the Excel Workbook \(.xlsx\) format only, not other formats such as Comma delimited \(.csv\) or Strict OpenXML Spreadsheet \(.xlsx\) format.

    ![Saving the completed spreadsheet. The file format Excel Workbook (.xlsx) is highlighted.](../image/lw-lam-upload-glossaries-fileformat-a.png)

    Because the value in the glossary\_name column is used to label and organize your glossary in Language Asset Management, the spreadsheet's filename is unimportant.

6.  In Language Asset Management, select **Import Glossary** to open the modal window Import existing glossary.

7.  On the modal window, select **Import Glossary** again.

8.  On the **Load Data** window: use the default settings \(Existing table = glossary\_import\_set and Source of the import = File\), and select **Choose File**.

    ![The Load Data window. The default settings are highlighted: Existing table with glossary_import_set, and Choose File.](../image/lw-lam-upload-glossaries-reupload.png)

9.  After choosing the completed spreadsheet file, select **Submit**.

10. When the **Progress** window displays Completion code: Success, select the **Run Transform** link.

    ![In the modal window, "Completion code: Success" is highlighted. Under Next Steps, the Run Transform link is also highlighted.](../image/lw-lam-upload-glossaries-run-transform-a.png)

11. At the **Specify Import set and Transform map** window, keep the default Import set and selected map \(GlossaryTransformMap\), then scroll down to select the **Transform** button.

    ![On the Specify Import set and Transform map window, the Transform button is highlighted. The defaults for Import set and map are selected.](../image/lw-lam-upload-glossaries-transform-a.png)

12. You can view the import set, Transform history, or Import log by selecting the appropriate link.

    ![The transform reports a State of Complete. Under Next steps, links for the import set, transform history, and Import log are available.](../image/lw-lam-upload-glossaries-final-a.png)

    Your new glossary appears in the list on the Glossaries tab of Language Asset Management.


## What to do next

To add or edit source terms, or make any modifications after the initial upload, see [Edit a glossary in Language Asset Management](lw-lam-edit-glossary.md).

**Parent Topic:**[Language Asset Management](../concept/lw-language-asset-management.md)

