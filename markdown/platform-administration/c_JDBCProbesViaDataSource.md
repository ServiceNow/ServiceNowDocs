---
title: JDBC Probes via Data Source
description: JDBC probes are executed via a JDBC data source when an import is running against the data source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/c\_JDBCProbesViaDataSource.html
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [JDBCProbe, Supported integration interfaces, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# JDBC Probes via Data Source

JDBC probes are executed via a JDBC data source when an import is running against the data source.

A JDBC data source JDBC probe is described by the JDBCProbe Topic and the `sys_id` of the data source in the Source field of the ECC Queue output record.

The data source record would look like this

\[Omitted image "JdbcDataSource.png"\] Alt text:

The following ECC Queue output probe will be created when you *load* from the data source.

\[Omitted image "JdbcDataSourceProbe.png"\] Alt text:

**Parent Topic:**[JDBCProbe](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/t_JDBCProbe.md)

**Related topics**  


[JDBCProbe](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/t_JDBCProbe.md)

