---
title: Accessing the connection details of Service Graph Connector for OpenTelemetry
description: You can access the connection details of the Service Graph Connector for OpenTelemetry in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.Access the details of an OpenTelemetry connection configured for the Service Graph Connector for OpenTelemetry.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2026-02-27"
reading_time_minutes: 1
keywords: [SGC-OpenTelemetry, SGC OpenTelemetry, SGC for OpenTelemetry, OpenTelemetry SGC, Service Graph Connector for OpenTelemetry, OpenTelemetry connection details, OpenTelemetry connection, common connection framework, CCF, SGC-OpenTelemetry, SGC OpenTelemetry, SGC for OpenTelemetry, OpenTelemetry SGC, Service Graph Connector for OpenTelemetry, OpenTelemetry connection details, OpenTelemetry connection, common connection framework, CCF]
breadcrumb: [OpenTelemetry, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Accessing the connection details of Service Graph Connector for OpenTelemetry

You can access the connection details of the Service Graph Connector for OpenTelemetry in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.

**Important:** Starting with the Australia release, Service Graph Connector for OpenTelemetry is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

With the CCF, you can access all the connections used by the Service Graph Connector for OpenTelemetry. The connection details include the connection alias, connection properties, data sources, and scheduled data imports associated with a connection. You can also test the connection.

## Access the details of an OpenTelemetry connection

Access the details of an OpenTelemetry connection configured for the Service Graph Connector for OpenTelemetry.

### Before you begin

**Important:** Starting with the Australia release, Service Graph Connector for OpenTelemetry is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **OpenTelemetry** &gt; **Connections**.

2.  From the **Name** column of the Service Graph Connections list, select a connection.

3.  On the Service Graph Connections page, view the connection details such as the connection name, alias, and data sources.

4.  Select a related list to view further details of the connection.

5.  Select the **Test Connection** related link to test the connection.


**Related topics**  


[Service Graph Connector for OpenTelemetry properties](../reference/sgc-cmdb-otel-props.md)

[Accessing the connection details of Service Graph Connectors](integration-commons-conn-fw.md)

