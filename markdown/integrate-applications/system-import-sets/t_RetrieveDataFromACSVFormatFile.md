---
title: Retrieving data from a CSV formatted file
description: In this method, you import data from another instance using an HTTPS data source to return a CSV formatted file containing the rows to be imported.
locale: en-US
release: zurich
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Importing from another ServiceNow instance, Import sets, Imports, Workflow Data Fabric]
---

# Retrieving data from a CSV formatted file

In this method, you import data from another instance using an HTTPS data source to return a CSV formatted file containing the rows to be imported.

## Before you begin

Role required: Admin.

## About this task

This approach uses the Import Sets application to retrieve the data from the source and import it to the destination.

![](../image/HTTPSDataSource.png "HTTPS Data Sources")

## Procedure

1.  Create a new data source by navigating to **Import Sets** &gt; **Data Sources** on the destination instance.

2.  Provide the following field values:

    -   **Import set table name**: Select a table.
    -   **Type**:File
    -   **Format**:CSV
    -   **File retrieval method**:HTTPS

        **Note:**

        If the **Server**, **File path**, **Username**, and **Password** fields are not visible when you select **HTTPS**, change the file retrieval method temporarily to **SCP** and enter this information. Remember to reset the **File retrieval method** to **HTTPS** after you enter these fields.

    -   **File path**:incident.do?CSV

        **Note:** To import specific change records, you can add qualifiers to the path. For example, the following path would return all active change records: `incident.do ?CSV &amp ;sysparm_query =active = true "`

    -   **User name** and **Password:** Enter the user name and password for a valid user on the destination instance.
3.  Click the **Test load 20 records** related link to verify that the import is configured correctly.

4.  After setting up the data source, configure a standard transform map.


**Parent Topic:**[Importing from another ServiceNow instance](../concept/c_ImportingFromAnotherSNInstance.md)

