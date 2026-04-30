---
title: Export and import a CMDB query
description: Export a saved CMDB or Service Mapping query definition to an XML file which you can later import and run in the CMDB Query Builder. This process lets you port a saved query between instances, such as from a development environment to a production environment.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Export and import a CMDB query

Export a saved CMDB or Service Mapping query definition to an XML file which you can later import and run in the CMDB Query Builder. This process lets you port a saved query between instances, such as from a development environment to a production environment.

## Before you begin

-   You must save a query before you can export it.
-   Domain in an exported query must be visible in both, source and destination instances.

Role required: cmdb\_query\_builder \(contained in itil, itil\_admin, and asset\).

## About this task

When exporting a combination query, the integrated Service Mapping query definition is included in the exported query.

For backward compatibility, you can alternatively [Export and import a query as an update set](export-query-to-update-set.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Query Builder**.

2.  Export a saved query:

    1.  In the **Saved Queries** tab, in either list view or card view, select a saved query.

    2.  Select the **Export query** icon at the top of the Query Builder canvas.

    3.  Wait for the **Query Export Complete** message to appear and then select **Download**.

        You can now access the query XML file.

3.  Import a saved query:

    1.  In the **Saved Queries** tab, select the **Import query** icon at the top of the CMDB Query Builder window.

    2.  In Finder, select the saved query XML file and select **Open**.

        The imported query is available in the **Saved Queries** tab of the CMDB Query Builder on the instance.


