---
title: Portal FAQ widget instance options form
description: The instance options enable you to configure the Portal FAQ widget on a portal page.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configurable Portal widgets instance options, Customer Service Management reference, Customer Service Management]
---

# Portal FAQ widget instance options form

The instance options enable you to configure the Portal FAQ widget on a portal page.

<table id="table_csm_base_entities"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table from which the records shown as frequently asked questions \(FAQs\) on the widget are selected.By default, this field is set to the Knowledge \[kb\_knowledge\] table.

</td></tr><tr><td>

Question Field

</td><td>

The field of the table set in the **Table** field that contains the questions.Records with an empty question field aren't displayed on the widget.

</td></tr><tr><td>

Answer Field

</td><td>

The field of the table set in the **Table** field that contains the answer.Records with an empty answer field aren’t displayed on the widget.

</td></tr><tr><td>

Query

</td><td>

Query to filter FAQs.If this field is empty, the widget displays all the FAQs.

You can include fields from the provided table only in the encoded filter query. For more information, see [Generate an encoded query string through a filter](https://www.servicenow.com/docs/access?context=t_GenEncodQueryStringFilter&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

</td></tr><tr><td>

Sort by

</td><td>

Field in the Knowledge \[kb\_knowledge\] table that determines the field by which FAQs are sorted and displayed on the widget. By default, the field is set to View Count.

</td></tr><tr><td>

Sort Order

</td><td>

The order of the FAQs on the search result page on the widget.The available options are:

-   z to a
-   a to z

The default order is z to a.

**Note:** Currently, if you select None, the order is set to z to a.

</td></tr></tbody>
</table>|Instance option|Description|
|---------------|-----------|
|Title|Required title of a Portal FAQ widget. The default text is `Frequently Asked Questions`.|

<table id="table_hpn_kb1_fzb"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display search

</td><td>

Option to display a Search field on the widget.

</td></tr><tr><td>

Search Bar placeholder text

</td><td>

Placeholder text for the search field label. The default text is `Search FAQs`.

</td></tr><tr><td>

FAQ View Page

</td><td>

The article page that opens when the **Read more** option is selected by the user.By default, this field is set to the kb\_article\_view.

</td></tr><tr><td>

FAQ per page

</td><td>

The number of FAQs to appear by default on the widget.The default value is set to 5.

</td></tr><tr><td>

Browse Options

</td><td>

The filter options that appear in the widget and can be selected by the user. The available options are:

-   Knowledge Category
-   Related products

The default option is Knowledge Category.

**Note:** Currently, if you select None, the filter option is set to Knowledge Category.

</td></tr><tr><td>

Show Read More

</td><td>

Displays the entire content of an article when the related FAQ is accessed on the widget.The available options are:

-   Always: Display the **Show Read More** option on a widget for both complete and incomplete preview content
-   Exceeds preview: Display the **Show Read More** option only when the article content exceeds the preview limit on the widget

The default option is Exceed preview.

**Note:** Currently, if you select None, the filter option is set to Knowledge Category.

</td></tr></tbody>
</table>**Related topics**  


[Portal FAQ widget](../concept/portal-faq-widget.md)

[Add and configure the Portal FAQ widget](config-portal-faq-widget-inst-optns.md)

