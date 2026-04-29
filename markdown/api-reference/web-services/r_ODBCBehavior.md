---
title: ODBC behavior
description: After testing the ODBC driver, you can use it to query your instance database from a variety of client applications.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# ODBC behavior

After testing the ODBC driver, you can use it to query your instance database from a variety of client applications.

## ODBC aggregate functions

The ODBC driver attempts to download data and apply aggregate functions locally. The ODBC driver supports the following aggregate functions.

-   COUNT
-   SUM
-   MIN
-   MAX
-   AVG

Activate the Aggregate web service plugin to improve the performance of aggregate queries through the ODBC driver.

## ODBC date and time values

The instance and the machine on which the ODBC driver is installed may use two different time zones. Date and time values returned by the ODBC driver are in the local time zone of the application using the driver, not the ServiceNow instance time zone.

Ensure that you query in accurate time zones for both the instance and the machine that hosts the ODBC driver. GlideRecord performs filtering based on the instance time zone, and the ODBC client is filtered based on the Windows time zone.

For example, an instance is in Central Standard Time \(CST\), and the ODBC driver is installed on a machine that is in Pacific Standard Time \(PST\). An incident is created on the instance at `2014-05-20 10:00:00`, and the time that the incident was created is displayed in the UI as `10:00:00` for users in both time zones. However, in order to successfully query this incident by creation date and time, a user on the machine in PST must query `2014-05-20 08:00:00` instead of `2014-05-20 10:00:00`.

Duration and timer type fields are returned using the UTC time zone, starting with ODBC version 1.0.10. See [KB0583982](https://support.servicenow.com/kb_view.do?sysparm_article=KB0583982) for details about this change.

## ODBC display values

Some examples of how to use and work with ODBC display values are shown below.

-   Display values in **Choice** and **Reference** columns:

    When querying a column of type **Choice**, **Reference**, **Duration**, or **Timer**, an additional column with the prefix `dv_` is available that contains the display value. For example, you can select **dv\_caller\_id** to return the **sys\_user.name** display value of the reference field from an incident record without making another request to the sys\_user table.

    ![Return the display value](../image/ReturnTheDisplayValue.png "Return the display value")

-   Display values in filter conditions:

    Display values can also be used in a filter condition. The ODBC driver optimizes the query condition and processes the filter on the server, for example, querying on the display value of **sys\_user** for the **caller\_id** field of an incident by using the **dv\_caller\_id** field name.

    ![Display values in filter conditions](../image/DisplayValuesInFilterConditions.png "Display values in filter conditions")

-   Display values in aggregate queries:

    Aggregate queries can also take advantage of display values if you specify them in the group by or where clause, for example, grouping on the **caller\_id** field of an incident, as well as specifying a filter for it. The query is optimized by passing through to the server.

    ![Display values in aggregate queries](../image/DisplayValuesInAggregateQueries.png "Display values in aggregate queries")


## Querying table and column names

You can get a list of accessible tables and columns based on the read ACLs for the querying user.

-   The following query returns the names of all tables for which the querying user has read access:

    `select * from oa_tables;`

-   After you know the name of the table you want to query, you can query the names of all columns for which the user has read access. The querying user must have read access for both the table and the columns.

    `select * from oa_columns where table_name=‘table_name’;`


**Note:** The oa\_tables and oa\_columns tables are internal ODBC tables. These tables are accessible only via the ODBC driver.

## Routing ODBC calls to Read Replica

Query routing is done to take the load off the primary database for SELECT queries that take numerous DB CPU cycles on the primary DB. For more information, see [Introduction to ServiceNow Read Replica Databases](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0824441).

For routing ODBC calls to Read Replica, go to **All** &gt; **Secondary Database** &gt; **Secondary DB Categories** and set **odbc** to `true`.

-   **[Increase the field length in SQL queries](../task/t_IncreaseTheODBCOutputFieldSize.md)**  
The ODBC driver limits the field length in SQL queries to the maximum length defined by the ServiceNow dictionary entry. You can increase the maximum field length to avoid truncating data.

**Parent Topic:**[Create data sources from other apps using ODBC driver](../concept/c_ODBCDriver.md)

