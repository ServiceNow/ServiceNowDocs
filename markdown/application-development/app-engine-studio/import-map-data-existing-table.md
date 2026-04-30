---
title: Create a data integration
description: Add new or updated information to your current data sets by importing it into existing tables in your application through the power of Integration Hub. Schedule future imports to add data at specific times.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Create a data model for your application, Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Create a data integration

Add new or updated information to your current data sets by importing it into existing tables in your application through the power of Integration Hub. Schedule future imports to add data at specific times.

This video shows you how to perform the following procedure.

This video shows you how to create a data integration. 

## Before you begin

-   You must have an existing table in your application. For more information, see [Create a blank table](use-existing-table.md).

    **Note:** Currently, Excel files are the only accepted data format users can upload.

-   Role required: admin, sn\_app\_eng\_studio.user, or delegated\_developer. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## Procedure

1.  Navigate to **All** &gt; **App Engine** &gt; **App Engine Studio**.

2.  From the My Apps page, open your application.

3.  Next to the Data heading, select the Add icon \(![Add icon](../image/plus-icon.png)\).

4.  Select **Create a data integration**.

5.  Configure your data import source
6.  Configure your data import source by performing the following steps.

    1.  Fill in the fields for the data integration.

        |Field|Description|
        |-----|-----------|
        |Name|Name of your integration.|
        |Short description|Description of your integration.|
        |Application|Name of the application scope for your integration.|

    2.  Select **Save &amp; Continue**.

    3.  Use the **Source type** menu to select a data source type.

        -   To choose an Excel or CSV file, select **AD-HOC** &gt; **** &gt; **File**, then either **Excel** or **CSV**. In the File upload section, upload an XLSX, XLS, CSV, or ZIP file.
        -   To choose a Data Stream action, select **Spokes**. Active Data Streams are organized by spoke and listed alphabetically. In the Connection section, select the connection alias. For Data Stream actions that use a connection alias, you can override the default connection alias with any of its children's aliases. For more information, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).
    4.  Configure the data source.

        -   To configure an Excel spreadsheet, specify which sheet to use and which row number to use for the header. Only one sheet and one header can be specified.
        -   To configure a CSV file, select the delimiter.
        -   To configure a data stream action, enter any required inputs. This section only appears if the Data Stream action has inputs to enter. Data Stream actions with inputs have unique inputs, so the fields in this section depend on which Data Stream action is selected and its configuration. Any default values already configured by the spoke inputs are pre-filled. You can view the details of the Data Stream action by clicking the information icon \(![Information icon](../../../administer/integrationhub/images/info-icon.png)\) next to it. Clicking the icon opens the Data Stream action's configuration.
7.  Select the **Save** button.

8.  Choose your target table and configure import options
9.  Select the **Map to target** tab.

10. Select the target table and options for the data integration you're creating.

    Mapping the source data to the target table allows you to control how the system treats the data you uploaded.

    1.  On the Source to target table data mapping page, select **Add a table**.

    2.  In the Mapping Properties window, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Target table|Name of the table to transform your data to.|
        |Run table's business rules when importing|Option to run the target table's business rules when you import the data.|
        |Run the import synchronously|Option to run the import synchronously. When data is transformed in parallel, and there are multiple source records with a specific coalesce value, checking this option ensures that only one record with that coalesce value is inserted at a time. For more information, see the Synchronized inserts section on the [Concurrent imports](https://www.servicenow.com/docs/access?context=concurrent-imports&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) page.|

    3.  Select **Save**.

        You can add multiple target tables to your integration. Repeat steps 4a through 4c for each target table you want to add.

        Tables are listed in the order they're added. You can change the order by using the drag icon ![drag icon](../image/drag-icon.png)to the left of each table card to drag the card to a different position. The order of the table cards determines the order in which data is transformed into the target tables at runtime.

        **Note:** You can't select the same table more than once, and you can't select an extended table or parent table of a table already in the integration.

11. Map import fields to your target table
12. Map the fields in your import to the target table by performing the following actions.

    ![Map data to the target table](../image/map-target.png "Mapping data to the target table")

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

        You can also map data by using the pill picker \(![Pill picker icon](../../../administer/integrationhub/images/pill-picker-green.png)\) on the right side of the target table. You can enter more than one value in the Value column, you can also enter text.

        After you map a source field to a target field, a small check mark icon \(![check mark icon](../../../administer/form-builder/image/check-mark-icon.png)\) appears next to the source field name. If you move your cursor to the check mark, the tooltip lists the target fields that source field has been mapped to, up to five fields.

    4.  Use the **Match** toggle switch to specify fields where the system should check for matching data and, if found, update existing records instead of creating new ones.

        For example, if a target table has an **Order number** field and a record with an order number of 743, there are two options for handling potential matches.

        -   If the **Match** toggle switch for the **Order number** field is on, the system checks for matching data. If the source data has a record with the same order number, the system updates the existing record in the target table.
        -   If the **Match** toggle switch for the **Order number** field is off, the system doesn't check for matching data. If the source data has a record with the same order number, the system creates a new record in the target table. In this case, the target table will have two records, both with an order number of 743.
    5.  For choice and reference fields, specify the column to map data to.

        1.  Select the gear icon \(![Gear icon](../image/gear-icon.png)\).
        2.  In **Field**, select the column to map to.
        3.  In **If no matching record exists then do the following**, specify what to do if that column isn't available.
            -   **Create a new choice/record**: Creates the choice or record in the target table.
            -   **Ignore this field**: Ignores only the field in the target table.
            -   **Skip this record**: Skips the entire record in the target table.
        4.  Select **Done**.
    6.  Change or modify your data by applying transform functions.

        For example, you can use the Uppercase transform function to change an input string to all uppercase characters. For more information, see [Transform functions](https://www.servicenow.com/docs/access?context=transform-functions&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

        **Note:** Not all the transform functions available while creating flows and subflows are available in Integration Hub - Import.

        1.  Select the transform function icon \(![Transform function icon](../../../administer/integrationhub/images/transform-function-icon.png)\).
        2.  Select a transform function from the menu, then select **OK**.
        3.  To apply additional transform functions, select **Add a new transform**. Transform functions are applied in the order they're selected.
        4.  After you've added all your transform functions, select **Done**.
13. When you're done with your mapping, click **Save**.

14. Import the file or schedule the data import
15. Choose what to do with your data import you just created and mapped.

    -   To import the data set you uploaded now, select **Run Import**.
    -   To set up a future import of the data, select **Schedule an import**.
    See [Run or schedule a data import](https://www.servicenow.com/docs/access?context=run-schedule-data-imports&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

16. If you ran the import, preview the table and ensure it appears with the additional content by returning to the target table, refreshing your browser screen, and clicking **Preview**.

17. If you added new columns during the import and want them to display on the target table, select **Personalize list** to edit the columns that display.


**Parent Topic:**[Create a data model for your application](../concept/add-data.md)

