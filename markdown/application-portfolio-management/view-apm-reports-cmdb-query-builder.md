---
title: Visualize Enterprise Architecture reports using CMDB Query Builder - Legacy
description: Enterprise Architecture uses CMDB Query Builder to query on a list of configuration items used in Enterprise Architecture and visualize them as reports.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Visualize Enterprise Architecture reports using CMDB Query Builder - Legacy

Enterprise Architecture uses CMDB Query Builder to query on a list of configuration items used in Enterprise Architecture and visualize them as reports.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

Enterprise Architecture takes advantage of CMDB Query Builder to build complex queries and retrieve data from CMDB CI classes, Enterprise Architecture tables, and configuration items that are associated to each other by different CMDB CI relationships.

Before launching the reports that fetch data from the tables and CMDB CI classes, you must run the respective scheduled jobs. These jobs are set as active with frequency as **On Demand**. However, update the frequency as per your requirement to daily, weekly, monthly, periodically, once, on demand, Business Calendar – entry start, or entry end, based on how often the data for the report should be updated. Set the frequency of these scheduled jobs accordingly. For more information, see [Run scheduled jobs for CMDB Query Builder reports](scheduled-job-cmdb-query-builder.md).

**Note:** Ensure to run these scheduled jobs from **Global** scope only. Only a system administrator can run these scheduled jobs from global scope. However, as an Enterprise Architecture user you can view the reports.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **CMDB Query Builder**.

    All reports that the base system offers are provided as menu options in the application navigator under CMDB Query Builder.

2.  Click the relevant CMDB query builder name for which you want to view the report.

    The report opens in a new tab and is rendered as a bar chart, by default. You can view and save the report for future use.

    **Note:** The data displayed on the report is retrieved from the latest execution of the scheduled job run on demand.

3.  Click each option to view the respective report.

    **Note:** You must activate the PPM Standard plugin to generate Projects on a Business Application CMDB query builder report.

    Enterprise Architecture base system provides the following list of queries to generate Enterprise Architecture reports:

    -   **Business Capabilities provided by Business Application**
    -   **Application Services consumed by Business Application**
    -   **Business Applications providing a Business Capability**
    -   **Business Services provided by a Business Capability**
    -   **Business Applications using an Information Object**
    -   **Information Objects used by a Business Application**
    -   **Demands on a Business Application**
    -   **Projects on a Business Application**

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\) - Legacy](../concept/using-apm.md)

**Related topics**  


[Run scheduled jobs for CMDB Query Builder reports - Legacy](scheduled-job-cmdb-query-builder.md)

