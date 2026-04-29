---
title: CMDB dependent relationship rules
description: Service definitions consist of CI types and relationship types. Dependent relationship rules define the dependency structure of the CI types and the relationship types in these service definitions, helping in CI identification and in the construction of business service maps.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, CMDB Identification and Reconciliation \(IRE\), Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB dependent relationship rules

Service definitions consist of CI types and relationship types. Dependent relationship rules define the dependency structure of the CI types and the relationship types in these service definitions, helping in CI identification and in the construction of business service maps.

The dependencies that are defined by these rules are used when identifying dependent CIs to prioritize the order of CI identification, and to match CIs and respective dependent CIs in a payload. Dependent relationship rules are also used by Service Mapping and can be defined for custom CI types. After defining a new CI type, you can define dependent relationship rules that specify how the new CI type is related to existing types in the CMDB.

Dependent relationship rules consist of hosting and containment rules \(dependent relationship rules\), each type modeling the data from a different perspective of the CI. Containment rules represent CIs' configuration hierarchy, describing which CI contains which other CIs. Hosting rules represent CIs' placement in a business definition, describing what CIs run on.

Both hosting and containment rules describe a relationship type between two CI types and the same relationship type can be used in a hosting rule and in a containment rule. It is the context in which the relationship is used that distinguishes between a containment and hosting rule.

Manage dependent relationship rules:

-   To access rules at the class level, use the CI Class Manager. Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**.
-   To access grouped rules, use the Metadata Editor. Navigate to **All** &gt; **Configuration** &gt; **Identification/Reconciliation** &gt; **Metadata Editor**.

The plugins that have been activated on an instance determine which hosting and containment rules exist in a base system.

## Hosting rules

Hosting rules represent all the possible valid combinations of pairs of hosting and hosted CIs in the service definition. Hosting rules are a flat set of rules that can be only one level deep, and which always involve resources, typically physical or virtual hardware. Each hosting rule is a stand-alone rule between two CI types, describing either a valid CI type that another CI type can host, or by which another CI type can be hosted. A hosting rule consists of a parent CI type, a relationship type \(such as Hosted On::Hosts\) and a child CI type. For example, you can have a hosting rule that specifies that the CI type ‘Application’ ‘Runs On::Runs’, the CI type ‘Hardware’.

A CI can be hosted on multiple resources \(such as Windows and Linux\). This CI is represented by a hosting rule for the CI with each resource that the CI can be hosted on. During CI identification, the pair of CIs that are being examined, should satisfy at least one hosting rule.

Hosting rules are stored in the CMDB Metadata Hosting Rules \[cmdb\_metadata\_hosting\] table.

## Containment rules

Containment rules represent the containment hierarchy for a CI type, describing valid objects that a CI type can contain in the service definition, and valid objects that can be contained by the CI type. Containment rules are chained to each other in a containment rules group, with a CI type that is the top-level \(root\) parent of the group. The collection of containment rules construct a hierarchy-like map of containment relationships. Containment rules are logical concepts used to represent logical CIs, for example to describe software that runs on a server. A containment rule consists of a parent CI type, a relationship type \(such as 'Contained By::Contains'\), and a child CI type. For example, you might have a containment rule specifying that the CI type ‘Tomcat’ ‘Contains::Contained By' CI type ‘WAR File’.

Endpoints are special containment rules that specify incoming or outgoing connections in the model, designating the CI types that data of some specified type flows in to or out from the service definition. After adding an endpoint to a containment rule, you cannot add any child rules to the endpoint rule.

Containment rules are stored in the CMDB Metadata Containment Rules \[cmdb\_metadata\_containment\] table.

## Reference rules

Reference rules are used mostly by Cloud Management to represent all of the possible valid combinations of pairs of referencing and referenced CIs in the service definition.

-   Reference rules are a flat set of rules that can be only one level deep.
-   Reference rules always involve resources, typically virtual entities. Each reference rule is a stand-alone rule between two CI types, describing either a valid CI type that another CI type can reference, or by which another CI type can be referenced. Both the CI classes should be able to live independent of each other.
-   A referencing rule consists of a parent CI type, a relationship type \(such as `Provisioned From::Provisioned`\) and a child CI type. For example, you can have a referencing rule that specifies that the CI type ‘Virtual Machine’ `Provisioned From::Provisioned`, the CI type ‘Image’.
-   A CI can reference multiple resources \(for example, a VM Instance can have a reference relation with both the Image and the Hardware templates\). This CI is represented by a referencing rule for the CI with each resource that the CI can be referenced from.
-   The reference rule cannot be part of the CI identification.
-   Reference rules are stored in the CMDB Metadata Reference Rules \[cmdb\_metadata\_reference\] table.

## Rules requirements

The rules that you create are bound by the following requirements which narrow the relationships and ensure that only valid options are available in the drop-down lists in the Metadata Editor.

-   Given a CI type that is as a child in a containment rule: Not this CI type or its children can be a top-level \(root\) parent of any other containment rule, and it cannot be in any hosting rule, either as a parent or as a child.
-   Given a CI type that is a top-level \(root\) parent of a containment rule: It cannot be a child in a hosting rule \(for example, you cannot be hosted on Tomcat, if Tomcat has any containment rules\).
-   Given a CI type that is a child in a hosting rule: It cannot be in any containment rule, either as a parent or a child.
-   Given a CI type that is a parent in a hosting rule: It cannot be a child in any containment rule.
-   Hosting rules cannot create loops such as Tomcat –runs\_on- VMWare –runs\_on- Tomcat.

## Hosting and containment rules model

![Hosting and containment rules.](../image/MetadataRulesDiagram.png)

Hosting rules that model the diagram:

Tomcat 'Runs on' Hardware.

Containment rules that model the diagram:

-   Tomcat 'Contains' Configuration File
-   Tomcat 'Contains' WAR
-   WAR has two endpoints for JDBC with MySQL:
    -   Inbound
    -   Outbound

## Valid set of rules

```

Tomcat Hosted Linux
Linux Hosted Computer
```

The second metadata entry triggers the third requirement, which is satisfied \(it is a hosting rule, not a containment rule\).

-   **[Create dependent relationship rules](create-dependent-relationship.md#)**  
Create hosting and containment rules \(dependent relationship rules\) for CI classes to help with correctly identifying dependent CIs during the business discovery process and service mapping. Discovery calls the identification API that applies dependent relationship rules.

**Parent Topic:**[Configuring CMDB Identification and Reconciliation](configuring-ire.md)

