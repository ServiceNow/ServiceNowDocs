---
title: Select \* JDBC Probe short cut
description: Alternatively, you may specify a table\_name parameter instead of a work element and the following query could be executed.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [JDBCProbe, Supported integration interfaces, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Select \* JDBC Probe short cut

Alternatively, you may specify a **table\_name** parameter instead of a work element and the following query could be executed.

```
select * from <table_name>
```

For example, using the following XML payload

```
<?xml version= "1.0" encoding= "UTF-8" ?><parameters><parameter name = "jdbc_driver" value = "com.microsoft.sqlserver.jdbc.SQLServerDriver" /><parameter name = "connection_string" value = "jdbc:sqlserver://xxx.service-now.com;databaseName=SMS_CRICKET;user=sms;password=sms" /><parameter name = "table_name" value = "System_DATA" /></parameters>
```

## Counting Rows

To count the number of rows in a table, you can indicate a select count\(\*\) type query by including the count\_rows parameter with a value of true.

For example

```
<?xml version= "1.0" encoding= "UTF-8" ?><parameters><parameter name = "jdbc_driver" value = "com.microsoft.sqlserver.jdbc.SQLServerDriver" /><parameter name = "connection_string" value = "jdbc:sqlserver://xxx.service-now.com;databaseName=SMS;user=sms;password=sms" /><parameter name = "count_rows" value = "true" /><parameter name = "table_name" value = "System_DATA" /></parameters>
```

The resulting response XML payload

```
<parameters>
  ...
  <result query = "SELECT count(*) as row_count FROM System_DATA" ><row id = "1" ><row_count class = "java.lang.Integer" length = "11" type = "4" >2312</row_count></row></result>
  ...
</parameters>
```

**Parent Topic:**[JDBCProbe](../task/t_JDBCProbe.md)

**Related topics**  


[JDBCProbe](../task/t_JDBCProbe.md)

