---
title: TNI Data Model Navigator
description: A Data Model Navigator is a CMDB framework feature that presents a curated, domain-specific view of the CMDB. With TNI \(Telecommunications Network Inventory\) context, it organizes thousands of CMDB CI classes into a focused, hierarchical structure relevant to telecom operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-network-inventory/telecommunications-network-inventory/data-model-navigator.html
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: concept
last_updated: "2026-07-09"
reading_time_minutes: 3
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# TNI Data Model Navigator

A Data Model Navigator is a CMDB framework feature that presents a curated, domain-specific view of the CMDB. With TNI \(Telecommunications Network Inventory\) context, it organizes thousands of CMDB CI classes into a focused, hierarchical structure relevant to telecom operations.

Data Model Navigator framework stores and organizes metadata in four interconnected components: Contexts: Hierarchical Organization Tables: CI Class Descriptions Fields: Critical Attributes Relationships: How tables connect with one another.

Data Model Navigator framework stores and organizes metadata in four interconnected components:

-   Contexts: Hierarchical Organization
-   Tables: CI Class Descriptions
-   Fields: Critical Attributes
-   Relationships: How tables connect with one another

## Context

A model context is a curated view of the Configuration Management Database \(CMDB\) that organizes CI classes, fields, and relationships around a specific operational domain. Instead of requiring you to navigate thousands of CI classes in the full CMDB hierarchy, a model context shows only the data relevant to your work.

Contexts are hierarchical. A **parent context** defines the broadest domain grouping. **Child contexts** subdivide it into focused subdomains, each carrying its own mapped tables, documented fields, and defined relationships.

Telecom Network Inventory \(TNI\) Context Hierarchy.

The Telecom Network Inventory is a parent context containing 6 child contexts, each representing a layer of telecom infrastructure:

-   TNI Physical: Fiber infrastructure \(cables, strands, splice closures, cross-connect panels\)
-   TNI Logical: Logical paths that ride over physical \(PON paths, VLAN circuits, MPLS LSPs\)
-   TNI Services: Service instances that contain logical paths
-   TNI Site: Site-level containers and racks
-   TNI Facilities: Power, cooling, physical plant infrastructure
-   TNI Topology: Network topology views and relationships

## Tables — CI Class Descriptions

Metadata describing what each CMDB CI class tracks, its purpose, and variations across contexts.

Example: Optical Fiber Cable Table.

|Field|Description|
|-----|-----------|
|**Table name**|cmdb\_ci\_optical\_fiber\_cable|
|**Purpose**|Physical cable containing individual fiber strands for telecom transmission. Cables bundle multiple fibers for protection and routing through infrastructure.|
|**Context**|TNI Physical layer|
|**GPON Planning use case**|Determines splitter capacity and service provisioning|
|**Inventory Management use case**|Tags equipment and tracks deployment|
|**Capacity Planning use case**|Aggregates service capacity by cable|

## Fields — Critical Attributes

Field-level metadata describing critical attributes, their importance across use cases, and sample values.

Example: Fiber Cable Fields.

Field 1: strand\_count.

|Aspect|Details|
|------|-------|
|**Description**|Number of individual fiber strands contained in this cable|
|**GPON Planning \(CRITICAL\)**|Determines how many circuits this cable can support|
|**Inventory \(INFORMATIONAL\)**|Tags equipment specification|
|**Sample data**|"24", "48", "96"|

Field Metadata = Describes individual fields within a CI class table, their purpose across use cases, and sample values.

**Importance of Field Metadata:** An agent knows which fields matter for which decisions and can provide realistic examples to users.

## Relationships

Metadata describing how CI classes relate to each other, why those relationships exist, and their importance in different use cases.

Relationship 1: Service Contains Logical.

|Field|Value|
|-----|-----|
|**Source**|cmdb\_ci\_connection\_service\_instance \(service layer\)|
|**Target**|cmdb\_ci\_nl\_logical\_path \(logical layer\)|
|**Modeling reason**|Customer services ride over logical connectivity paths|
|**Critical for**|End-to-end service mapping, customer billing|

Relationship 2: Logical Rides Over Physical.

|Field|Value|
|-----|-----|
|**Source**|cmdb\_ci\_nl\_logical\_path \(PON path\)|
|**Target**|cmdb\_ci\_nl\_physical\_link \(fiber span\)|
|**Modeling reason**|Logical connectivity requires physical fiber to carry signals|
|**Critical for**|Network topology mapping, troubleshooting, capacity planning|

Relationship Metadata: Describes how CI classes connect across TNI layers and why those relationships matter.

Understanding Relationship Mapping: An agent understands how to traverse the data model \(Service → Logical → Physical → Equipment\) to answer complex questions.

**Parent Topic:**[Telecommunications Network Inventory reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/telecommunications-network-inventory-reference.md)

**Related topics**  


[Access TNI data model navigator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecommunications-network-inventory/access-tni-data-model-navigator.md)

