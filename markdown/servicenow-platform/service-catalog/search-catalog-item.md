---
title: Configure keyword search for catalog items
description: When you search for a catalog item by a keyword in Service Catalog, the search results are displayed by considering a few fields of the catalog table.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure search and navigation, Service catalog home page configuration, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure keyword search for catalog items

When you search for a catalog item by a keyword in Service Catalog, the search results are displayed by considering a few fields of the catalog table.

## Before you begin

Role required: admin

## About this task

If the keyword doesn’t have exact matches, its closest matches are displayed as **Did you mean** suggestions. This search functionality is also applicable in Service Portal.

The search results are sorted in the following order based on the frequency of the keyword:

-   Catalog items whose **Name** field contains the keyword \(top\).
-   Catalog items whose **Meta** field contains the keyword.

    **Note:** The **Meta** field is used for the Zing search, and if AI search is enabled, the field is used for the keyword search as well. If the **Meta** field is empty, the Zing search uses other sources, such as short descriptions and names.

-   Catalog items whose **Description** or **Short description** field contains the keyword.
-   Categories whose **Name** or **Description** field contains the keyword.
-   Catalogs whose **Name** or **Description** field contains the key term, or the catalog items whose **Class** field contains the keyword \(bottom\).

**Note:**

-   If your organization has multiple service catalogs, a search returns a result only from the catalog being viewed.
-   Search results return an item only when the item is active, has a valid catalog and category association, and you’re authorized to view the item.

## Procedure

1.  Complete the following steps to regenerate a text index for the sys\_metadata table.

    1.  Navigate to **System Definition** &gt; **Text Indexes**.

    2.  Open the text index for the Application File \[sys\_metadata\] table.

    3.  Select the **Regenerate Text Index** related link and select **OK**.

        The system schedules the table for the text indexing.

2.  Complete the following steps to enable the **Did you mean** suggestions.

    1.  Navigate to **System Properties** &gt; **Text Search**.

    2.  Under the **Did You Mean Properties** section, enable the **Suggest alternate search spellings for knowledge, catalog or global search** property.


**Parent Topic:**[Configure search and navigation](../concept/c_ConfigSrchNavUseProps.md)

**Related topics**  


[bundle-platadm.search-administration]

[Service Catalog for managers and end users](../concept/c_UsingTheServiceCatalog.md)

[bundle-platadm.t_RegenerateATextIndexForATable]

[bundle-platadm.t_ConfigureADidYouMeanSuggestion]

[Create or edit a catalog item](t_DefineACatalogItem.md#)

[Create a record producer](t_DefRecProdInSCat.md)

[Create an order guide](t_CreateAnOrderGuide.md)

[Define a content item](t_AddingContentItemServiceCatalog.md)

