---
title: Data fabric tables
description: Fuel your AI agents and enrich workflows on the ServiceNow AI Platform with external data using data fabric tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/data-fabric-tables-zcc.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Zero Copy Connectors, Workflow Data Fabric]
---

# Data fabric tables

Fuel your AI agents and enrich workflows on the ServiceNow AI Platform with external data using data fabric tables.

## Key benefits

-   Fetch external data in real time and view the data in lists and forms as if it's stored in your instance.
-   Reduce storage consumption and performance load in your instance.
-   Control access to external data so that only authorized users can view the data.

A data fabric table is a virtual representation of data stored in an external source, accessible directly from the ServiceNow AI Platform. The data fabric table definition is stored in the ServiceNow AI Platform, but its external records live in the memory in read-only mode. You can view external records from a data fabric table in lists and forms the same way you view records in a physical table.

Access to a data fabric table is controlled the same way access is controlled to a physical table. Data fabric tables belong to the application scope selected by the data steward during their creation.

\[Omitted image "zcc-data-fabric-table.png"\] Alt text: A list of your data fabric tables.

## Required ServiceNow AI Platform roles

A role containing the df\_data\_steward role or the df\_connection\_admin role is required to create and manage data fabric tables.

## Accessing data fabric tables

View and manage data fabric tables on the **Data fabric tables** tab by navigating to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Data fabric tables** or **All** &gt; **Zero Copy Connector Hub** &gt; **Data fabric tables**.

## Managing data fabric tables

For information on viewing and managing data fabric tables, see [Managing data fabric tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/managing-data-fabric-tables-zcc.md).

## Related information

For use cases, see [Use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/use-cases-zcc.md).

For a comparison of data fabric tables and remote tables, see [Differences between data fabric tables and remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/dft-vs-remote-tables.md).

