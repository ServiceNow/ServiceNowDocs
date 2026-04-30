---
title: Parameters
description: The following parameters are available in a direct JDBC probe.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [JDBCProbe, Supported integration interfaces, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer]
---

# Parameters

The following parameters are available in a direct JDBC probe.

<table id="table_k4c_ywv_4y"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**jdbc\_driver**

</td><td>

Required. Java class name for the JDBC driver to use, the currently supported drivers are:-   Oracle: `oracle.jdbc.OracleDriver`
-   Microsoft SQL Server: `com.microsoft.sqlserver.jdbc.SQLServerDriver`
-   MySQL: `com.mysql.jdbc.Driver`

</td></tr></tbody>
</table>**Example**

```
com.microsoft.sqlserver.jdbc.SQLServerDriver
```

<table id="table_dtt_fwv_4y"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**connection\_string**

</td><td>

Required. The JDBC connection string/URL for defining the connection usually contains information about the database server and name, the user ID, and password for connecting to the database. The syntax is vendor-specific. See the following links for reference:-   Oracle: `[jdbc:oracle:thin:<username/password>@<database>]`
-   Microsoft SQL Server: `[jdbc:sqlserver://localhost;user=MyUserName;password=*****;]`
-   MySQL - `[jdbc:mysql://localhost/database?user=username%26password=passwd]`

</td></tr></tbody>
</table>**Example**

```
jdbc:sqlserver://xxx.service-now.com;
databaseName=SMS;
user=sms_user;
password=sms_password;
```

<table id="table_wvq_5vv_4y"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**work**

</td><td>

Required if not using the **table\_name** parameter short cut. Parent element of an XML fragment describing the SQL command to execute.

</td></tr></tbody>
</table>**Example**

```
...
  <parameter name= "work" ><select table = "System_DATA" where = "InstanceKey=692" ><MachineID /><SMSID0 /></select></parameter>
  ...
```

|Parameter|Description|
|---------|-----------|
|**query\_timeout**|Optional during SELECT. Number of seconds the JDBC driver waits for a `query (SELECT)` to complete. Zero means no timeout. If timeout is exceeded, the integration considers the JDBC result inaccessible and places it in an error state.|

<table id="table_c2c_z5v_4y"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**table\_name**

</td><td>

Optional \(except required during `count_rows == true`\).Alternate way of executing a `select *` query; instead of using the **work** element. Equivalent to executing `select * from <table_name>`.

</td></tr></tbody>
</table>|Parameter|Description|
|---------|-----------|
|**count\_rows**|Optional. Indicates whether a `select count(*)` query should return the number of rows \(true/false\). The result of the count is returned as a **row\_count**element in the **result** element.|

|Parameter|Description|
|---------|-----------|
|**query**|Optional. Type of query. Possible choices are "All Rows from Table" or "Specific SQL." If "Specific SQL", the sql\_statement will be required to specify the SQL statement.|

|Parameter|Description|
|---------|-----------|
|**sql\_statement**|Optional. Use a specific SQL query. The presence of this element executes a direct query specified in the value attribute.|

**Example**

```
...
  select * from any_table where id = 123
  ...
```

|Parameter|Description|
|---------|-----------|
|**skip\_sensor**|Optional. Determines if Discovery attempts to process the ECC input from the JDBCProbe. Default = true|

For example, to query a table using a direct JDBC probe, requires the following parameters:

-   JDBC driver class name
-   JDBC connection string
    -   Database server
    -   Database name
    -   User name
    -   User password
-   The table name

**Parent Topic:**[JDBCProbe](../task/t_JDBCProbe.md)

**Related topics**  


[JDBCProbe](../task/t_JDBCProbe.md)

