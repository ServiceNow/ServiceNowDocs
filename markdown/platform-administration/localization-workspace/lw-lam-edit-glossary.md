---
title: Edit a glossary in Language Asset Management
description: Edit the contents of your glossary in Language Asset Management. Modify existing terms and translations or add more terms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-workspace/lw-lam-edit-glossary.html
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 4
breadcrumb: [Language Asset Management, Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Edit a glossary in Language Asset Management

Edit the contents of your glossary in Language Asset Management. Modify existing terms and translations or add more terms.

## Before you begin

-   First, create a glossary using the provided spreadsheet template and upload it to Language Asset Management. For information see [Upload glossaries to Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-lam-upload-glossaries.md).
-   Role required: sn\_lw.user. From version 3.1.0, both the sn\_lw.user and the sn\_lw.terminology\_manager roles are required.

## About this task

Initially you create a glossary in Language Asset Management by uploading a spreadsheet template. If you want to modify any source terms or their translations, or you want to add more items, use the following procedure to make your updates directly in the UI.

**Note:** The same source term may be repeated in a glossary if assigned to different Part of Speech or Product/Service categories. A source term repeated in two different categories is considered to be two different records. Any changes you make to a source term in one category aren't propagated to the same source term in other categories.

## Procedure

1.  Navigate to **All** &gt; **Localization Workspace** &gt; **Language Asset Management.**.

2.  On the Glossaries tab, select your glossary from the values in the **Glossary Name** column.

3.  From your glossary's default tab \(**Details**\), select the **Glossary Sources** tab to open a list of source terms.

    \[Omitted image "lw-lam-edit-glossary-details-tab-a.png"\] Alt text: In Language Asset Management, an example glossary titled "Key terminology used in HR" has been selected. Its Details tab opens by default, showing the glossary name and glossary description.

4.  To open information about a particular source term, select its value in the **Term** column.

    **Note:** Because it's possible to have the same source term in different Part of Speech or Product/Service categories, be sure to select the desired source term.

    \[Omitted image "lw-lam-edit-glossary-gloss-sources-a.png"\] Alt text: An example glossary opened to the Glossary Sources tab. The New button, for adding another source term to the current glossary, is highlighted.

5.  On the source term's Details tab, modify any values \(such as Definition, Product/Service, Part of Speech, or Source Language\) then select Save.

6.  Select the **Glossary Translations** tab to open a list of all translations for your source term.

    The Glossary Translations tab includes the number of translations for that term.\[Omitted image "lw-lam-edit-glossary-source-term-details-a.png"\] Alt text: A source term's Details tab, showing fields such as the Definition. The Glossary Translation tab for this source term is highlighted. That tab opens a list of the term's translations.

7.  If you want to modify a translation: on the Glosssary Translations list, select the value in the Translation column to open a tab for the individual translation.

    Select Save after you have finished.\[Omitted image "lw-lam-edit-glossary-open-translation-a.png"\] Alt text: A source term's list of translations on the Glossary Translations tab. The New button, for adding a translation, is highlighted.

8.  To add another translation for your source term, select New on the Glossary Translations list.

    \[Omitted image "lw-lam-edit-glossary-create-translation-a.png"\] Alt text: The form to add a translation for a source term. Available fields are Language and Translation.

9.  To add a source term to an existing glossary, select New on the Details tab of the glossary.

<table id="table_o3v_rr1_l3c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Term

</td><td>

Enter the source term \(the original word or phrase\). Terms can contain spaces, special characters, and punctuation marks.Source terms can be written in languages other than English. However, translation requests in Localization Workspace must be from English to non-English languages.

You can enter the same source term multiple times in a glossary, but each variation must be assigned to either a different Part of Speech or a different Product/Service category.

</td></tr><tr><td>

Definition

</td><td>

The definition for the source term.

</td></tr><tr><td>

Product/Service

</td><td>

You can filter or subdivide your glossary using this category. **Note:** The same source term can be listed multiple times in one glossary when associated to different Product/Service values. A source term repeated in two different Product/Service categories is considered to be two different records, with different translations possible.

</td></tr><tr><td>

Part of Speech

</td><td>

This is a drop-down selection. Choose from noun, verb, and so forth.**Note:** The same source term can be listed multiple times in one glossary when associated to different Part of Speech values. A source term repeated in two different Part of Speech categories is considered to be two different records, with different translations possible.

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

This read-only field confirms the name of the current glossary. **Note:** The same source term can be listed in more than one glossary. A source term repeated in two different glossaries is considered to be two different records, with different translations possible.

 To create a separate glossary, see [Upload glossaries to Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-lam-upload-glossaries.md).

</td></tr></tbody>
</table>
## What to do next

You can delete a source term and its translations by selecting Delete from More Options \[Omitted image "Form\_MoreOptions.png"\] on the source term's Details tab.

You can also delete a translation from a source term using Delete from More Options\[Omitted image "Form\_MoreOptions.png"\] on the translation's Details tab.

**Parent Topic:**[Language Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/localization-workspace/lw-language-asset-management.md)

