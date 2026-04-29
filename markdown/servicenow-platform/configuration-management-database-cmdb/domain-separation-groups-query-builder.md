---
title: Domain separation and CMDB Query Builder
description: Domain separation is supported in the CMDB Query Builder. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and CMDB Query Builder

Domain separation is supported in the CMDB Query Builder. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## How domain separation works in the CMDB Query Builder

With the CMDB Query Builder you can easily build complex infrastructure and service queries that span multiple CMDB classes, and that involve many CIs that are connected by different relationships. Domain separation is set to be on by default.

-   **Saved Query**

    The user creates a query by dragging a class node from the class hierarchy and dropping it to the canvas and connecting the nodes with the relationships type.

    The user can save the created query as an XML file to the database \[qb\_saved\_query\] table in the CMDB for future use. The saved query is domain separated.

-   **Query results**

    With a saved query, the user selects **Run** and the query result is saved and displays in the platform list view.

    In the query results, domain separation behaves in the same way as the platform list view for the CI relationship \[cmdb\_rel\_ci\] table and CMDB CI \[cmdb\] table. Consequently, since the CI relationship is not domain separated, all relationships of the query result display, regardless of the domains. Conversely, if the query result is CI only, since the CMDB CI is domain separated, the results display only if visible in the current domain.


**Related topics**  


[Domain separation and Configuration Management Database \(CMDB\)](domain-separation-cmdb.md)

