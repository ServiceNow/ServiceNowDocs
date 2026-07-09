---
title: Preview read table entities in Zero Copy Connector for ERP
description: Preview read table entities in Zero Copy Connector for ERP to examine and verify the entity before adding it to a model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/erp-canvas-preview-entity.html
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, entity, preview, see, model]
breadcrumb: [Add an entity to a model, Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Preview read table entities in Zero Copy Connector for ERP

Preview read table entities in Zero Copy Connector for ERP to examine and verify the entity before adding it to a model.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP model page by selecting the models icon \[Omitted image "image.erpc-data-model-icon"\] in the side panel.

3.  Select the model to which you want to add a read table entity.

4.  Select **Manage model**.

    If you have a read operation already, skip to step 8.

5.  Select **Add model operation**.

6.  In **Select type**, select **Read**.

7.  Select **Save and continue**.

8.  Select the **Read** operation tile.

9.  Select **Select entity**.

10. In **Select type**, select **Read table**.

11. Select **Preview table data**.

    \[Omitted image "image.erpc-preview-entity-preview-button"\] Alt text: Manage model page with preview table data button highlighted.

12. In **Search**, start entering any part of a table name and make a selection from the list.

13. In **Recently viewed tables**, select **Get data** on the table tile to obtain real-time data.

    \[Omitted image "image.erpc-preview-entity-get-data"\] Alt text: Preview table data page with a tile highlighted to show get data option.

    After the data is retrieved and available to view, the icon on the table tile turns green.

    \[Omitted image "image.erpc-preview-entity-got-data"\] Alt text: Preview table data page with a tile highlighted to show that the icon is now green.

14. Select the tile.

15. Explore the information available for the table.

    Ten rows of randomly selected records are displayed. Use the **Query** option to search for a specific record.

    \[Omitted image "image.erpc-preview-entity-records-list"\] Alt text: List of records in tables with a query highlighted.

    **Note:** If no records are found when querying, an error message is displayed. Select the **View details** link to open a new browser tab containing information about the error.

    \[Omitted image "image.erpc-preview-entity-error-msg"\] Alt text: Unable to display table data error message with view details link.

    To return to the unfiltered list, select the tile in **Recently viewed tables**.

    \[Omitted image "image.erpc-preview-entity-records-list-tiles"\] Alt text: Preview table data page with a tile highlighted in the recently viewed tables section.

    The **Selected fields** section contains the columns that are displayed in the records list.

    \[Omitted image "image.erpc-preview-entity-fields-list"\] Alt text: List of fields associated with the specified table.

    All fields associated with the table are listed and are categorized based on data type, such as date or time. Edit the **Selected fields** section by selecting a pill to remove it from the list or expanding a category and selecting a pill to add it to the list.

    \[Omitted image "image.erpc-preview-entity-edit-fields-list"\] Alt text: Field list with data type-C section expanded and ABDIS field selected.

    **Note:** Add no more than 7-8 fields to the **Selected fields** list so information is displayed clearly in the records list.

    To find a specific field, use the search. Keywords you enter are used to search the description, table type, and the table name.

    \[Omitted image "image.erpc-preview-entity-fields-search"\] Alt text: Field list with search option highlighted.

16. Continue to search for tables or select table tiles in **Recently viewed tables** and explore the table contents.


## What to do next

After viewing tables, select **Manage entities**, then **Select entity**. In **Select type**, select **Read** and in **Select entity** specify the table for the read operation to use.

\[Omitted image "image.erpc-preview-entity-manage-entities"\] Alt text: Manage model page with manage entities option highlighted.

For detailed information about adding entities, see [Add an entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/add-an-entity-to-model.md).

**Parent Topic:**[Add an entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/add-an-entity-to-model.md)

