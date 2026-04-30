---
title: Configure the SCCM integration and schedule an import
description: Importing data from Microsoft SCCM requires a connection to the SCCM database via a JDBC data source and a schedule that tells the MID Server when to fetch the data.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Microsoft SCCM integration, ServiceNow provided integrations, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure the SCCM integration and schedule an import

Importing data from Microsoft SCCM requires a connection to the SCCM database via a JDBC data source and a schedule that tells the MID Server when to fetch the data.

## Before you begin

You must have sufficient credentials to query the SQL Server that contains the SCCM database. Create a SQL Server account in order to connect to the SCCM database on the MID Server to use the data sources.

Connect to your SCCM SQL Server and configure the following:

1.  Create a new login user name and password for SQL Server authentication.
2.  Choose the SCCM database that ServiceNow data sources will connect to.
3.  Assign the 'db\_datareader' role membership to the new user.

Role required: admin

## About this task

The system uses the details of the database connection you create in this procedure to configure the default SCCM data sources automatically.

**Note:** If you want to configure the JDBC data source to authenticate on your SQL Server database using the Windows MID Server service user, select the **Use integrated authentication** box on each of the existing data sources.

## Procedure

1.  Navigate to **All** &gt; **Integration - Microsoft SCCM &lt;version&gt;** &gt; **Setup**.

2.  Complete the required fields to configure connection to the SCCM SQL database. Make sure to include a valid MID Server that has access to the SQL database server.

    ![SCCM data import setup](../image/SCCMIntegrationSetup.png "SCCM data import setup")

3.  Under Related Links, click **Test data source connections** to test the connection to the SCCM database.

4.  If the data source connects to the SCCM database, navigate to **Integration - Microsoft SCCM** &gt; **Scheduled Import**.

    The Scheduled Data Import form appears for your version of the SCCM integration. The Computer Identity data source runs first. The other data sources listed on the form run in sequence, based on their default order.

    ![](../image/SCCM_Import_Schedule.png)

5.  Select a calendar interval \(Day, Week, etc.\) in the **Run** field and specify the time of day the import should run.

    Your selection displays additional fields required to complete the schedule.

6.  Click **Update** to schedule the import or click **Execute Now** to perform the import immediately.

    After the instance imports data using the **SCCM &lt;version&gt; Computer Identity** data source, the other data sources run in the order configured to retrieve the remainder of the SCCM data.


**Parent Topic:**[Microsoft SCCM integration](../concept/c_MicrosoftSCCMIntegration.md)

