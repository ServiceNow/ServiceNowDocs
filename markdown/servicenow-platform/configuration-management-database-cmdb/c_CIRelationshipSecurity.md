---
title: CI relationship security
description: When applying security to CI relationships, it is important to apply the access controls both to the CI Relationship \(cmdb\_rel\_ci\) table and to create an operation editCIRelations to the \* table as well.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/c\_CIRelationshipSecurity.html
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

**Parent Topic:**[CI relationships in the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_CIRelationships.md)

**Related topics**  


[Suggested class relationships]()

[Add a suggested relationship]()

[Relationship governance rules]()

[CI relations formatter]()

[CI relationship editor]()

[Relation qualifier]()

[Create a CI relation rollup]()

[CI relationships in the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_CIRelationships.md)

[Create a CI relation rollup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/t_CreateACIRelationRollup.md)

