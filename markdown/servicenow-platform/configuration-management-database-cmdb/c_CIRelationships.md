---
title: CI relationships in the CMDB
description: The CMDB, in contrast to a static asset list, helps you track not only the configuration items \(CIs\) within your system, but also the relationships between those items.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CI relationships in the CMDB

The CMDB, in contrast to a static asset list, helps you track not only the configuration items \(CIs\) within your system, but also the relationships between those items.

A relationship in the CMDB consists of two CIs and a relationship type:

-   Parent CI
-   Child CI
-   Type of the relationship that links both CIs

For example, in the \[Server1\] \[Managed by\] \[Server2\] relationship:

-   Server1 is the child CI
-   Server2 is the parent CI
-   \[Managed by\] is the relationship type

For example, a web application might read data from an instance of Oracle, which in turn might depend on a piece of underlying hardware. Most CIs in a CMDB have multiple relationships to other CIs, users, and groups.

The relationships between CIs can be automatically discovered. If you use Discovery, many relationships can be automatically loaded into the system through the discovery process. If you import your data from another system, you get some form of relationships.

You can add to automatically discovered relationships, create relationships, or edit relationships for a CI by launching the [CI relationship editor](c_RelationshipEditor.md) from the CI form. As an alternative to the CI relationship editor, [Unified Map](cmdb-workspace-unified-map.md) in the [CMDB Workspace store app](cmdb-workspace.md) provides the latest functionality for editing CI relationships. For more information, see [Edit relationships in Unified Map](../task/unified-map-edit-connection.md).

## Dependent and non-dependent relationships

[Dependent relationships](c_ServiceRulesMetadata.md), such as tomcat RunsOn Hardware, are used by the Identification and Reconciliation Engine \(IRE\) to identify dependent CIs. The IRE avoids duplicate entries of CIs into your Configuration Management Database \(CMDB\) by leveraging these relationships to determine if a recently discovered CI is already in the CMDB.

For non-dependent relationships, the CMDB tracks the discovery source and the last scanned time in the Relationship Sources \[sys\_rel\_source\] table. Non-dependent relationships aren't used for CI identification, and can be deleted when no longer needed.

To avoid burdening your IRE with excessive load, by default, the Relationship Sources \[sys\_rel\_source\] table doesn't auto-populate. If you want to track full information on non-dependent relationships, you can change the default using the glide.identification\_engine.populate\_sys\_rel\_source property.

[Dependent relationships](c_ServiceRulesMetadata.md) are used for CI identification, so they shouldn't be directly deleted as they aren't tracked.

Information in the Relationship Sources \[sys\_rel\_source\] table can be used to decide if it’s safe to delete a potentially non-dependent relationship. For example, a discovery source, which is attempting to delete a non-dependent relationship can confirm that:

-   There are no other data sources for that relationship.
-   The relationship wasn't updated for some specified length of time and therefore is no longer needed.

When a non-dependent relationship is deleted from the CI Relationship \[cmdb\_rel\_ci\] table, all cascading corresponding records in the Relationship Sources \[sys\_rel\_source\] table are deleted.

## Key relationships

The following table contains descriptions for some key CMDB relationships.

<table id="table_tq1_nsr_rsb"><thead><tr><th>

Parent

</th><th>

Child

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Applicative Flow To

</td><td>

Applicative Flow From

</td><td>

Connections between endpoint CIs.

 **Note:** For internal use only \(service model\).

</td></tr><tr><td>

Connects to

</td><td>

Connected by

</td><td>

Network Connections between elements that are talking to each other.

 Examples: Workstation to switch, switch to switch, kubernetes workload to service.

</td></tr><tr><td>

Contains

</td><td>

Contained by

</td><td>

Typically a containment relationship \(CI to contained CI\). The child CI typically has a single parent CI with this relationship type.

 Examples: Tomcat to Tomcat WAR, VMware Datacenter contains Network.

</td></tr><tr><td>

Defines resources for

</td><td>

Gets resources from

</td><td>

Parent CI defines/gets resources from a child CI.

 Example: VMware - Resource pool gets resources from ESX Server.

</td></tr><tr><td>

Depends on

</td><td>

Used by

</td><td>

Parent CI depends on child CI. Meaning that problem/change in the child CI may impact the parent CI.

</td></tr><tr><td>

Hosted on

</td><td>

Hosts

</td><td>

Hosting relationship between an element and its host.

 Examples: Cloud resource to logical data center, k8s workload to k8s cluster.

</td></tr><tr><td>

Implement End Point To

</td><td>

Implement End Point From

</td><td>

Endpoint to CI that exposes this endpoint.

 **Note:** For internal use only \(service model\).

</td></tr><tr><td>

Manages

</td><td>

Managed by

</td><td>

Typically used where one CI manages one or more other CIs.

 Example: vCenter manages vCenter Datacenter.

</td></tr><tr><td>

Members

</td><td>

Member of

</td><td>

Typically used with clusters where a cluster node is a member of a cluster.

 Example: ESXi Server is a member of vCenter Cluster.

</td></tr><tr><td>

Owns

</td><td>

Owned by

</td><td>

Usually a containment relationship \(CI to owned CI\). The child CI typically has a single parent with this relationship type.

</td></tr><tr><td>

Runs on

</td><td>

Runs

</td><td>

Typically between a CI that represents a software application, to the hosting hardware/VM.

 Example: Tomcat 'Runs on' Linux server.

</td></tr><tr><td>

Use End Point To

</td><td>

Use End Point From

</td><td>

From the CI to an outgoing endpoint.

 **Note:** For internal use only \(service model\).

</td></tr></tbody>
</table>-   **[Suggested class relationships](../reference/r_SuggestedRelationshipModel.md)**  
The system keeps a table \(Suggested Relationship \[cmdb\_rel\_type\_suggest\]\) of relationship types that are appropriate for a CI type, based on its class. You can manage suggested relationships by navigating to **Configuration** &gt; **Suggested Relationships**, or in the CI Class Manager.
-   **[Add a suggested relationship](../task/t_AddANewSuggestedRelationship.md)**  
Add a suggested relationship for a class. The list of suggested relationships for a class is available when you create a new relationship for a CI of that class.
-   **[Relationship governance rules](relationship-governance.md)**  
Relationship governance rules is a set of relationship rules used to ensure consistency and validity in modeling relationships between configuration items \(CIs\) in the CMDB. Use relationship governance rules to prevent the selection of relationship types or directions that are not allowed between specific CI types.
-   **[CI relations formatter](c_CIRelationsFormatterNG.md)**  
The default CI form includes a CI relations formatter from which you can examine a CI and its relationships in various views. From the CI relations formatter, you can also launch the CI relationship editor for the CI.
-   **[CI relationship editor](c_RelationshipEditor.md)**  
Use the relationship editor to view, create, modify, or delete CI relationships. Open the relationship editor from the CI Relations formatter.
-   **[Relation qualifier](c_RelationQualifier.md)**  
A relation qualifier, which is a CI of the Qualifier \[cmdb\_ci\_qualifier\] type, stores important information about the CI relationships.
-   **[CI relationship security](c_CIRelationshipSecurity.md)**  
When applying security to CI relationships, it is important to apply the access controls both to the CI Relationship \(cmdb\_rel\_ci\) table and to create an operation editCIRelations to the \* table as well.
-   **[Create a CI relation rollup](../task/t_CreateACIRelationRollup.md)**  
A CI relation rollup allows you to sum, count, max, min, or mean a relationship type. You can create CI relation rollups.

**Parent Topic:**[Configuration Management Database \(CMDB\)](c_ITILConfigurationManagement.md)

**Related topics**  


[Create a CI relation rollup](../task/t_CreateACIRelationRollup.md)

