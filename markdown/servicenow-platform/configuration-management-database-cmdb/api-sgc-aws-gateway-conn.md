---
title: Accessing the connection details of API Service Graph Connector for AWS API Gateway
description: You can access the connection details of the API Service Graph Connector for AWS API Gateway in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.Access the details of an AWS API Gateway connection configured for the API Service Graph Connector for AWS API Gateway.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AWS API Gateway, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Accessing the connection details of API Service Graph Connector for AWS API Gateway

You can access the connection details of the API Service Graph Connector for AWS API Gateway in a single view using the common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app.

With the CCF feature, you can access all connections for a connector. Connection details include the alias, properties, data sources, and associated scheduled data imports. In addition, you can test a connection. Additional details may appear depending on the connector type. For more information, see [Accessing the connection details of Service Graph Connectors](integration-commons-conn-fw.md).

## Access the details of an AWS API Gateway connection

Access the details of an AWS API Gateway connection configured for the API Service Graph Connector for AWS API Gateway.

### Before you begin

Role required: sn\_cmdb\_int\_util.sgc\_admin oradmin

### Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **AWS API Gateway** &gt; **Connections**.

2.  From the **Name** column of the Service Graph Connections list, select a connection.

3.  On the Service Graph Connections page, view the connection details such as the connection name and alias.

4.  Select a related list to view further details of the connection.

5.  Select the **Test Connection** related link to test the connection.


