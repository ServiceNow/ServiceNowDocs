---
title: Using the Work Element
description: The work element encodes SQL statements to be executed by the probe.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [JDBCProbe, Supported integration interfaces, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer]
---

# Using the Work Element

The work element encodes SQL statements to be executed by the probe.

**Note:** This API can only be used by the following:

-   Development users who have the rights to edit scripts to insert records to the ecc\_queue.
-   Admin users to insert records through the UI.

There’s no backend sanitization of any SQL statements, table names, or column names. It's the development users’ responsibility to sanitize them if non-trusted users can manipulate them to execute malicious queries.

The following are the valid work child elements.

-   select
-   update
-   insert
-   delete

## SELECT

Retrieve rows from the specified table in the database specified by the JDBC connection string. The simplest select work just specifies the table name and will retrieve all fields in a row, for example:

```
 ...
  <parameter name= "work" ><select table = "System_DATA" /></parameter>
  ...
```

To specify a search criteria, specify the where attribute on the select element, for example:

```
 ...
  <parameter name= "work" ><select table = "System_DATA" where = "InstanceKey=692" /></parameter>
  ...
```

To specify the fields you want returned, embed the fields as child elements of the select element, for example:

```
  ...
  <parameter name= "work" ><select table = "System_DATA" where = "InstanceKey=692" ><MachineID /><SMSID0 /></select></parameter>
  ...
```

To use a direct SQL statement, specify it in the **query** parameter

```
 ...
  <parameter name= "query" value= "Specific SQL" /><parameter name = "sql_statement" value = "select * from any_table where value='test'" />
  ...
```

## UPDATE

An **update** SQL can be executed by specifying the **table**, optional where clause and required child elements for the fields and their values to update.

```
...
<parameter name= "work" ><update table = "alerts.status" where = "ServerName %= 'NCOMS' AND ServerSerial=3935" ><Agent>ServiceNow - INC10020</Agent><URL>http://Macintosh-9.local:8080/glide/incident.do?sys_id=17a31f380a0a0bae0048ca875c8891d0</URL><Severity quoted = "false" >3</Severity><Acknowledged quoted = "false" >0</Acknowledged></update></parameter>
...
```

## INSERT

An **insert** SQL can be executed by specifying the **table**, and required child elements for the fields and their values to insert.

```
...
<parameter name= "work" ><insert table = "alerts.status" ><Agent>ServiceNow - INC10020</Agent><URL>http://Macintosh-9.local:8080/glide/incident.do?sys_id=17a31f380a0a0bae0048ca875c8891d0</URL><Severity quoted = "false" >3</Severity><Acknowledged quoted = "false" >0</Acknowledged></insert></parameter>
...
```

## DELETE

A delete SQL can be executed by specifying the table and optional where clause.

```
...
<parameter name= "work" ><delete table = "alerts.status" where = "ServerName %= 'NCOMS' AND ServerSerial=3935" /></parameter>
...
```

**Parent Topic:**[JDBCProbe](../task/t_JDBCProbe.md)

**Related topics**  


[JDBCProbe](../task/t_JDBCProbe.md)

