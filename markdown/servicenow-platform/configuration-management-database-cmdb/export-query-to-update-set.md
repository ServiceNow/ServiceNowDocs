---
title: Export and import a query as an update set
description: Export a saved query definition to an XML file as an update set, which you can later import.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Export and import a CMDB query, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Export and import a query as an update set

Export a saved query definition to an XML file as an update set, which you can later import.

## Before you begin

Role required: To export — cmdb\_query\_builder. To import — user with permission to import an update set.

Domain in the exported query must be visible in both, source and destination instances.

## About this task

Export a query definition as an update set which you can later import and commit. This process lets you port a query between instances, such as from a development environment to a production environment. For more information about exporting and then committing update sets using XML files, see [Save an update set as a local XML file](https://www.servicenow.com/docs/access?context=t_SaveAnUpdateSetAsAnXMLFile&version=australia&pubname=australia-application-development&ft:locale=en-US).

When exporting a combination query, the integrated Service Mapping query definition is included in the exported update set.

## Procedure

1.  Export a saved query:

    1.  In the **Filter navigator**, enter `qb_saved_query.list`.

    2.  Select **Enter** to navigate to the Saved Queries table.

    3.  In the Saved Queries list view, select the query that you want to export.

    4.  Select **Actions on selected rows** and then **Export query**.

    5.  Wait for the **Query Exporter** to complete the export.

2.  Import the exported saved query:

    1.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

    2.  On the Retrieved Update Sets form, select **Import Update Sets from XML**.

    3.  On the Import XML page, select **Choose file**.

    4.  Select the exported XML file.

    5.  Select **Upload**.

    6.  Open the new record that was added to the Retrieved Update Sets list view.

    7.  On the Retrieved Update Set form, select **Preview Update Set Batch**.

    8.  Close the Batch Update Set Preview dialog box.

    9.  Select **Commit Update Set Batch**.

    10. Close the Commit Update Set Batch dialog box.


## Result

The imported query is added to the Query Builder saved queries on the instance.

