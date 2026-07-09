---
title: Visualize Enterprise Architecture reports using CMDB Query Builder
description: Enterprise Architecture uses CMDB Query Builder to query on a list of configuration items used in Enterprise Architecture and visualize them as reports.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-portfolio-management/view-apm-reports-cmdb-query-builder.html
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Visualize Enterprise Architecture reports using CMDB Query Builder

Enterprise Architecture uses CMDB Query Builder to query on a list of configuration items used in Enterprise Architecture and visualize them as reports.

## Before you begin

Role required: sn\_apm.apm\_user

## About this task

Enterprise Architecture takes advantage of CMDB Query Builder to build complex queries and retrieve data from CMDB CI classes, Enterprise Architecture tables, and configuration items that are associated to each other by different CMDB CI relationships.

Before launching the reports that fetch data from the tables and CMDB CI classes, you must run the respective scheduled jobs. These jobs are set as active with frequency as **On Demand**. However, update the frequency as per your requirement to daily, weekly, monthly, periodically, once, on demand, Business Calendar – entry start, or entry end, based on how often the data for the report should be updated. Set the frequency of these scheduled jobs accordingly. For more information, see [Run scheduled jobs for CMDB Query Builder reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/scheduled-job-cmdb-query-builder.md).

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

        \[Omitted image "BusCapSuppByBusApp.png"\] Alt text: Business capabilities provided by business application report

    -   **Application Services consumed by Business Application**

        \[Omitted image "AppServForBusApp.png"\] Alt text: Application services consumed by business application report

    -   **Business Applications providing a Business Capability**

        \[Omitted image "BusAppProvBusCap.png"\] Alt text: Business applications providing a business capability report

    -   **Business Services provided by a Business Capability**

        \[Omitted image "BSProvedbyBC.png"\] Alt text: Business services provided by a business capability report

    -   **Business Applications using an Information Object**

        \[Omitted image "BusAppUsingInfObj.png"\] Alt text: Business applications using an information object report

    -   **Information Objects used by a Business Application**

        \[Omitted image "InfObjUsedByBusApp.png"\] Alt text: Information objects used by a business application report

    -   **Demands on a Business Application**

        \[Omitted image "DemandsOnBusApp.png"\] Alt text: Demands on a business application report

    -   **Projects on a Business Application**

        \[Omitted image "ProjectsOnBusApp.png"\] Alt text: Projects on a business application report


**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/using-apm.md)

**Related topics**  


[Run scheduled jobs for CMDB Query Builder reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-portfolio-management/scheduled-job-cmdb-query-builder.md)

