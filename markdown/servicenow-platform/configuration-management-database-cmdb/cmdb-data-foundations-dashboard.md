---
title: CMDB Data Foundations dashboard
description: Use the CMDB Data Foundations dashboard to monitor foundational key health-related metrics in CMDB.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 19
breadcrumb: [CSDM and CMDB Data Foundations Dashboards, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB Data Foundations dashboard

Use the CMDB Data Foundations dashboard to monitor foundational key health-related metrics in CMDB.

## Requirements

-   To access the CMDB Data Foundations dashboard, users must be configured with the sn\_cmdb\_admin, admin, itil\_admin, or asset roles. Some metrics that let you drill-down to Performance Analytics \(PA\) data, might require additional roles for accessing specific tables. Those roles are specified as appropriate per metric.
-   The CMDB Data Foundations dashboard adds the following scheduled jobs, which must be running:
    -   **CMDB Get Well Metric Collection**: Calculates and stores details for compliant CIs associated with metrics, populating the list view of the metrics. Data appears on the dashboard only after the first run of this scheduled job. Metrics' scores are stored in the CMDB Data Foundations Metric Scores \[sn\_getwell\_cmdb\_score\] table. This non-PA job runs daily by default.
    -   **CMDB Data Foundations PA Metric Collection**: Calculates the total non-compliant CIs associated with metrics and populates the PA widgets on the dashboard. Also, provides trending data over time for the non-compliant CIs associated with metrics. This PA job runs daily by default.
    -   **CMDB Get Well CIs Processed Via IRE Metric Batch Collection**: Invoked once a day \(by default\) by the **CMDB Get Well Metric Collection** job and repeatedly runs in 10 minute intervals, to process as many 1,000-CIs \(default\) batch files as possible. After each 10-minute run, the job stops for a minute.

## Overview of CMDB Data Foundations dashboard

![CMDB Data Foundations dashboard with compliant and non-compliant CIs.](../image/CMDB-DataFoundations-Xanadu.png)

The CMDB Data Foundations dashboard provides four tabs, each grouping a distinctive set of CMDB metrics:

-   **Best Practices**: Checks if usage of tables and properties is as intended for supporting the health of the CMDB. This set of metrics checks adherence of CSDM-related standards, for example, for populating services and relationships.
-   **Customizations**: Checks how customizations to the CMDB are used. This set of metrics checks that customizations are not used excessively, and that they are used only when needed and are correctly applied.
-   Data Management Practices: Checks if importing third-party data into the CMDB is properly done without compromising the integrity of the CMDB. This set of metrics checks if the imported data is properly configured and formatted to provide the foundation for CMDB functions.
-   **ITSM Processes**: Check if ITSM processes leverage CMDB data.

## Columns in the list view of metrics

The following columns appear in the list view of metrics:

-   **Name**

    Name of metric.

-   **Priority**

    Priority of an metric. The priority for an metric is a calculation of the weight of the metric and the severity of the percentage score. Priority ranges from **1- Critical** as the highest priority, to the lowest priority which is **5 - Low**. Metrics are listed in their priority order, starting with the highest priority metric \(lowest priority number\).

-   **Result**

    Percentage number of CIs \(or the measured item\) which are in compliance with the metric.

    **Note:** Some metrics use a lower threshold value which impacts the result that appears in the dashboard. For these metrics, if the percentage of compliant CIs is less than the lower threshold value, then the result appears as 0 for the metric.

-   **Remediation playbook URL**

    Links to remediation playbook articles in Now Support. These knowledge articles provide context for the respective issue, guidelines to help remediate the issue, and other necessary details to bring CIs into compliance. Click the link and use your Now Support credentials to access the knowledge article.


## Performance Analytics widgets

Most metrics are associated with [Performance Analytics \(PA\) widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/performance-analytics/c_Widgets.md) \(tiles\) that provide further details about CIs that are not in compliance with the metric. Drill down the tiles to access PA widgets, which are provided by the **CMDB Data Foundations PA Metric Collection** scheduled job.

On the Analytics Hub page:

-   Click the **Breakdowns** context menu to see any available breakdowns.
-   Ensure that the **Real-time** \(![Real-time](../image/RealTimeFoundationsDashboard.png)\) option is selected and then click **Show Records** to see a list view of the respective CIs.

## Best Practices metrics

The **Best Practices** tab contains the following metrics:

-   **Create Asset Business Rule is Enabled**

    Checks for the existence of the **Create Asset on insert** business rule. If the business rule exists, the percentage score for the metric is 100. Otherwise, the percentage score is set to 0.

-   **Custom CMDB Attributes at the Right Level**

    Percentage of custom attributes that should be added at a higher level in the CMDB hierarchy. For example, the custom attribute **Warranty duration** was added three times in the Computer class, instead of adding the attribute once at a higher level in the hierarchy, which is more efficient.

    -   If \(total number of attributes that can be moved up &gt; 10\): Percentage is set to 0.
    -   Otherwise: Percentage is set to \(10 – total number of attributes that can be moved up\)\*10.
-   **Hardware CIs with Serial Numbers**

    Percentage of Computer or Network Gear CIs with a serial number versus those CIs without. The metric is based on the following conditions:

    -   Class is an instance of Computer or Gear
    -   Status = installed
    -   Operational status = operational
    -   Serial number is empty
    The complete set of CIs for this metric consists of the CIs that satisfy the first three conditions. The CIs that satisfy all conditions are counted as non-compliant Computer or Network Gear CIs, which are without a serial number.

    **Note:** If the percentage of compliant CIs is less than 70%, then the percentage score for this metric is set to 0.

    The Hardware CIs Missing Serial Numbers tile shows the total number of CIs which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those CIs.

    The Hardware CIs Missing Serial Number by Key Classes chart shows those CIs that are missing a Serial Number, grouped by key classes. Point to a class bar on the chart to show more details, and select a class bar to access a list view of those CIs for class.

    To manage a potential performance impact, other than deactivating the metric, you can limit the performance impact by adjusting the following performance management columns for the metric in the CMDB/CSDM Get Well Metrics \[sn\_getwell\_metric\] table. For this metric, those columns are set with the following default values:

    -   **Aggregate limit**: 30 \(% of CIs in the metric\)
    -   **Fail count threshold**: 3
    -   **Runtime threshold**: 3,600
    For more information about these columns, see Performance management in [Monitor health in CSDM and CMDB Data Foundations Dashboards](csdm-cmdb-foundations-dashboards.md).

-   **Services with Owners**

    Percentage of operational services in which the **owned\_by** field is populated versus those operational services in which this field isn't populated.

    The complete set of CIs for this metric consists of all the operational services in the Service \[cmdb\_ci\_service\] table \(where **operational\_status** = **Operational**\). The percentage score for this metric is calculated as \(Compliant CIs/Complete set of CIs\) \*100.

    The Services Missing Owners tile shows the total number of CIs which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those CIs.


## Customizations metrics

The **Customizations** tab contains the following metrics:

-   **Base System Business Application Table Usage**

    Checks for the existence of a custom business application table, which is any table that extends \[cmdb\_ci\], whose name starts with “u\_” or “x\_” and which contains the strings “bus” and “app”.

    If such custom table exists, then is 0, and if not, the percentage is 100.

    The Custom Business Application Tables tile shows any custom business application tables. Click the tile to drill down the PA widget for further details, such as the list all those tables.

-   **Base System CMDB Relationship Types Usage**

    Percentage of base system relationship types versus custom relationship types that were created by users. Creating custom relationship types can interfere with the integrity of the CMDB therefore this metric can help you prevent such problems.

    This metric counts records in the Relationship Type \[cmdb\_rel\_type\] table where **sys\_package** is “global” and **name** is not “Manages::Managed by”. The percentage score for this metric is calculated as follows:

    -   If count is &lt;= 0, then percentage is 100
    -   If count is &gt; 10, then percentage is 0
    -   Otherwise percentage = \(10 – count\)\*10
    The Custom CMDB Relationship Types tile shows the relationships which are not in compliance with the metric. Those are the relationships that were not included in the base system and were custom created. Click the tile to drill down the PA widget for further details, such as the list all those relationships.

-   **Base System Relationship Types Not Deleted or Recreated**

    Percentage of relationship types that exist in the base system and which were not deleted or recreated, versus those that were deleted and maybe recreated. Deleting and recreating base system relationships can interfere with the integrity of the CMDB, therefore this metric can help you prevent potential problems.

    This metric counts the number of base system relationships that were deleted and possibly recreated. The percentage score for the metric is calculated as follows:

    -   If count is &lt;= 0 then the percentage is set to 100
    -   If count is &gt; 10 then the percentage is set to 0
    -   Otherwise, the percentage = \(10 – count\)\*10
    .

    The Base System CMDB Relationship Types Deleted and/or Recreated tile shows the relationships which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those relationships.

-   **Custom CMDB Tables Using Standard Naming**

    Percentage of custom CMDB tables whose name doesn't start with the standard string “u\_cmdb\_ci”. The metric counts tables in the Tables \[sys\_db\_object\] table that extend from the CMDB table and whose name starts with the string “u\_” \(indicating that it is a custom table\) but not with “u\_cmdb\_ci”.

    The percentage score for this metric is calculated as follows:

    -   If count &lt;= 0 then percent is 100
    -   If count &gt; 6 then percent is 0
    -   If count is between 0 and 6, then percent is \(1-\(count/6\)\)\*100
    The Custom CMDB Tables Not Using Standard Naming tile shows the tables which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those tables.

-   **Use of Custom Attributes**

    Percent of custom attributes that were added to CMDB tables in the base system. Custom attributes are identified by a table name that starts with "cmdb\_ci" and a column name that starts with “u\_.”

    The percentage score for the metric is calculated as follows:

    -   If \(total custom attribute count &gt; 50\): Percentage is set to 0.
    -   If \(total custom attribute count &lt; 10\): Percentage is set to 100.
    -   If \(total custom attribute count is 10–50\): Percentage is set to \(total custom attribute count – 10\)/\(50-10\)\*100.

## Data Management Practices metrics

The **Data Management Practices** tab contains the following metrics:

-   **Active CIs Updated in Last 90 days**

    Percentage of Hardware \[cmdb\_ci\_hardware\] or Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] active CIs that were updated in the past 90 days versus those CIs that were not \(stale CIs\). The metric is based on the following conditions:

    -   Class is an instance of Hardware or VMware Virtual Machine Instance
    -   Status = installed
    -   Operational status = operational
    -   Updated &gt;= 90 days
    The complete set of CIs for this metric consists of CIs that satisfy the first three conditions. The CIs that satisfy all conditions, are counted as stale CIs of the Hardware \[cmdb\_ci\_hardware\] and Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] classes.

    **Note:** If the percentage of compliant CIs is less than 65%, then the result displayed for this metric is set to 0.

    The Active CIs Not Updated in 90 Days tile shows the total number of CIs which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those CIs.

-   **CIs Processed via IRE**

    Percentage of Hardware \[cmdb\_ci\_hardware\] or Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] CIs processed via IRE versus those CIs not processed via IRE. CIs are counted as processed via IRE if they satisfy all of the following conditions:

    -   Instance of Hardware \[cmdb\_ci\_hardware\] or Virtual Machine Instance \[cmdb\_ci\_vm\_instance\]
    -   Status = installed
    -   Operational status = operational
    -   Sys\_id is IN \(target\_sys\_id FROM sys\_object\_source table\)
    The CIs that satisfy only the first three conditions but fail the forth condition, are counted as CIs not processed via IRE.

    **Note:** Viewing the data provided by PA for this metric, requires the additional role of sn\_cmdb\_admin, admin, or discovery\_admin. However, the **Show Records** button on the Analytics Hub page isn't supported.

    To manage a potential performance impact, other than deactivating the metric, you can limit the performance impact by adjusting the following performance management columns for the metric in the CMDB/CSDM Get Well Metrics \[sn\_getwell\_metric\] table. For this metric, those columns are set with the following default values:

    -   **Fail count threshold**: 3
    -   **Runtime threshold**: 72,000 \(Daily limit of total runtime of all **CMDB Get Well CIs Processed Via IRE Metric Batch Collection** job runs\)
    For this metric, there is no trigger for automatically setting the metric score to 0. For more information about these columns, see 'Performance management' in [Monitor health in CSDM and CMDB Data Foundations Dashboards](csdm-cmdb-foundations-dashboards.md).

-   **CIs with Names**

    Percentage of Hardware, VMware Virtual Machine Instance, or Application CIs with a name up to 200. The metric is based on the following conditions:

    -   Class is an instance of Hardware \[cmdb\_ci\_hardware\], Virtual Machine Instance \[cmdb\_ci\_vm\_instance\], or Application \[cmdb\_ci\_appl\]
    -   Status = installed
    -   Operational status = operational
    -   Name is empty
    Non-compliant CIs are counted as the CIs that are missing a name, which are those CIs that satisfy all conditions.

    The percentage score for the metric is calculated as follows:

    -   If count of CIs without names is &gt; 200, percent is 0
    -   If count of CIs without names is &lt; 200, percent is \(200-\(count of CIs without names\)/200 \* 100\)
    The CIs Missing Names tile shows the total number of CIs which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those CIs.

-   **CIs with Relationships to Parent and Child**

    Percentage of non-orphan CIs versus orphan CIs.

    The complete set of CIs for this metric consists of CIs in records from the CI Relationship \[cmdb\_rel\_ci\] table. CIs in which \[parent.sys\_class\_name=\(empty\)\] OR \[child.sys\_class\_name=\(empty\)\], are counted as orphan CIs.

    The Orphan CIs tile shows the total number of orphan CIs, correlating the darker portion of the metric bar. Select the tile to drill down to the list all those CIs.

    To manage a potential performance impact, other than deactivating the metric, you can limit the performance impact by adjusting the following performance management columns for the metric in the CMDB/CSDM Get Well Metrics \[sn\_getwell\_metric\] table. For this metric, those columns are set with the following default values:

    -   **Aggregate limit**: 1,000
    -   **Fail count threshold**: 3
    -   **Runtime threshold**: 3,600
    For more information about these columns, see Performance management in [Monitor health in CSDM and CMDB Data Foundations Dashboards](csdm-cmdb-foundations-dashboards.md).

-   **Handled Duplicate CIs**

    Percentage of duplicate CIs of the Hardware or VMware Virtual Machine Instance classes, that were remediated, up to 200. If the number of unhandled duplicate CIs is greater than the upper threshold of 200, then is set to 0. The metric is based on the following conditions:

    -   Class is an instance of the Hardware \[cmdb\_ci\_hardware\] or the Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] class.
    -   Status = installed
    -   Operational status = operational
    -   Duplicate\_of in not empty
    Non-compliant CIs are counted as those CIs that satisfy all conditions. Non-compliant CIs are those Hardware \[cmdb\_ci\_hardware\] or Virtual Machine Instance \[cmdb\_ci\_vm\_instance\] duplicate CIs that were not remediated. For more information, see [Duplicate CIs remediation](de-duplication-tasks.md).

    The percentage score for this metric is calculated as follows:

    -   If count of non-compliant CIs is &gt; 200 then percent is 0
    -   If count of non-compliant CIs is &lt; 200 then percent is \(200-count of non-compliant CIs\)/200\*100
    The Unhandled Duplicate CIs tile shows the total number of CIs which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those CIs.

-   **Installed Server CI Naming Reflecting Hostname**

    Percent of Server CIs where name reflects the host name, up to the first period in the name. The complete set of CIs for the metric are all the servers in the Server \[cmdb\_ci\_server\] table in which **install\_status**=1 and **host\_name** is not empty.

    Examples of compliant CIs:

    -   Server Name is “abc”, and host name is “abc.1.2.3”
    -   Server Name and host name are the same
    The percentage score for the metric is calculated as \(Compliant CIs/Total CIs\)\*100.

    The Installed Server CI Naming Not Reflecting Hostname tile shows the number of Server CIs which are not in compliance with the metric. Click the tile to drill down the PA widget for further details, such as the list all those CIs.

    **Note:** If you need to manually refresh the Installed Server CI Naming Not Reflecting Hostname widget, then you must first run the CMDB Get Well Metric Collection job, and then run the CMDB Data Foundations PA Metric Collection job.

-   **Managed CIs with Model Entries**

    Percentage of Hardware \[cmdb\_ci\_hardware\] CIs with a model ID versus those CIs without.

    The complete set of CIs for this metric consists of all the CIs in the Hardware \[cmdb\_ci\_hardware\] table. Compliant CIs are those in which **model\_id** is populated.

    The Managed CIs Missing Model Entries tile shows the total number of CIs which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those CIs.

-   **Servers with Location**

    Percentage of Server CIs in which **Location** is populated versus Server CIs in which **Location** isn't populated. The complete set of CIs for this metric are the Server CIs in the Server \[cmdb\_ci\_server\] table in which install\_status =1 and operational\_status=1. Compliant CIs are those CIs in which also location is not null.

    The percentage score for the metric is calculated as \(Compliant CIs/Total CIs\)\*100.

    The Servers Missing Location tile shows the number of Server CIs which are not in compliance with the metric. Those are the Server CIs in which **Location** is empty. Click the tile to drill down the PA widget for further details, such as the list all those CIs.

-   **Unique Locations**

    Percentage of unique locations versus non-unique \(duplicate\) locations.

    The complete set of locations for this metric consists of all the locations in the Location \[cmn\_location\] table records, in which **name** is not null. A duplicate location is counted as a record in which **name** is not null, and the same name is used more than once.

    The percentage score for the metric is calculated as \(Compliant CIs/Total CIs\)\*100.

    The Duplicate Locations tile shows the total number of CIs which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those CIs.

    **Note:** If you need to manually refresh the Installed Server CI Naming Not Reflecting Hostname widget, then you must first run the CMDB Get Well Metric Collection job, and then run the CMDB Data Foundations PA Metric Collection job.


## ITSM Processes metrics

The **ITSM Processes** tab contains the following metrics:

-   **Changes Referencing a CI**

    Percentage of change requests with a reference to CIs versus those change requests without. The complete set includes all change requests created in the last 90 days. Compliant records are those change requests in which the **cmdb\_ci** field is not empty.

    The percentage score for the metric is calculated as \(Compliant change requests/Total change requests\) \* 100.

    The Changes Not Referencing a CI tile shows the total number of records which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those change requests.

    **Note:** Viewing all the data provided by Performance Analytics for this metric \(when drilling down\), requires the additional role of sn\_cmdb\_editor,itil, or sn\_change\_read.

-   **Changes Relating to both a Service and a CI**

    Percentage of changes relating services to CIs versus those changes that don't. The complete set of CIs for this metric consists of all change request records. Compliant records are those change requests in which both, the **cmdb\_ci** and the **business\_service** fields, are not empty.

    The Incidents Relating to Neither a Service nor a CI tile shows the total number of records which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those CIs.

    **Note:** Viewing all the data provided by Performance Analytics for this metric \(when drilling down\), requires the additional role of sn\_cmdb\_editor,itil, or sn\_change\_read. Click the tile to drill down the PA widget for further details, such as the list all those CIs.

-   **Incidents Referencing a CI**

    Percentage of incidents referencing a CI versus those incidents that don't. The complete set of records includes all incidents created in the last 60 days. Compliant incidents are all those in which the **cmdb\_ci** field is not empty.

    The percentage score for the metric is calculated as \(Compliant Incidents/Total Incidents\)\*100.

    The Incidents Not Referencing a CI shows the total number of incidents which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those incident records.

    **Note:** Viewing all the data provided by Performance Analytics for this metric \(when drilling down\), requires the additional role of sn\_cmdb\_editor,itil, or sn\_incident\_read.

-   **Incidents Relating to both a Service and a CI**

    Percentage of incidents relating to both a service and a CI versus those incidents that don't. The complete set for this metric is all incident created in the last 60 days. Compliant records are those incidents in which both, the **cmdb\_ci** and the **business\_service** fields, are not empty.

    The percentage score for the metric is calculated as \(Compliant Incidents/Total Incidents\) \* 100.

    The Incidents Relating to Neither a Service nor a CI shows the total number of records which are not in compliance with the metric. Select the tile to drill down the PA widget for further details, such as the list all those incident records.

    **Note:** Viewing all the data provided by Performance Analytics for this metric \(when drilling down\), requires the additional role of sn\_cmdb\_editor,itil, or sn\_incident\_read. Click the tile to drill down the PA widget for further details, such as the list all those CIs.


