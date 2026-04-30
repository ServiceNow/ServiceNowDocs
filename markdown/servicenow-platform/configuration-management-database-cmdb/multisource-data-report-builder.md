---
title: Multisource Report Builder \(legacy\)
description: Improve CMDB data management by querying and reporting on Multisource CMDB data. Use the Multisource Report Builder to gain insights about how discovery sources are populating the CMDB and their reliability. You can then adjust reconciliation rules to improve the quality of CMDB data, if needed.Query the Multisource CMDB data to gain insights about how discovery sources are populating the CMDB, and then use that query to create a Multisource data report.After saving and running a Multisource query, create a schedule for the query to run automatically on a set schedule. Query results are stored in a results table and you can configure email addresses for the results to be sent to or include the results in CMDB dashboards.After creating, saving, running, and scheduling a Multisource \(CMDB 360\) query, you can create a Multisource \(CMDB 360\) report that integrates the query results with the platform Reporting feature. You can for example, include such Multisource \(CMDB 360\) report in the platform CMDB dashboards.Use sample queries to create your own CMDB 360/Multisource CMDB queries.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [CMDB 360/Multisource CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Multisource Report Builder \(legacy\)

Improve CMDB data management by querying and reporting on Multisource CMDB data. Use the Multisource Report Builder to gain insights about how discovery sources are populating the CMDB and their reliability. You can then adjust reconciliation rules to improve the quality of CMDB data, if needed.

## CMDB 360 in CMDB Workspace

Starting with the Zurich release, the Multisource CMDB feature is part of the CMDB 360 feature which is accessible in the CMDB Workspace. Create, view, modify, schedule, create reports, and run CMDB 360 queries using the [CMDB 360 query builder](cmdb-workspace-cmdb360-view.md) in the [CMDB Workspace](cmdb-workspace.md) store app. Use the CMDB 360 query builder to create queries of the following types:

-   [Get Records](../task/workspc-mltsrc-query-get-records.md): Queries your discovery sources for CIs that match your criteria.
-   [Find Gap](../task/workspc-mltsrc-query-find-gap.md): Queries for gaps in discovery sources reporting your CMDB 360 data. Queries discovery sources that report CIs against discovery sources that don't report those same CIs.
-   [Compare Attribute Values](../task/workspc-mltsrc-query-comp-attr-value.md): Queries for CIs with attribute values that differ across multiple discovery sources or against the CMDB. Queries at least two discovery sources and/or the CMDB for CIs that match your criteria.

## Legacy Multisource Report Builder

Instead of using the CMDB 360 query builder in CMDB Workspace, you can still use the legacy Multisource Report Builder as described in this topic.

After you create a Multisource query in the Multisource Report Builder, you can run the query to see the results. You can then also create a Multisource report that integrates the Multisource query results with the platform [Reporting](https://www.servicenow.com/docs/access?context=reporting-landing-page&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) capabilities. High level steps for creating a Multisource report:

1.  Create a query, then save and run it.
2.  Create a schedule for the query.
3.  Create a Multisource report that is based on the Multisource query.

You can create queries that find:

-   All the discovery sources populating data in your CMDB.
-   CIs not reported by any discovery source.
-   All CIs discovered by one discovery source, but not by another discovery source.

You can create other queries that show differences in CI attribute values between multiple data sources, while being compared to the CMDB:

-   Show how an attribute value is different between a discovery source and the current CMDB record. For example, find Hardware CIs with different location than what SCCM reports.

-   Show how an attribute is different between SourceA, SourceB, and SourceC. For example, show all Computer CIs where RAM is different between SCCM, ServiceWatch, and CMDB.


You can show query results by CI records, Multisource CMDB data records, or discovery sources. You can also limit the report results to CIs within a specific application service, technical service, or a CMDB group.

## Create a Multisource query

Query the Multisource CMDB data to gain insights about how discovery sources are populating the CMDB, and then use that query to create a Multisource data report.

### Before you begin

[Enable and configure CMDB 360](multisource-cmdb.md).

Role required: cmdb\_ms\_editor

### About this task

The Multisource Report Builder page updates dynamically as you set fields. Therefore, some of the fields that are described in the steps below might not appear.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Multisource Report Builder​**.

2.  On the Multisource Report Builder page, select a query to edit or run, or click **New**.

3.  Enter **Name** and **Description** for the query.

4.  Select the **Result type** for the query.

    -   **CI records**: Results show unique CIs from the Multisource CMDB data store.
    -   **Multisource data records**: Results show all entries of CI/discovery source combinations from Multisource CMDB data.
    -   **Discovery sources​**: Results are grouped by discovery sources that match the query criteria.
5.  Select **Only show difference** to show differences in CI attribute values and then select the **Type of difference**.

    -   **Between CMDB record and discovery source**: Show differences in attribute values between the CMDB data and the specified discovery sources.
    -   **Between discovery sources**: Show differences in attribute values between specified discovery sources based on Multisource data.
6.  Select the **Class** to apply the query to, or select **All Classes** to apply the query to all classes. Use the condition builder to specify conditions that must be met for the class. Use **And** or **Or** to specify multiple conditions.

7.  Use the list collector to select one or more **Discovery source** items to query on.

8.  Set **Field to compare** to the class attributes for which to show differences.

    Use the OR and AND operators to compare based on multiple attributes. The list of attributes is a pre-populated subset of the class attributes, to which you cannot add or remove items.

9.  Set **Limit results to** to limit the query results to CIs that belong to a specific application service, technical service, or a CMDB group.

10. Click **Save** and then click **Run**.


### What to do next

-   On the CMDB Multisource Query Results page:
    -   If the number of results exceeds the number of results appearing on the page:
        -   Click **Load More Results​**: To show the next page of results. The number of results that appear on each result page is specified by the [glide.identification\_engine.multisource.query.batch.limit](../reference/components-multisource-cmdb.md) system property \(100 items by default\).
        -   Click **Load All Results**: To show all results, up to the limit specified by the [glide.identification\_engine.multisource.query.max.limit](../reference/components-multisource-cmdb.md) system property \(10000 by default\).
        -   Click a Multisource CMDB value link or a CI value link to access the respective records and see more details.
    -   In the Configuration Item column, click a CI link to open the CI form. In the Related Links section on the CI form, click the **Multisource Data** tab to show Multsource data, such as discovery sources, related to the CI.
-   Create a schedule for the query and ensure that the schedule runs at least once. This step is required for creating a Multisource report.

    **Note:** Initially, after creating a query, both the **Create Schedule** and the **Create Report** buttons are grayed out. Only after saving the query, you can create and run a schedule for the query, and only then you can create a report that is based on the query.


## Schedule a Multisource query

After saving and running a Multisource query, create a schedule for the query to run automatically on a set schedule. Query results are stored in a results table and you can configure email addresses for the results to be sent to or include the results in CMDB dashboards.

### Before you begin

The query for the schedule must be already saved and run at least one time.

Role required: cmdb\_ms\_user

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Multisource Report Builder​**.

2.  On the Multisource Report Builder page, select the query that you want to create a schedule for.

3.  On the Multisource Report form, click **Create Schedule**.

4.  On the Scheduled Email of Multisource Report Builders, click **New**.

5.  Fill in the Scheduled Email of Multisource Report Builders form.

<table id="table_pvh_hcg_ltb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Query

</td><td>

Saved query that was created in Multisource Report Builder.

</td></tr><tr><td>

Users

</td><td>

Users to email the query results to.

</td></tr><tr><td>

Groups

</td><td>

User groups to email the query results to.

</td></tr><tr><td>

Run

 Time

</td><td>

Frequency and time to run the query automatically.

 When you set **Run** to **On Demand**, the query runs only when you run it manually.

</td></tr><tr><td>

Email addresses

</td><td>

More ad-hoc email addresses to email the query results to.

</td></tr><tr><td>

Subject

</td><td>

Text that will appear as the subject of the email with the query results.

</td></tr><tr><td>

Introductory message

</td><td>

Text that is included in the body of the email with the query results.

</td></tr><tr><td>

Type

</td><td>

Type of the file with the query results, which will be attached to the email.

</td></tr><tr><td>

Zip output

</td><td>

Enables zipping of the results file.

</td></tr><tr><td>

Conditional

</td><td>

Enable a condition for running the query and specify the condition in the **Condition** field. If the specified condition isn't met, the query doesn't run.

</td></tr><tr><td>

Condition

</td><td>

Condition that must be met for the query to run \(Java script\).

 Appears only if **Conditional** is selected.

</td></tr><tr><td>

Omit if no records

</td><td>

Disable sending an email for a query run that returns no results.

</td></tr></tbody>
</table>    **Note:** When using [update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=zurich&pubname=zurich-application-development&ft:locale=en-US) to port Multisource schedules from a non-production to a production environment, check the **Users** and **Groups** settings in the schedule. Any user or group that doesn't exist in the production environment, and which needs to receive the query results, must be re-added in either of the following ways:

    -   Manually created in the production environment. In this case, you must also remove the invalid user or group in the production environment \(ported from non-production environment\) from any schedules and add the new user or group instead.
    -   Explicitly ported from the non-production to production environment.
6.  Click **Submit**.


### What to do next

-   If **Run** is set to **On Demand** in a schedule, or if you need to run a query randomly even if it has a recurring schedule, you can manually run that query as follows:
    1.  Navigate to **All** &gt; **Configuration** &gt; **Multisource Report Schedules**.
    2.  In the Scheduled Email of Multisource Report Builders list view, select the query that you want to run.
    3.  On the Scheduled Email of Multisource Report Builder form, click **Execute Now**.
-   Create a Multisource report for the query, that integrates the Multisource query results with the platform [Reporting](https://www.servicenow.com/docs/access?context=reporting-landing-page&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) feature.

## Create a report based on a Multisource \(CMDB 360\) query

After creating, saving, running, and scheduling a Multisource \(CMDB 360\) query, you can create a Multisource \(CMDB 360\) report that integrates the query results with the platform Reporting feature. You can for example, include such Multisource \(CMDB 360\) report in the platform CMDB dashboards.

### Before you begin

The Multisource \(CMDB 360\) query for the report must be already saved, have a schedule, and must have already run at least once.

Role required: cmdb\_ms\_user

### About this task

Creating a report that is based on a Multisource \(CMDB 360\) query, creates a report source which you can then manage using [Reporting](https://www.servicenow.com/docs/access?context=reporting-landing-page&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) capabilities.

**Note:** If you are using the [CMDB 360 view in CMDB Workspace](cmdb-workspace-cmdb360-view.md) to generate the CMDB 360 query and the report, you can skip to step 4 in the procedure below.

### Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Multisource Report Builder​**.

2.  In the Multisource Report Builder list view, select the query that you want to create a schedule for.

3.  On the Multisource Report form, click **Create Report**.

4.  On the Create a report form, click **Save** or **Run**.


A report shows the results for the most recent query run. If meanwhile the query has changed, then the report shows results that are out of synchronization with the query. When you update the query, ensure to immediately run the updated query so that the report is synchronized with the query.

### What to do next

To add a Multisource \(CMDB 360\) report to the CMDB Correctness Dashboard for example, see [Add a report to a dashboard](https://www.servicenow.com/docs/access?context=add-report-to-dashboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

## Sample CMDB 360/Multisource CMDB queries

Use sample queries to create your own CMDB 360/Multisource CMDB queries.

|Field|Setting|
|-----|-------|
|Name|Discrepancy in multiple attributes between multiple discovery sources \(discovery source vs. discovery source\)|
|Description|Find Linux servers with name containing “backup” which have discrepancy in **Disk Capacity** OR **CPU Count** OR **Serial Number** between discovery sources ServiceNow/ServiceWatch/SCCM/Tivoli.|
|Result type|Multisource data records|
|Only show difference|Selected|
|Type of difference|Between discovery sources|
|Class|Linux Server \[cmdb\_ci\_linux\_server\]|
|Conditions|\[Name\] \[contains\] \[backup\]|
|Discovery Source|ServiceNow/ServiceWatch/SCCM/Tivoli|
|Field to compare|**Disk Capacity** OR **CPU Count** OR **Serial Number**|
|Limit results to|All|

|Field|Setting|
|-----|-------|
|Name|Discrepancy in multiple attributes between multiple discovery sources \(CMDB vs. discovery sources\)|
|Description|Find Linux Servers with name containing “backup” which have discrepancy in **Disk Capacity** AND **CPU Count** AND **Fully Qualified Domain Name** for discovery sources ServiceNow/ServiceWatch/SCCM|
|Result type|Multisource data records|
|Only show difference|Selected|
|Type of difference|Between CMDB record and discovery source|
|Class|Linux Server \[cmdb\_ci\_linux\_server\]|
|Conditions|\[Name\] \[contains\] \[backup\]|
|Discovery Source|ServiceNow/ServiceWatch/SCCM|
|Field to compare|**Disk Capacity** AND **CPU Count** AND **Fully Qualified Domain Name**|
|Limit results to|All|

<table id="table_kky_fw4_rlb"><thead><tr><th>

Field

</th><th>

Setting

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Missing Discovery by Tivoli

</td></tr><tr><td>

Description

</td><td>

Servers discovered by ServiceNow but not by Tivoli

</td></tr><tr><td>

Result type

</td><td>

CI records

</td></tr><tr><td>

Class

</td><td>

Server \[cmdb\_ci\_server\]

</td></tr><tr><td>

Discovery Source

</td><td>

\[is\] \[ServiceNow\]

 \[is not\] \[Tivoli\]

</td></tr><tr><td>

Limit results to

</td><td>

All

</td></tr></tbody>
</table><table id="table_qmh_vw4_rlb"><thead><tr><th>

Field

</th><th>

Setting

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Discovery Sources Backup Servers

</td></tr><tr><td>

Description

</td><td>

All discovery sources for backup servers

</td></tr><tr><td>

Result type

</td><td>

Data sources

</td></tr><tr><td>

Class

</td><td>

Server \[cmdb\_ci\_server\]

 and class condition:

 \[Host name\]\[starts with\]\[backup\]

</td></tr><tr><td>

Limit results to

</td><td>

All

</td></tr></tbody>
</table><table id="table_gzg_cy4_rlb"><thead><tr><th>

Field

</th><th>

Setting

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Compare Location-Altiris vs. Tivoli

</td></tr><tr><td>

Description

</td><td>

List all Multisource CMDB records where the reported value of Location is different between Altiris and Tivoli discovery sources

</td></tr><tr><td>

Result type

</td><td>

Multisource data records

</td></tr><tr><td>

Only show difference

</td><td>

Selected

</td></tr><tr><td>

Type of difference

</td><td>

Between discovery sources

</td></tr><tr><td>

Discovery Source

</td><td>

-   Altiris
-   Tivoli

</td></tr><tr><td>

Field to compare

</td><td>

Location

</td></tr><tr><td>

Limit results to

</td><td>

All

</td></tr></tbody>
</table>|Field|Setting|
|-----|-------|
|Name|Linux Server Location - Diff than Tivoli value|
|Description|All Multisource CMDB records for Linux Server, where the Location value is different than the value reported by Tivoli.|
|Result type|Multisource data records|
|Class|Linux Server|
|Only show difference|Selected|
|Type of difference|Between CMDB record and discovery source|
|Discovery Source|\[is\]\[Tivoli\]|
|Field to compare|Location|
|Limit results to|All|

