---
title: Edit a glossary in Language Asset Management
description: Edit the contents of your glossary in Language Asset Management. Modify existing terms and translations, and add new ones.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Language Asset Management, Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Edit a glossary in Language Asset Management

Edit the contents of your glossary in Language Asset Management. Modify existing terms and translations, and add new ones.

## Before you begin

-   First, create a glossary using the provided spreadsheet template and upload it to Language Asset Management. For information see [Upload glossaries to Language Asset Management](lw-lam-upload-glossaries.md).
-   Role required: sn\_lw.user

## About this task

Initially you create a glossary in Language Asset Management by uploading a spreadsheet template. If you want to modify any source terms or their translations, or you want to add new items, use the following procedure to make your updates directly in the UI.

**Note:** The same source term may be repeated in a glossary if assigned to different Part of Speech or Product/Service categories. A source term repeated in two different categories is considered to be two different records. Any changes you make to a source term in one category aren't propagated to the same source term in other categories.

## Procedure

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Language Asset Management.**.

2.  On the Glossaries tab, select your glossary from the values in the **Glossary Name** column.

3.  From your glossary's default tab \(**Details**\), select the **Glossary Sources** tab to open a list of source terms.

    ![In Language Asset Management, the glossary "Key terminology used in HR" has been opened. It opens to the Details tab by default.](../image/lw-lam-edit-glossary-details-tab-a.png)

4.  To open information about a particular source term, select the value in the first column.

    **Note:** Because it's possible to have the same source term in different Part of Speech or Product/Service categories, be sure to select the desired source term.

    ![A glossary opened to the Glossary Sources tab. A value in the first column is highlighted. Also highlighted is the New button, the way to add a source term.](../image/lw-lam-edit-glossary-gloss-sources-a.png)

5.  On the source term's Details tab, modify any values \(such as Definition, Product/Service, Part of Speech, or Source Language\) then select Save.

6.  Select the **Glossary Translations** tab to open a list of all translations for your source term.

    The Glossary Translations tab includes the number of translations for that term.![A source term's Details tab, showing fields such as the Definition. The Glossary Translation tab is highlighted, the way to view this term's translations.](../image/lw-lam-edit-glossary-source-term-details-a.png)

7.  If you want to modify a translation, select the value in the Translation column to open the translation's tab.

    Select Save after you have finished.![A source term's list of translations on the Glossary Translations tab. A value in the Translation column is highlighted, and also the New button, for adding a translation.](../image/lw-lam-edit-glossary-open-translation-a.png)

8.  To add a new translation for your source term, select New on Glossary Translations.

    ![The form to add a new translation for a source term. Available fields are Language, Translation, and Glossary Source.](../image/lw-lam-edit-glossary-create-translation-a.png)

9.  To add a new source term, select New on the Details tab of the glossary.

<table id="table_o3v_rr1_l3c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Term

</td><td>

Enter the source term \(the original word or phrase\). Terms can contain spaces, special characters, and punctuation marks.Source terms can be written in languages other than English. However, translation requests in Localization Workspace must be from English to non-English languages.

You can enter the same source term multiple times, but each variation must be assigned to either a different Part of Speech or a different Product/Service category.

</td></tr><tr><td>

Definition

</td><td>

The definition for the source term.

</td></tr><tr><td>

Product/Service

</td><td>

This is a way to filter or subdivide a glossary. Use this when a source term has different translations depending on the Product/Service value. **Note:** The same source term can be listed multiple times in one glossary when associated to different Product/Service values. A source term repeated in two different Product/Service categories is considered to be two different records.

</td></tr><tr><td>

Part of Speech

</td><td>

This is a drop-down selection. Choose from noun, verb, and so forth.**Note:** The same source term can be listed multiple times in one glossary when associated to different Part of Speech values. A source term repeated in two different Part of Speech categories is considered to be two different records.

</td></tr><tr><td>

Source Language

</td><td>

This is a drop-down selection. Choose from among the languages installed on your instance.

</td></tr><tr><td>

Do Not Translate

</td><td>

This is a Boolean check box. The default is unchecked \(cleared\). Select this check box when the term shouldn't be translated.

</td></tr><tr><td>

Glossary Info

</td><td>

This is a drop-down selection. The current glossary is selected by default, or you can choose a different existing glossary. You can't create a new glossary while editing an existing glossary. To create a separate glossary, see [Upload glossaries to Language Asset Management](lw-lam-upload-glossaries.md).

</td></tr></tbody>
</table>
## What to do next

You can delete a source term and its translations by selecting Delete from More Options ![](../../../common/image/Form_MoreOptions.png) on the source term's Details tab.

You can also delete a translation from a source term using Delete from More Options![image.more-options-menu], when you are on the translation's Details tab.

**Parent Topic:**[Language Asset Management](../concept/lw-language-asset-management.md)

