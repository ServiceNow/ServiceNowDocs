---
title: Configure a data source
description: Start importing data with Integration Hub by creating a data source. A data source specifies how and where to get the data you want to import.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub - Import, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Configure a data source

Start importing data with Integration Hub by creating a data source. A data source specifies how and where to get the data you want to import.

## Before you begin

-   Imports in Integration Hub require the ServiceNow IntegrationHub Action Template - Data Stream \[com.glide.hub.action\_type.datastream\] plugin. For more information, see [Request IntegrationHub](../../flow-designer/concept/request-ih-overview.md).
-   A data source in Integration Hub uses an Excel file, a CSV file, or a Data Stream action. Data Stream actions have unique inputs, so if you plan to use one, make sure to familiarize yourself with it first. To learn more, see [Data Stream actions and pagination](../concept/data-stream-actions.md). You can use Data Stream actions with dynamic outputs, but dynamic inputs aren't supported.
-   Role required: admin or ih\_import.

## About this task

Configuring a data source is the first step to importing data in Integration Hub. After you set up the data source, you can select a target table, determine how data is transformed to the target table, and run and schedule the import.

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **IntegrationHub - Import**.

2.  Select **Create new integration**.

    The New Data Import Integration screen displays.

3.  Configure your data source.

    1.  Fill in the fields for the data integration.

        |Field|Description|
        |-----|-----------|
        |Name|Name of your integration.|
        |Short description|Description of your integration.|
        |Application|Name of the application scope for your integration.|

    2.  Select **Save &amp; Continue**.

    3.  Use the **Source type** menu to select a data source type.

        -   To choose an Excel or CSV file, select **AD-HOC** &gt; **** &gt; **File**, then either **Excel** or **CSV**. In the File upload section, upload an XLSX, XLS, CSV, or ZIP file.
        -   To choose a Data Stream action, select **Spokes**. Active Data Streams are organized by spoke and listed alphabetically. In the Connection section, select the connection alias. For Data Stream actions that use a connection alias, you can override the default connection alias with any of its children's aliases. For more information, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).
    4.  Configure the data source.

        -   To configure an Excel spreadsheet, specify which sheet to use and which row number to use for the header. Only one sheet and one header can be specified.
        -   To configure a CSV file, select the delimiter.
        -   To configure a data stream action, enter any required inputs. This section only appears if the Data Stream action has inputs to enter. Data Stream actions with inputs have unique inputs, so the fields in this section depend on which Data Stream action is selected and its configuration. Any default values already configured by the spoke inputs are pre-filled. You can view the details of the Data Stream action by clicking the information icon \(![Information icon](../images/info-icon.png)\) next to it. Clicking the icon opens the Data Stream action's configuration.
4.  Select **Save**.


## Result

The structure of the source data appears in the Source data structure preview pane. For an Excel or CSV file, the preview displays the column headers. For a Data Stream action, it displays the complex object output. If you edit the source configuration, click **Save** to reload the source data. The data must be previewed at least once before you can map it to a target table.

## What to do next

Map your source data to target tables. See [Map source data to a target table](map-source-data-target.md).

**Parent Topic:**[Integration Hub - Import](../concept/integrationhub-imports.md)

