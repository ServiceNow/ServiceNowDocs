---
title: Established connections
description: Access data from external sources directly in the ServiceNow AI Platform, without copying any data to your instance using zero copy connections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/connections-zcc.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, Zero Copy Connectors, Workflow Data Fabric]
---

# Established connections

Access data from external sources directly in the ServiceNow AI Platform, without copying any data to your instance using zero copy connections.

## Key benefits

-   Access external data without the complexity and maintenance involved with extract, transform, and load \(ETL\) processes.
-   Minimize security risks associated with copying and storing data in multiple locations.
-   Maintain data accuracy by avoiding errors associated with data replication.
-   View external data assets and create data fabric tables with mapped data.

Zero copy connections enable access to external data locally, while reducing storage consumption and minimizing security risks typically associated with duplicating data across multiple systems.

In the Zero Copy Connector Hub, a connection admin can navigate to the **Available connectors** tab to view primary and community connectors and create a zero copy connection. After the connection is established, the connection admin can grant access to a data steward. The data steward can then access the zero copy connection from the **Established connections** tab to create a data fabric table.

\[Omitted image "zcc-zc-connections.png"\] Alt text: Established connections in Zero Copy Connector Hub.

## Required ServiceNow AI Platform roles

The df\_connection\_admin role is required to create and manage zero copy connections.

A role containing the df\_data\_steward role is required to access established connections and create data fabric tables.

## Accessing established connections

View established connections by navigating to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Established connections** or **All** &gt; **Zero Copy Connector Hub** &gt; **Established connections**.

**Related topics**  


[Monitoring established connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/monitoring-connection-status-zcc.md)

[Data steward access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/steward-access-zcc.md)

[Use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/use-cases-zcc.md)

