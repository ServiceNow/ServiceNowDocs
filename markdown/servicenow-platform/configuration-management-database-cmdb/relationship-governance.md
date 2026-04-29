---
title: Relationship governance rules
description: Relationship governance rules is a set of relationship rules used to ensure consistency and validity in modeling relationships between configuration items \(CIs\) in the CMDB. Use relationship governance rules to prevent the selection of relationship types or directions that are not allowed between specific CI types.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CI relationships in the CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Relationship governance rules

Relationship governance rules is a set of relationship rules used to ensure consistency and validity in modeling relationships between configuration items \(CIs\) in the CMDB. Use relationship governance rules to prevent the selection of relationship types or directions that are not allowed between specific CI types.

Different applications such as Discovery and Service Mapping create relationships between CIs. Each application might use inconsistent relationship type or direction to represent the same entity, resulting in multiple views of the same CIs. Relationship governance rules define what are valid relationship types and valid directions between pairs of CI types resulting in valid and consistent relationships in the CMDB.

Relationship governance rules consist of:

-   [CMDB dependent relationship rules](c_ServiceRulesMetadata.md): Rules \(hosting and containment rules\) that are used for CI identification. You can view and modify dependent relationship rules in the CI Class Manager, after selecting a class from the class hierarchy and clicking **Dependent Relationship**.
-   [Suggested relationships](../reference/r_SuggestedRelationshipModel.md): Rules that are based on existing suggested relationships in the Suggested Relationship \[cmdb\_rel\_type\_suggest\] table. Suggested relationships are used in the [CI relationship editor](c_RelationshipEditor.md). You can view and modify suggested relationships in the CI Class Manager, after selecting a class from the class hierarchy and clicking **Suggested Relationships**.
-   [Reference rules](c_ServiceRulesMetadata.md): Rules that are used mostly by Cloud Management to represent all the possible valid combinations of pairs of referencing and referenced CIs in the service definition.
-   Built-in valid relationships: The following relationships are pre-defined in the base system as valid relationships:
    -   cmdb\_ci\_endpoint -&gt; Applicative Flow To::Applicative Flow From -&gt; cmdb\_ci\_endpoint
    -   cmdb\_ci\_endpoint -&gt; Implement End Point To::Implement End Point From -&gt; cmdb\_ci
    -   cmdb\_ci -&gt; Use End Point To::Use End Point From -&gt; cmdb\_ci\_endpoint

## General behavior

-   Relationship governance rules support inheritance.

    For example, suppose that the suggested relationship cmdb\_ci\_appl Runs On::Runs cmdb\_ci\_hardware exists. Then a Runs On::Runs relationship between a cmdb\_ci\_appl\_dot\_net CI and a cmdb\_ci\_windows\_server CI is valid. That is because .Net Application class inherits from the Application class and the Windows Server class inherits from the Hardware class.

-   Duplicate relationship governance rules are not allowed.
-   Relationship governance rules are not domain separated.
-   It is allowed to have more than one relationship type between the same two CI types.

    For example, the following relationships are valid:

    -   cmdb\_ci\_appl Depends On::Used by cmdb\_ci\_service
    -   cmdb\_ci\_appl Receives data from::Sends data to cmdb\_ci\_service

## Reports

A relationship between CIs is considered valid if it conforms to any of the relationship governance rules. Use the Relationship Health Dashboard to view reports about [relationships health](../task/t_ViewRelationshipsHealth.md) including relationships compliance with relationship governance rules. The 'Relationships not compliant with all relationship rules' report shows CI relationships that are not compliant with any of the relationship governance rules.

**Parent Topic:**[CI relationships in the CMDB](c_CIRelationships.md)

**Related topics**  


[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)

[Add a suggested relationship](../task/t_AddANewSuggestedRelationship.md)

[CI relations formatter](c_CIRelationsFormatterNG.md)

[CI relationship editor](c_RelationshipEditor.md)

[Relation qualifier](c_RelationQualifier.md)

[CI relationship security](c_CIRelationshipSecurity.md)

[Create a CI relation rollup](../task/t_CreateACIRelationRollup.md)

