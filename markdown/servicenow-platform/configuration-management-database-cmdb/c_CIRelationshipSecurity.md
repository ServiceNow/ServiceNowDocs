---
title: CI relationship security
description: When applying security to CI relationships, it is important to apply the access controls both to the CI Relationship \(cmdb\_rel\_ci\) table and to create an operation editCIRelations to the \* table as well.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI relationship security

When applying security to CI relationships, it is important to apply the access controls both to the CI Relationship \(cmdb\_rel\_ci\) table and to create an operation editCIRelations to the \* table as well.

If the current instance has defined security for editCIRelations, it will be applied to edit\_ci\_relations automatically in the process of upgrading, and the out-of-date security will be removed.

**Parent Topic:**[CI relationships in the CMDB](c_CIRelationships.md)

**Related topics**  


[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[Add a suggested relationship](../task/t_AddANewSuggestedRelationship.md)

[Relationship governance rules](relationship-governance.md)

[CI relations formatter](c_CIRelationsFormatterNG.md)

[CI relationship editor](c_RelationshipEditor.md)

[Relation qualifier](c_RelationQualifier.md)

[Create a CI relation rollup](../task/t_CreateACIRelationRollup.md)

[CI relationships in the CMDB](c_CIRelationships.md)

[Create a CI relation rollup](../task/t_CreateACIRelationRollup.md)

