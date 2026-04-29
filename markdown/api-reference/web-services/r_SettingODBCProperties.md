---
title: Setting ODBC properties
description: The following properties customize connectivity and optimize the query behavior of the ODBC driver.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring the ODBC driver, Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Setting ODBC properties

The following properties customize connectivity and optimize the query behavior of the ODBC driver.

## ODBC administrator properties

These properties are specified in the ODBC Data Source Administrator for the DSN or in the **Custom Properties** field of the login dialog box.

<table id="table_vxg_tmt_jp"><thead><tr><th>

Property Name

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

BatchSize

</td><td>

During fetching of results from the instance, this batch size configures the number of records to fetch for every request. Typically, the default is an optimal number for normal sized rows. If an error occurs during fetching of records that indicates this value should be lowered, you can modify it to optimize memory usage versus performance.

</td><td>

2000

</td></tr><tr><td>

url

</td><td>

This is the ServiceNow instance URL or endpoint. It should indicate the URL to the ServiceNow instance you want to connect to.

</td><td>

https://demo.service-now.com

</td></tr><tr><td>

EnablePassThrough

</td><td>

During processing of aggregate functions, enabling pass through mode allows directly calling Aggregate Web Service for optimized and speedy response. Whenever possible, this mode should be left enabled.

</td><td>

true

</td></tr><tr><td>

debug

</td><td>

By default, debugging messages are not produced. Set **debug** to **true** when you operate the ODBC driver from the ISQL console window to write all HTTP-related network communication traffic to the console window. When using this option, set **gzip** to **false** so that data is not compressed. Otherwise, the data is unreadable.

</td><td>

false

</td></tr><tr><td>

gzip

</td><td>

By default, data sent over the network is compressed. Set **gzip** to **false** when using the **debug** parameter to write network communication to the ISQL console so that data is not compressed.

</td><td>

true

</td></tr><tr><td>

timeout

</td><td>

Specifies the socket inactivity timeout value in seconds.

</td><td>

175

</td></tr><tr><td>

retries

</td><td>

Number of times to retry the failing request in the event of a socket timeout error.

</td><td>

0

</td></tr><tr><td>

mode

</td><td>

The query mode used to parse complex where clauses. You can configure the ODBC driver query mode to use either AND or OR operators.While the OR operator provides the greatest compatibility with complex queries, the AND operator is usually more efficient and results in fewer database operations.

</td><td>

or

</td></tr><tr><td>

EnableDBSchema

</td><td>

The ODBC driver issues a database schema request to retrieve table names from the instance. This functionality is enabled by default so reporting applications such as Microsoft Excel can display a list of tables to query from. Disabling this property may improve the performance of the first query sent from a reporting application, especially if the instance has a large number of tables.

</td><td>

true

</td></tr><tr><td>

ExtendedSchemaCache

</td><td>

The ODBC driver caches the database schema for each connection. When a new connection is created, the driver clears the database cache and queries the database schema from the instance again. This behavior is beneficial when connecting to different data source, or when modifying the table schema. When querying a single data source with a consistent schema, enable this property to avoid sending unnecessary schema requests, including when **EnableDBSchema** is **true**.

</td><td>

false

</td></tr><tr><td>

LegacyDurationTimeZone

</td><td>

The ODBC driver returns timer and duration field values in the UTC timezone by default, starting with the 1.0.10 version. When this property is **true**, the ODBC driver returns timer and duration field values using the display value, as shown in the UI. This property can be used to preserve compatibility with legacy integrations that depend on the display value. See [KB0583982](https://support.servicenow.com/kb_view.do?sysparm_article=KB0583982) for details about this behavior.

</td><td>

false

</td></tr></tbody>
</table>If you need to use more than one of these properties in your connection, concatenate the settings with a semicolon \(;\) delimiter. For example, the following string sets the URL to a specific instance and changes the batch size to 200 records.

`url=https://demo1234.service-now.com;BatchSize=200`

## ODBC management console properties

You can access these properties from the ODBC Management Console available in the Windows Start menu at **ServiceNow ODBC** &gt; **Management Console**.

<table id="table_mdz_znt_jp"><thead><tr><th>

Property name

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

ServiceJVMOptions\(Services\\Service Settings\\IP Parameters\)

</td><td>

JVM command line properties and option. For example, to change the maximum Java heap size, modify the -Xmx150m parameter.

</td><td>

-Xms64m -Xmx150m

</td></tr><tr><td>

DataSourceIPProperties\(OpenAccess SDK 6.0 Manager\\&lt;installation location&gt;\\Services\\ServiceNow\_ODBC\\Data Source Settings\\ServiceNow\\IP Parameters\)

</td><td>

Global default of the instance URL for all ODBC connections. For more flexibility, you may also create new DSNs with default URL configurations.

</td><td>

https://demo.service-now.com

</td></tr><tr><td>

ServiceSQLDiskCacheMaxSize\(Services\\Service Settings\\SQL Engine Parameters\)

</td><td>

Specifies the maximum size of the disk cache files. Increase this value when you see `Disk Cache file size limit has reached` errors.

</td><td>

200

</td></tr><tr><td>

Timeout\(Data Source Settings\\ServiceNow\\IP Parameters\)

</td><td>

Specifies the socket inactivity timeout value in seconds. Increase this to a value greater than glide.soap.request\_processing\_timeout.odbc when you see `GetKeys failed (Socket timeout)` errors.

</td><td>

175

</td></tr><tr><td>

ServiceJVMLocation

</td><td>

Contains the JRE location used by the ODBC driver.

</td><td>

There is no default value for this property. You are prompted to enter the JRE location at the time of installation.

</td></tr></tbody>
</table>## Service JVM options

You can specify these values within the ServiceJVMOptions parameter in addition to standard JVM arguments such as -Xmx.

|Option|Description|Default|
|------|-----------|-------|
|-DLOG\_FILE\_NAME|The location of the ODBC log file. This property is available starting with the ODBC driver 1.0.7.1 release.|$\{user.home\}\\AppData\\Local\\ServiceNow\\odbc\\logging\\odbc.log|
|-DLOG\_LEVEL|The logging level used when writing to the ODBC log file. You can specify the logging level using Logback levels, such as TRACE, INFO, or ERROR. This property is available starting with the ODBC driver 1.0.8 release.|INFO|

## Instance properties

An administrator can configure these properties by adding a property or modifying an existing one in the ServiceNow instance.

|Property name|Description|Default|
|-------------|-----------|-------|
|glide.db.max.aggregates|The maximum number of rows returned by aggregate functions.|100000|
|glide.db.max\_view\_records|The maximum number of rows returned by a database view.|10001|

**Parent Topic:**[Configuring the ODBC driver](../concept/configuring-odbc.md)

