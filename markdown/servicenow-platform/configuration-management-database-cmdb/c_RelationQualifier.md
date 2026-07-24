---
title: Relation qualifier
description: A relation qualifier, which is a CI of the Qualifier \[cmdb\_ci\_qualifier\] type, stores important information about the CI relationships.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/configuration-management-database-cmdb/c\_RelationQualifier.html
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Relation qualifier

A relation qualifier, which is a CI of the Qualifier \[cmdb\_ci\_qualifier\] type, stores important information about the CI relationships.

In a relation qualifier, you can annotate arbitrary unique information about the relationship between two CIs. You can define multiple qualifiers for a single relationship, resulting in a qualifier chain. But, there can be only a single qualifier chain for a specific relationship type between two CIs.

For example, for a relationship between a parent CI and a child CI, you can add a relation qualifier to note that the relationship was discovered based on traffic \(such as **cmdb\_ci\_qualifier\_traffic\_based\_connection**\). This results in having two records in the CI Relationship \[cmdb\_rel\_ci\] table for the relationship.

-   A record that links the parent CI and the new qualifier
-   A record that links the new qualifier and the child CI

For this relationship, there is a parent CI and a child CI, and a relation qualifier of type **cmdb\_ci\_qualifier\_trafficbased**.

For information about usage of relation qualifiers in the identification process, see [Identification rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_IdentificationRules.md).

**Parent Topic:**[CI relationships in the CMDB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_CIRelationships.md)

**Related topics**  


[Suggested class relationships]()

[Add a suggested relationship]()

[Relationship governance rules]()

[CI relations formatter]()

[CI relationship editor]()

[CI relationship security]()

[Create a CI relation rollup]()

