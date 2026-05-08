---
title: Integration Hub - Import
description: Automate data import tasks through a consolidated interface that provides a guided, step-by-step experience. Define external data sources, specify target tables, map how source data becomes target data, and schedule regular imports.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Integration Hub - Import

Automate data import tasks through a consolidated interface that provides a guided, step-by-step experience. Define external data sources, specify target tables, map how source data becomes target data, and schedule regular imports.

Managing imports through Integration Hub simplifies the process of importing data from external sources and transforming it to ServiceNow tables. You can configure, run, and schedule your data imports all through a single interface.

You can access Integration Hub - Import directly through App Engine Studio to build data integrations for your custom applications. For more information, see Adding data in App Engine Studio.

## Benefits

Managing your imports through Integration Hub provides these benefits.

-   Consolidates multiple data integration capabilities into a single environment, eliminating the need to create and manage several forms throughout the platform.
-   Enables you to manage multiple integrations through a single interface.
-   Guides you through the configuration of data sources and target tables.
-   Enables you to map and transform data from a single simplified interface.
-   Enables you to schedule data imports or manually import data on demand.
-   Provides usage information about data imports run and details about imported rows, updates, and errors.

## Overview of the import process

There are three steps to importing data.

-   **1. Configure a data source.**

    The data source specifies how and where to get the data to import. In Integration Hub, the data source uses an Excel file, a CSV file, or a Data Stream action to get data from an external source. A Data Stream action sends a REST, SOAP, or JDBC request to an API and returns a stream of data.

-   **2. Map the data to the target tables.**

    The target tables are the tables that you want to transform the data to. After you've selected the target tables, you can specify how the source data should be transformed to them. Creating a data map outlines how to transform the data, the data isn't transformed until you run the import.

-   **3. Run or schedule the import.**

    After you've configured the data source and determined the data mapping, you can run the import. You can also schedule the import to run later. When the import runs, data is gathered from the source, moved to a staging table, and transformed to the target tables according to the specifications in your mapping.


For more details about how importing data works, see [Import sets](../../import-sets/reference/import-sets-landing-page.md).

## Integration Hub import environment

The Integration Hub import environment includes the following interfaces.

-   Landing page
-   Source configuration
-   Map to target
-   Schedule imports
-   Execution details

The following sections explain each interface in greater detail.

## Landing page

Create and access integrations through the landing page.

![User interface for the IntegrationHub import landing page.](../images/ih-import-landing.png "Landing page user interface")

The landing page has these components.

-   **1. List of integrations**

    Integrations created through the Integration Hub import interface are accessible here.

-   **2. Create new integration button**

    Button to start building a new integration.


## Source configuration

Define a data source for an import through the source configuration page. The data source must be an Excel file, a CSV file, or a Data Stream action.

![User interface for the IntegrationHub import source configuration section.](../images/ih-import-source.png "Source configuration section user interface")

The source configuration section has these components.

-   **1. Source type selector**

    Menu to select the data source type. It has the following sections.

    -   AD-HOC: Select an Excel or CSV file as a data source.
    -   SPOKES: Select a Data Stream action as a data source. Displays active Data Streams organized by spoke and listed alphabetically.
-   **2. File upload or Connection section \(the Connection section isn't shown\)**

    If the data source is an Excel or CSV file, the File upload section appears here. You can drag a file over or browse to upload. Accepts XLSX, XLS, CSV, and ZIP files.

    If the data source is a Data Stream action, the Connection section appears here. For Data Stream actions that use a connection alias, you can override the default connection alias with any of its children's aliases. Select the connection alias from the menu. For more information, see Create a Connection and Credential alias.

-   **3. Configuration section**

    Section to configure the selected data source. The available fields depend on the type of data source that you're using.

    -   For an Excel file, you can select the sheet and specify which row number to use for the header.
    -   For a CSV file, select the delimiter.
    -   For a Data Stream action, enter the inputs for it here. This section only appears if the Data Stream action has inputs. Data Stream actions with inputs have unique inputs, so the fields that appear here depend on which Data Stream action is selected and its configuration. Any default values already configured by the spoke inputs are pre-filled.
-   **4. Source data structure preview**

    Section that shows the structure of the source data. For an Excel or CSV file, the preview displays the column headers. For a Data Stream action, it displays the complex object output.

-   **5. Properties button**

    Button to view the name of the integration, its description, and the application scope. You can edit the name and description at any time. The application scope can't be edited and must be selected when the integration is created.

-   **6. Save button**

    Button to save the source configuration. This button is only enabled when the source configuration is updated. When you select a source type, the structure of the source data is automatically loaded in the Source data structure preview pane. If you edit the source configuration, click **Save** to reload the source data. The data must be previewed at least once before you can map it to a target table.


## Map to target

Select the target tables and determine how the source data is mapped to them. Map data by dragging data pills from the source to the target, using the pill picker, or selecting **Automap**. Transform the data in the target tables by applying transform functions.

The Map to target section has two parts. In the first part, select the target tables. In the second part, map the data to the target tables.

![User interface for the IntegrationHub table selection section.](../images/ih-import-target.png "Table selection user interface")

The table selection section has these components.

-   **1. Add a table**

    Button to add target tables.

-   **2. Transform Settings**

    Button to configure the transform settings for your integration. You can specify batch size and empty-field handling, enable verbose mode, or run a script before or after the integration. For more information, see [Transform settings](../reference/transform-settings.md).

    The **Transform Settings** button doesn't appear until you've added at least one target table.

-   **3. Target table cards**

    Each card has the name of the target table, its creation details, and whether it's been mapped. Select the card to open the data-mapping interface.

-   **4. Target table drop-down list**

    List of options for the target table. Includes the following.

    -   **Properties**: Opens the Mapping Properties window where you can view or edit the options to run the table's business rules when importing and to run the import synchronously.
    -   **Edit mapping**: Opens the data-mapping section where you can create or edit your data mapping.
    -   **Table Configuration**: Opens Table Builder where you can configure the target table. This option is only available if you have Table Builder installed. For more information, see Table Builder.
    -   **Revalidate**: Checks to see if there are any changes to the target entity schema. If changes are detected, the target table card displays a message saying the target schema has changed. Selecting the target table card opens a window where you can **Update** the target entity schema or **Cancel** to keep the schema the same. Revalidate your table whenever you edit the target table's configuration.
    -   **Delete**: Deletes the target table from the integration.

![User interface for the IntegrationHub import data mapping section.](../images/ih-import-map.png "Data-mapping user interface")

The data-mapping section has these components.

-   **1. Target table name**

    Name of the target table you're currently mapping to.

-   **2. Source data section**

    Section that displays the source data as data pills. To map the data, drag the data pills to the target table data section. You can also use the pill picker. After you map a source field to a target field, a small check mark icon \(![check mark icon](../images/check-mark-icon.png)\) appears next to the source field name. If you move your cursor to the check mark, the tooltip lists the target fields that source field has been mapped to, up to five fields.

-   **3. Target table data section**

    Section that displays how the source data maps to each field in the selected target table. You can display all the fields in the target table, or select individual fields with the **Add a field** button. For choice and reference fields, you can specify which column to map data to or you can use the default display column.

-   **4. Match toggle switch**

    Toggle switch to specify fields where the system should check for matching data and, if found, update existing records instead of creating new ones. In this image, the **Match** toggle switch is turned on for the **user id** field. If a record in the source data has a user id that matches the user id for a record in the target table, the system will update the existing record in the target table instead of creating a new one.

-   **5. Mapping properties button**

    Button to view or edit the options to run the table's business rules when importing and to run the import synchronously.

-   **6. Automap button**

    Button to automatically map source entities to similarly named target entities.

-   **7. Data pill picker**

    Button to open the data pill picker. You can use the pill picker to map source data pills to field values in the target table.

-   **8. Transform function icon**

    Button to open the list of available transform functions. Use transform functions to change or modify your data. For example, the Trim transform function removes white space from the beginning and end of an input string.


## Schedule imports

Run an import immediately, or schedule it to run at a specific time, at regular intervals, or after a parent import. Schedule large imports to run concurrently to reduce processing time.

![User interface for the IntegrationHub import schedule imports section.](../images/ih-import-schedule.png "Schedule imports section user interface")

The schedule imports section has these components.

-   **1. Scheduled imports**

    List of import schedules. Each import schedule appears in its own button.

-   **2. Schedule an import button**

    Button to create an import schedule.

-   **3. Executions section**

    Section with information about executed imports. Includes links to execution records, execution context records, and scheduled import records. This section only appears after an import is run.

-   **4. Execution records**

    List of execution records. Each execution record provides information about an execution, including the imported rows, errors, and log messages.

-   **5. Execution context records**

    List of execution context records. Each execution context record specifies the next scheduled import to use when processing a hierarchical scheduled import.

-   **6. Scheduled import records**

    List of scheduled import records. Each record provides the name, data source, schedule, and partition method for the scheduled import.

-   **7. Run Import button**

    Button to run the import once.


## Execution details

View details for each import, such as the execution time and date, and execution context. Open the import's execution records to view the import state and the imported rows, errors, and logs.

![User interface for the IntegrationHub import execution details section.](../images/ih-import-execution.png "Execution details section user interface")

The execution details section has these components.

-   **1. Execution information**

    Section providing details about the execution, including the number of the execution record, the name of the scheduled import, the import set number, and the date it was updated.

-   **2. Execution Details**

    Section with cards showing the total number of rows imported, processed, pending, or skipped, and the number of errors that occurred. If the import is processed concurrently, this section also includes a Partitions card. For more information, see [Concurrent imports](../../import-sets/concept/concurrent-imports.md).

    You can click the cards to filter the results. Filtered results display in the Import Set Rows tab toward the bottom of the page. For example, clicking the **Pending** card displays the pending rows. Clicking **Total rows imported** or **Clear Selection** clears the filters.

    **Note:** Card filtering is only available for import set rows. To see the filtered list, make sure you're on the Import Set Rows tab.

-   **3. Partitions card**

    Graphical view of the import set partitions. The partitions card only appears for concurrent import sets. You can click a partition to view its details. You can also use the Execution Details cards for additional filtering. When you combine the partition filter with the card filters, the system uses an AND operation for filtering. For example, if you click a partition, then click the Errors card, the Import Set Rows tab displays only the errors for that partition.

-   **4. Partitions list view**

    Option to view the details for each partition, including the import set number, and the type and state for each import set job. The partitions list view only appears for concurrent import sets. The partitions list view provides the same filtering capabilities as the Partitions card, so you can use either to filter a partition.

-   **5. Import details**

    Section detailing the import set rows, outbound HTTP requests, action execution history, import logs, and errors for each execution record.


## Integration Hub import terms

Imports in Integration Hub have these components.

-   **Data source**

    A data source is a configuration record that defines the type of data to import and the endpoint where your instance can get it.

-   **Data Stream action**

    A Data Stream action is an action that sends REST, SOAP, or JDBC requests from Workflow Studio to APIs and returns a stream of response data. Use Data Stream actions to retrieve data larger than 10 MB, or when working with APIs that return paginated results.

-   **Target table**

    A target table is the table that you want your source data to be transformed to.

-   **Transform function**

    A transform function is a function that changes or modifies your data. For example, a function that transforms an input string to all uppercase characters.

-   **Execution**

    An execution is a run-time record that contains the execution details for a single import. Each execution provides import details for a specific target, including rows imported, log messages, and errors.

-   **Execution context**

    An execution context is a record that specifies the next scheduled import to use when processing a hierarchical scheduled import.

-   **Import set**

    An import set is a set of run-time records that contain the raw data imported from a data source. The system stores imported records in an Import Set staging table.


## Design considerations

Follow these guidelines to achieve the benefits offered by Integration Hub imports.

-   **Create all Integration Hub imports from within Integration Hub**

    Only integrations created in the Integration Hub import environment are accessible there. For example, you can't configure a data source and mapping through platform forms, but then schedule the import from within Integration Hub. Only integrations created in Integration Hub appear on the landing page.

-   **Don't alter configuration records outside of Integration Hub**

    Altering configuration records directly might change if and how data is imported and mapped. If you need to change the configuration of the data source, mapping, or import schedule, do so from within the Integration Hub import interface.

-   **Avoid modifying Data Stream actions used in data sources**

    Modifying Data Stream actions used as data sources might change the mapping from source to target. When the output for a Data Stream action changes, the Map to target page displays a warning that the complex object schema has changed. You might need to reconfigure the mapping.


-   **[Configure a data source](../tasks/configure-data-source.md)**  
Start importing data with Integration Hub by creating a data source. A data source specifies how and where to get the data you want to import.
-   **[Map source data to a target table](../tasks/map-source-data-target.md)**  
Specify how source data is transformed to your target tables.
-   **[Run or schedule a data import](../tasks/run-schedule-data-imports.md)**  
Specify when to run a data import by creating a schedule. Schedule an import to run at a specific time, at regular intervals, or after a parent import. You can also run your import immediately.
-   **[Transform settings](../reference/transform-settings.md)**  
Configure the transform settings for your Integration Hub - Import integration. Specify batch size and empty-field handling, enable verbose mode, or run a script before or after the integration.

**Parent Topic:**[Importing and streaming data in Integration Hub](importing-streaming-data-ih.md)

