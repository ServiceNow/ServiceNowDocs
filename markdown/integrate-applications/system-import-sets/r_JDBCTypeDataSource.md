---
title: JDBC type data source
description: A JDBC data source retrieves its data via a JDBC driver, usually type 4 network.Extend the available JDBC driver options by creating a new choice list entry to specify the JDBC driver Java package name.Extend the available JDBC driver options by activating the Sybase or DB2 choices.You can install a new JDBC driver JAR file to a MID server to access database formats that are not supported by default.Add a new JDBC data source by defining a data source record.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Data sources, Import sets, Imports, Data and Automation]
---

# JDBC type data source

A JDBC data source retrieves its data via a JDBC driver, usually type 4 network.

The JDBC connection is available either directly from the ServiceNow instance \(a VPN setup required\), or via a dedicated MID Server installed inside your firewall that can access the database port.

**Note:** JDBC calls from the MID Server are never encrypted. Limit the rights available to the MID Server user whenever making JDBC calls from a MID server.

## JDBC data source supported database formats

JDBC data sources support several database formats and ports.

|SQL Server Type|Port|
|---------------|----|
|MySQL|3306|
|Microsoft SQL Server|1433|
|Oracle|1521|

**Note:** Oracle DATE fields are loaded as ServiceNow Date/Time fields.

## JDBC data source SQL statement requirements

JDBC queries that run SQL statements must specify a column name.

For example, this query specifies the column name **ServerID**.

```
SELECT DISTINCT 'server_name:' + CONVERT ( VARCHAR , lg .ResourceID ) AS 'ServerID' 
,LastHWScan
,Account0
,Category0
Fromv_GS_WORKSTATION_STATUSsInner  JOIN
v_GS_LocalGroupMembers0lg
ON s .ResourceID  = lg .ResourceID
WhereType0  = 'Local' AND Category0  = 'SystemAccount'
```

## SQL server integrated authentication for Windows

A JDBC data source can use the ID of for the Windows MID Server service user to authenticate with SQL Server.

The **Use integrated authentication** check box on the Data Source form determines if the JDBC data source uses the MID Server service user credentials. For this field to appear on the Data Source form, the integration must meet these criteria:

-   The MID Server must be running on a Windows computer with SQL Server.
-   The MID Server service must use the same credentials that SQL Server requires.
-   The data source **Type** is JDBC.
-   The data source **Use MID Server** check box is selected.
-   The data source **Format** is SQLServer.

**Important:** If integrated authentication is chosen, and you are integrating with Microsoft System Center Configuration Manager, the account running the MID Server service must have read rights on the SCCM database.

![Data Source form](../image/JDBC_SQLServerIntegratedAuth.png "Data Source form")

**Note:** The **Last run database field** on the JDBC data source is case-sensitive for the SQL server.

## Adding JDBC drivers for unsupported database formats

Use the following procedure to extend the data source to use a driver for a database that is not provided in the base system. JDBC connections are supported for the following default databases:

## Add a new JDBC format choice

Extend the available JDBC driver options by creating a new choice list entry to specify the JDBC driver Java package name.

### Before you begin

Role required: import\_admin

### About this task

Add a new choice list entry for the new database to the **Format** field in the **sys\_data\_source** table.

### Procedure

1.  Navigate to **System Import Sets &gt; Administration &gt; Data Sources**.

2.  Click **New**.

3.  In the Data Sources form, right-click the **Format** field label, and select **Show Choice List** from the pop-up menu.

    ![JDBC source list](../image/jdbc-choice-list.png)

4.  Click **New** in the list of choices.

5.  Provide the following values to create the new database choice.

    Look at the existing drivers for examples.

    -   Table: **sys\_data\_source**
    -   Label: Database name that appears as an option in the **Format** choice list, for example: Teradata.
    -   Value: Package name and class of the driver. For example, the value for TeraData is **com.ncr.teradata.TeraDriver**.

        **Note:** The driver package and class must be provided by the driver vendor. This information is often available in the vendor's documentation, such as for [MariaDB](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) or [Teradata](https://developer.teradata.com/doc/connectivity/jdbc/reference/current/faq.html).

    -   Dependent value: JDBC
    ![JDBC choice list.](../image/edit-jdbc-choice-list.png)

6.  Click **Submit**.

    The new data source now appears in the list of available JDBC formats.


## Add Sybase or DB2 JDBC format choices

Extend the available JDBC driver options by activating the Sybase or DB2 choices.

### Before you begin

Roles required: admin

**Important:** To use Sybase or DB2 JDBC drivers, you must manually install the driver JAR file on a MID server. Refer to [KB0551236](https://support.servicenow.com/kb_view.do?sysparm_article=KB0551236) for more information.

### About this task

Activate the Sybase or DB2 JDBC drivers to connect with those database formats through a MID server. This procedure assumes you are using the following Sybase or DB2 drivers:

|Format|Driver|Driver class|
|------|------|------------|
|Sybase|jconnect-jdbc|com.sybase.jdbc3.jdbc.SybDriver|
|DB2|db2jcc|com.ibm.db2.jcc.DB2Driver|

If you are using a different implementation of the Sybase or DB2 driver, you must modify the choice **Value** to use the driver class from your driver implementation.

### Procedure

1.  Navigate to **System Import Sets &gt; Administration &gt; Data Sources**.

2.  Click **New**.

3.  In the **Type** field, select **JDBC**.

4.  Right-click the **Format** field label, and select **Configure Choices** from the pop-up menu.

5.  Move the **Sybase** or **DB2 Universal** choices from the **Available** column to the **Selected** column.

6.  Click **Save**.

    The new data source now appears in the list of available JDBC formats.


## Install a driver on a MID Server

You can install a new JDBC driver JAR file to a MID server to access database formats that are not supported by default.

### Before you begin

Role required: agent\_admin

### Procedure

1.  Navigate to **MID Server &gt; JAR Files**.

2.  Click **New**.

3.  Complete the following fields:

    -   Name: A unique and descriptive name for identifying the file in the instance.
    -   Version: A version number for the file, if one is available.
    -   Source: Location of the JAR file for reference purposes. Source information is not used by the system.
    -   Description: Short description of the JAR file and its purpose in the instance.
4.  Click the paper clip icon in the banner and attach the JAR file to the record.

    ![Attach a file](../image/JARFileSync.png)

5.  Click **Submit**.

6.  Restart the MID Server service.

    The platform makes the JAR file available to any MID Server configured to communicate with the instance.


## Create a new JDBC data source for an unsupported database format

Add a new JDBC data source by defining a data source record.

### Before you begin

Role required: import\_admin

### Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Data Sources** and click **New**.

2.  In the Data Source form, select **JDBC** from the list in the **Type** field.

3.  Select the new data source from the choice list in the **Format** field.

    ![JDBC Data Source](../image/JDBCDataSource.png)

4.  [Configuring the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and add the **Connection URL** field.

5.  Provide the connection URL to the JDBC data source, and then click **Submit**.

    No other connection information is required.

    ![JDBC Data Source](../image/CompleteJDBCDataSource.png)


