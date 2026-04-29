---
title: Suggested class relationships
description: The system keeps a table \(Suggested Relationship \[cmdb\_rel\_type\_suggest\]\) of relationship types that are appropriate for a CI type, based on its class. You can manage suggested relationships by navigating to Configuration Suggested Relationships , or in the CI Class Manager.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Suggested class relationships

The system keeps a table \(Suggested Relationship \[cmdb\_rel\_type\_suggest\]\) of relationship types that are appropriate for a CI type, based on its class. You can manage suggested relationships by navigating to **Configuration** &gt; **Suggested Relationships**, or in the CI Class Manager.

## Suggestion model

The relationship editor has a base CI. The base CI designates the CI that a user was on before launching the editor, as the base CI in the new relationship. If you launched the relationship editor from the lnux100 CI, then lnux100 becomes the base CI. Also, every CI in the system has a type \(class\). For example, bond lnux100 is of the Linux server type.

Many CI types are children of other types in the hierarchy. For example, the class hierarchy for a Linux server is:

`cmdb_ci` -&gt; `cmdb_ci_hardware` -&gt;`cmdb_ci_computer` -&gt; `cmdb_ci_server` -&gt; `cmdb_ci_linux_server`

The suggestion model works by analyzing the suggested relationship table for all relationships whose base class is the current base class or any one of its parent classes. For example, looking at a Linux server, the suggestion model would retrieve any relationships whose base class was:

`cmdb_ci_linux_server`, `cmdb_ci_server`, `cmdb_ci_computer`, `cmdb_ci_hardware`, or `cmdb_ci`

ITOM Visibility, if available, uses enhanced discovery patterns to identify and add CI relationships to the Suggested Relationships table.

## Suggested CI relationships in the relationship editor

The CI relationship editor uses the suggestion model to help users select reasonable relationships for configuration items.

For example, consider these relationship types in the system:

-   Provides Power for :: Receives Power From
-   Runs on :: Hosts

Typically, a user uses these relationships to define the following reasonable relationships between two items as follows:

-   a database runs on a server
-   a rack provides power for a server

Typically, neither of the following definitions would be appropriate:

-   a rack runs on a server
-   a server runs on a database

For descriptions of some key relationships, see [CI relationships in the CMDB](../concept/c_CIRelationships.md).

**Parent Topic:**[CI relationships in the CMDB](../concept/c_CIRelationships.md)

**Related topics**  


[Add a suggested relationship](../task/t_AddANewSuggestedRelationship.md)

[Relationship governance rules](../concept/relationship-governance.md)

[CI relations formatter](../concept/c_CIRelationsFormatterNG.md)

[CI relationship editor](../concept/c_RelationshipEditor.md)

[Relation qualifier](../concept/c_RelationQualifier.md)

[CI relationship security](../concept/c_CIRelationshipSecurity.md)

[Create a CI relation rollup](../task/t_CreateACIRelationRollup.md)

[CI Class Manager](../task/t_AddANewSuggestedRelationship.md)

