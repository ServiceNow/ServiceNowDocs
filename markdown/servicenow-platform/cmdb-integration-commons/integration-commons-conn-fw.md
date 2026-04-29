---
title: Accessing the connection details of Service Graph Connectors
description: The common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app enables you to access connection details for Service Graph Connectors.
locale: en-US
release: australia
product: CMDB Integration Commons
classification: cmdb-integration-commons
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integration Commons for CMDB, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Accessing the connection details of Service Graph Connectors

The common connection framework \(CCF\) included within the Integration Commons for CMDB \(sn\_cmdb\_int\_util\) store app enables you to access connection details for Service Graph Connectors.

With the CCF feature, you can access all connections for a connector. Connection details include the alias, properties, data sources, and associated scheduled data imports. In addition, you can test a connection. Additional details may appear depending on the connector type. For more information, see [Accessing the connection details of Service Graph Connectors](integration-commons-conn-fw.md).

## Viewing connections

To view the connection details for all Service Graph Connectors that use the CCF, navigate to **All** &gt; **Service Graph Connectors** &gt; **Connections** from the application navigator.

If a Service Graph Connector uses CCF, you can also view the connections specific to the connector. To view the connection details, open the Service Graph Connector from the application navigator, access its Connections module to view the Service Graph Connections list, and then select the connection name.

The Service Graph Connections page displaying the connection details also includes the **Test Connection** related link that you can select to test the connection. If the connection is successful, a success message is displayed. Else, an error message with the reason of failure is displayed.

## CCF tables

The CCF uses the following tables:

-   **Service Graph Connections \[sn\_cmdb\_int\_util\_service\_graph\_connection\]**

    Stores the connection records for all the Service Graph Connectors that use the CCF. The Service Graph Connections \[sn\_cmdb\_int\_util\_service\_graph\_connection\] table also includes other CCF tables as related lists.

-   **Properties \[sn\_cmdb\_int\_util\_service\_graph\_connection\_property\]**

    Stores the connection properties associated with a specific connection.

-   **Service Graph Connection Data Sources \[sn\_cmdb\_int\_util\_service\_graph\_connection\_data\_source\]**

    Stores the many-to-many \(m2m\) connection details between the Service Graph Connections \[sn\_cmdb\_int\_util\_service\_graph\_connection\] table and the data sources for a Service Graph Connector.

-   **Service Graph Connection Scheduled Data Imports \[sn\_cmdb\_int\_util\_service\_graph\_connection\_scheduled\_data\_import\]**

    Stores the m2m connection details between the Service Graph Connections \[sn\_cmdb\_int\_util\_service\_graph\_connection\] table and the scheduled data imports for a Service Graph Connector.

-   **Service Graph Connection Test Script \[sn\_cmdb\_int\_util\_service\_graph\_connection\_test\_script\]**

    Stores records that include scripts for triggering the test connection process for Service Graph Connectors.


