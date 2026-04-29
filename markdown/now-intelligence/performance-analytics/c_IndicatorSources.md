---
title: Indicator sources
description: Indicator sources are data sets consisting of filtered records from one table or database view.To provide a filtered data set of records that you can evaluate with one or more indicators, create an indicator source.You can select a database view as the facts table in an indicator source. Database views enable you to combine data from tables in your ServiceNow instance that are not connected by default.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Indicators, Configure fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Indicator sources

Indicator sources are data sets consisting of filtered records from one table or database view.

An indicator source configuration specifies a table, such as Incident \[incident\], conditions for filtering records from that table, and a frequency that you base on the conditions. Supported tables include database views and Workflow Data Fabric tables. An indicator source cannot specify a rotated table. Multiple indicators can use the same indicator source. Data collection jobs query the database once for each indicator source. Thus, all indicators that use the same indicator source get data from the same point in time.

Typically, an indicator tracks the situation on a certain date. The indicator source conditions should include a date-related filter, such as `[Opened][on][Today]`. Indicators collected less frequently might specify a larger date range, such as `[Closed][on][This month]`.

Create indicator sources carefully. Since multiple indicators may be linked to an indicator source, it is not easy to change the indicator source after you created it. Furthermore, changing an indicator source can cause a disjoint with scores that you have already collected.

**Note:** Indicator sources must be created before you can create an indicator.

## Define an indicator source

To provide a filtered data set of records that you can evaluate with one or more indicators, create an indicator source.

### Before you begin

Look at the list of indicator sources, for these reasons:

-   An indicator source that meets your requirements may already exist. To help maintain your instance, you should not create duplicate indicator sources.
-   Ensure that you give a unique name to any indicator source that you create. Giving the same name to different indicator sources can be confusing.

Role required: pa\_data\_collector or admin

### Procedure

1.  Use one of the following navigation paths:

    -   If you are on an upgraded instance that has not migrated to Platform Analytics, navigate to **All** &gt; **Performance Analytics** &gt; **Sources** &gt; **Indicator Sources** and select **New**.
    -   If you are on a new instance or have migrated to Platform Analytics, navigate to **All** &gt; **Platform Analytics Administration** &gt; **Data Sources** &gt; **Indicator Sources** and select **New**.
2.  Enter a unique **Name** by which you can easily see what the indicator source is used for, such as **Incidents.Open**.

3.  Add a detailed **Description** to help others understand the use and purpose of this indicator source and to help them avoid creating duplicates.

4.  In the **Calendars** field, select either the standard calendar or a business calendar that is defined on the instance.

    **Warning:** If you use a business calendar and later alter that business calendar's entries, you invalidate your Performance Analytics data. The scores you collected before changing the entries will not be compatible with the scores you collect after you change the entries. This warning also applies to fiscal calendar schedules.

    If you use a business calendar, you can create data collection jobs that run on the Business Calendar: Entry start or Business Calendar: Entry end times.

5.  Fill either the **Valid for frequency** or **Calendar Frequency** field.

    -   If you select the standard calendar, you have the **Valid for frequency** field. This field gives you a choice of standard indicator frequencies. The default choice is **Daily**.
    -   If you select a business calendar, you have the **Calendar Frequency** field. This field is required. The business calendar you selected determines the range of frequencies that are available.
    Indicators based on this indicator source use the value of this field as the indicator **Frequency**. By default, the score collection periods on the indicators follow this frequency. You can override this behavior on the indicator record.

    If you are uncertain about the frequency to set, base the frequency on your business cycle.

6.  Select a facts table, either directly or by reusing a report source.

<table id="choicetable_bwt_24j_dbb"><thead><tr><th align="left" id="d139594e279">

Field

</th><th align="left" id="d139594e282">

Description

</th></tr></thead><tbody><tr><td id="d139594e288">

**Facts table**

</td><td>

Specify the facts table and any conditions for filtering the records of that table. You can specify a [database view](performance-analytics-glossary.md#) as the facts table. Remote tables are not supported, but Workflow Data Fabric tables are supported.

</td></tr><tr><td id="d139594e304">

**Report source**

</td><td>

Specify an existing report source to reuse. A report source specifies a facts table and filtering conditions.If the report source changes, a warning appears when you view the indicator source to inform you about the change. To update the indicator source, click the refresh button next to the **Report source** field.

</td></tr></tbody>
</table>    **Warning:**

    -   Performance Analytics does not support remote tables.
    -   Performance Analytics does not support Workflow Data Fabric tables.
    -   Do not change the facts table for a source after you have started collecting data. If you change the facts table, you lose all historical scores for the associated indicators at the next score collection.
7.  If you select a facts table directly, add **Conditions** that must be fulfilled before the data is included in the subset.

    For example, set the conditions `[Active] [is] [true]` or `[Created] [at or before] [date]`.

    **Tip:**

    -   Indicator source conditions on text fields are not case-sensitive.
    -   Conditions set on indicator sources and indicators all apply.
    -   For an indicator to display real-time scores, set a condition either on the indicator or the indicator source.
    -   Due to the reusability of indicator sources, use only high-level criteria to define indicator source conditions. Use the advanced filters on individual indicators to go deeper into the data.
    -   Indicator sources should have at least one date condition, such as \[Created\]\[on\]\[Today\].
    -   Usually, your date conditions should refer to the same time period as the indicator frequency. For example, conditions about the number of days should only be on daily indicators. Conditions about the number of months should only be on monthly indicators.
    -   Avoid dot-walking to the sys\_id or display value of a table. Instead, use the reference field by itself, to avoid creating unnecessary joins.
    -   If you design the indicator source conditions well, at least one of the indicators on that source does not have any additional conditions of its own.
    For general information about building conditions, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

8.  Define **RELATED LIST CONDITIONS** to include a relationship with another table in the filter.

    For more information, see [Add related list conditions](https://www.servicenow.com/docs/access?context=create-related-list-query&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

9.  To see how many records this indicator source would return, click **Preview**.

    **Warning:**

    You may exceed the maximum limit of collected records despite what the Preview function shows. The Preview function shows you a lower number of records than the number that the data collector actually fetches. The Data Collection job ignores ACLs and business rules when fetching records, but the Preview function follows them. For more information, see [KB0756238](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=bf1399dedb7e0150e515c22305961986).

10. In the Records View tab, in **List view**, select the default view.

    The default view applies on Workbench widgets and to the lists of records collected for this indicator source on the Analytics Hub and KPI Details. The available views vary depending on the facts table.

11. In the Records Collection tab, override the maximum number of records that a job can collect for a single indicator source, for this indicator source only.

    Select **Override record collection**, then enter a value in **Maximum number of records collected**. You are overriding the default value set on the property **com.snc.pa.dc.max\_row\_count\_indicator\_source**. For more information, see [Performance Analytics properties](../reference/pa-properties.md).

12. Expand the context menu and click **Save**.

13. If you have configured this indicator source to use a business calendar, set the number of periods for retaining scores and snapshots and for finding seasonal patterns.

    These settings apply to all indicator sources and indicators that use the same calendar frequency. The owner of an indicator can override these settings for that indicator. If you do not set these values in the indicator source, the first time someone creates an indicator using this calendar frequency, they are prompted to set these values.

    1.  In the Related Links, click **Configure retention periods**.

        A PA Business Calendar Retention Period record opens.

    2.  In the **Number of entries to establish seasonality** field, enter the number of time periods, as defined in the business calendar or schedule entries, that are necessary to find seasonal patterns.

        For more information about business calendar entries, see [Creating business calendars](https://www.servicenow.com/docs/access?context=business-calendars&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

    3.  Set the number of time periods, as defined in the business calendar or schedule entries, to retain scores and snapshots.

        A default value of one is provided, but you should consider changing it.


### Simple indicator source

The following settings create an indicator source that collects new incidents daily:

-   **Name**: `Incidents.New`
-   **Frequency**:`Daily`
-   **Facts table**:`Incident [incident]`
-   **Condition**:`[Opened] [on] [Today]`

![Create indicator sources](../image/CreatingIndicatorSources.png "Create indicator sources")

### What to do next

After you create an indicator source, you can define text index configurations in a related list on the record. Use these configurations to create Performance Analytics text widgets with word clouds. For more information, see [Set up text analytics](../task/set-up-text-analytics.md).

If you are reusing a report source and the report source changes, a warning appears on the indicator source record. To update the indicator source to match the report source, click **Update report source**. You can also click the refresh button next to the **Report source** field.

The read-only **Report source updated at** field displays the last time the report source was updated. This date and time always appear in the GMT time zone.

**Related topics**  


[Report sources](../../reporting/concept/c_ReportSources.md#)

[Creating business calendars](https://www.servicenow.com/docs/access?context=business-calendars&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

## Use a database view in an indicator source

You can select a database view as the facts table in an indicator source. Database views enable you to combine data from tables in your ServiceNow instance that are not connected by default.

### Before you begin

Role required: pa\_admin

### About this task

By joining tables in a database view, you can easily access them by calling up the view. Then you can select fields from any of the tables included in the view. For example, if you want to report on the number of SLAs breached, you need fields from both the SLA and the Incident tables.

### Procedure

-   If you select a database view as the facts table for an indicator source, provide additional configuration in the **Records view** section of the Indicator Source form.

    ![Records View section on indicator source form](../image/indicator-source-record-view.png "Records View section on the indicator source form")

<table id="table_lrc_1p5_dmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View Table

</td><td>

A snapshot of records is collected from only one table in the database view. Select which table has its records collected.**Important:** If you change this value, you effectively remove all earlier snapshots. This change takes effect the next time that the data collection job runs. This change does not affect historical scores.

</td></tr><tr><td>

List View

</td><td>

Select the list view used to display collected record sets. **Default view** is suggested, but you can select any defined view, such as **Workspace**.

</td></tr></tbody>
</table>    **Note:** If you collect second-level breakdowns on a view table that does not generate unique system IDs, the score and the number of records may disagree. If these values disagree, the score is correct. The record count is wrong because it is an artifact of non-unique sys\_ids.


### Indicator source from database view

Let's say you want to create some indicators tracking the number of incidents that violate SLAs. You already have a database view included in your base system called incident\_sla, which joins the Task SLA \[task\_sla\] and Incident \[incident\] tables. Therefore, you create a new indicator source using this database view.

Looking at the database view, you see that it gets the records where the task on the Task SLA table matches the unique sys\_id value on the Indicator table.

![Database view tables list with Where clause highlighted](../image/ind-source-db-view-where-clause.png)

You can only take snapshots from one table, and it is generally better to take snapshots of the table with a field with unique values. Therefore, you select Incident \[incident\] as the View table on the indicator source.

![Records view tab](../image/ind-source-db-view-table.png)

**Related topics**  


[Database views](https://www.servicenow.com/docs/access?context=c_DatabaseViews&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

