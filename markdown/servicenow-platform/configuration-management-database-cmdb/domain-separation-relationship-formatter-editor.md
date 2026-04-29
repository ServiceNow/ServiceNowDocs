---
title: Domain separation
description: Domain separation is supported in the relations formatter and the CI relationship editor. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CI relations formatter, CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Domain separation

Domain separation is supported in the relations formatter and the CI relationship editor. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## How domain separation works in the relations formatter and relationship editor

-   **Relations formatter**

    The relations formatter is domain-separation supported. The relations formatter is used to display CMDB relationships in the UI in different views. Since the CI Relationship \(cmdb\_rel\_ci\) table is not domain separated, relationships are visible in the relations formatter only if both parent and child CIs \(cmdb\) are visible in the domain.

    The CI Relationship Type \(cmdb\_rel\_type\) table is not domain separated. Therefore, in the relations formatter, all the relationship types are available to be selected as a filter.

    By default domain separation is supported in the relations formatter.

-   **Relationship editor**

    The relationship editor is domain-separation supported. You can use the relationship editor to add new relationships or delete existing relationships for the current CI.

    -   The CI relationship editor displays a list of CIs to add or remove from relationships. Since they are domain separated, the CI list view in the relationship editor displays the CIs that are visible to the current domain.
    -   The CI relationship editor displays a list of relationships to add or remove. Since the CI Relationship \[cmdb\_rel\_ci\] table is not domain separated, the relationships list view displays all the relationships of the current CI.

The Suggested Relationship \(cmdb\_rel\_type\_suggest\) table is not domain separated, which means that all the suggested relationship types in the relationship editor are visible for all domains.

By default domain separation is supported in the relationship editor.

**Parent Topic:**[CI relations formatter](c_CIRelationsFormatterNG.md)

**Related topics**  


[Domain separation and Configuration Management Database \(CMDB\)](domain-separation-cmdb.md)

