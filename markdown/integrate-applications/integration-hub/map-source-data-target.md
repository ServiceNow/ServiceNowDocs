---
title: Map source data to a target table
description: Specify how source data is transformed to your target tables.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub - Import, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Map source data to a target table

Specify how source data is transformed to your target tables.

## Before you begin

[Configure a data source](configure-data-source.md).

Role required: admin or ih\_import.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **IntegrationHub - Import**.

2.  On the landing page, select your integration.

3.  On the left navigation panel, select **Map to target**.

4.  Add your target tables.

    1.  On the Source to target table data mapping page, select **Add a table**.

    2.  In the Mapping Properties window, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Target table|Name of the table to transform your data to.|
        |Run table's business rules when importing|Option to run the target table's business rules when you import the data.|
        |Run the import synchronously|Option to run the import synchronously. When data is transformed in parallel, and there are multiple source records with a specific coalesce value, checking this option ensures that only one record with that coalesce value is inserted at a time. For more information, see the Synchronized inserts section on the [Concurrent imports](../../import-sets/concept/concurrent-imports.md) page.|

    3.  Select **Save**.

        You can add multiple target tables to your integration. Repeat steps 4a through 4c for each target table you want to add.

        Tables are listed in the order they're added. You can change the order by using the drag icon ![drag icon](../images/drag-icon.png)to the left of each table card to drag the card to a different position. The order of the table cards determines the order in which data is transformed into the target tables at runtime.

        **Note:** You can't select the same table more than once, and you can't select an extended table or parent table of a table already in the integration.

5.  Map the fields from your source data to a target table.

    1.  On the Source to target table data mapping page, select the button with the target table you want to map to.

        This opens the data-mapping section for the table. The left side of the page shows the source data. The right side is for the target table.

    2.  Use the **Add a field**, **Add all fields**, or **Automap** button to configure the target side and begin mapping data.

        -   To add all the fields in the target table, select **Add all fields**. Fields are added alphabetically.
        -   To add fields individually, select **Add a field** and choose the field name from the list. A field can only be added once.
        -   To add fields and map them automatically, select **Automap**. Automap maps source entities to similarly named target entities. The **Automap** button has two options.
            -   **All matching fields in the target table** adds all the fields and maps the ones that match.
            -   **All unmapped fields in the target selection** maps only the fields that you've already added but haven't mapped yet. If you haven't added any fields yet, this option is not available.
        -   For a target entity that has already been mapped, selecting **Automap** doesn't change its value. An automapped field has a wand icon on its data pill.

            By default, Automap maps a maximum of one source entity to a target entity. You can change this by setting the **glide.ih.automap.extractone** property to false.

            Automap matches source to target entities by looking for column names that are at least an 80% match. You can modify this with the **glide.ih.automap.minimum.score** property. For example, to make matches based on a 60% similarity, you can set **glide.ih.automap.minimum.score** to 60.

    3.  Map data by dragging data pills from the source to the **Value** column on the target table.

        You can also map data by using the pill picker \(![Pill picker icon](../images/pill-picker-green.png)\) on the right side of the target table. You can enter more than one value in the Value column, you can also enter text.

        After you map a source field to a target field, a small check mark icon \(![check mark icon](../images/check-mark-icon.png)\) appears next to the source field name. If you move your cursor to the check mark, the tooltip lists the target fields that source field has been mapped to, up to five fields.

    4.  Use the **Match** toggle switch to specify fields where the system should check for matching data and, if found, update existing records instead of creating new ones.

        For example, if a target table has an **Order number** field and a record with an order number of 743, there are two options for handling potential matches.

        -   If the **Match** toggle switch for the **Order number** field is on, the system checks for matching data. If the source data has a record with the same order number, the system updates the existing record in the target table.
        -   If the **Match** toggle switch for the **Order number** field is off, the system doesn't check for matching data. If the source data has a record with the same order number, the system creates a new record in the target table. In this case, the target table will have two records, both with an order number of 743.
    5.  For choice and reference fields, specify the column to map data to.

        1.  Select the gear icon \(![Gear icon](../../../build/app-engine-studio/image/gear-icon.png)\).
        2.  In **Field**, select the column to map to.
        3.  In **If no matching record exists then do the following**, specify what to do if that column isn't available.
            -   **Create a new choice/record**: Creates the choice or record in the target table.
            -   **Ignore this field**: Ignores only the field in the target table.
            -   **Skip this record**: Skips the entire record in the target table.
        4.  Select **Done**.
    6.  Change or modify your data by applying transform functions.

        For example, you can use the Uppercase transform function to change an input string to all uppercase characters. For more information, see Transform functions.

        **Note:** Not all the transform functions available while creating flows and subflows are available in Integration Hub - Import.

        1.  Select the transform function icon \(![Transform function icon](../images/transform-function-icon.png)\).
        2.  Select a transform function from the menu, then select **OK**.
        3.  To apply additional transform functions, select **Add a new transform**. Transform functions are applied in the order they're selected.
        4.  After you've added all your transform functions, select **Done**.
6.  When you're done with your mapping, select **Save**.

    If you're mapping to more than one target table, repeat steps 5 and 6 for each table.


## What to do next

[Run or schedule a data import](run-schedule-data-imports.md).

**Parent Topic:**[Integration Hub - Import](../concept/integrationhub-imports.md)

