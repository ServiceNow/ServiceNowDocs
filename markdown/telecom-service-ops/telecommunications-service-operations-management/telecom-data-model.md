---
title: Telecom data model
description: The Telecom data model defines a structured framework for representing telecommunications networks within the CMDB. It extends the core Configuration Item \(CI\) model to describe telecom‑specific infrastructure, connections, and relationships in a consistent and scalable way.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Telecom Discovery, Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Telecom data model

The Telecom data model defines a structured framework for representing telecommunications networks within the CMDB. It extends the core Configuration Item \(CI\) model to describe telecom‑specific infrastructure, connections, and relationships in a consistent and scalable way.

At its core, the Telecom data model organizes network elements such as equipment, interfaces, ports, sites, and connections, and defines how these elements relate to one another. The model captures both physical and logical aspects of the network and uses containment and consumption relationships to represent how network components are assembled and interconnected. This structure enables accurate modeling of complex telecom environments while remaining aligned with the standard CMDB architecture.

The Telecom data model is designed to be extensible and technology‑agnostic. It provides a common foundation that supports multiple telecommunications domains by reusing existing CMDB classes where possible and introducing new classes only when telecom‑specific representation is required.

## Key components

-   Network equipment and hardware: Physical and logical equipment, along with the components they contain, such as interface cards and ports.
-   Interfaces and ports: Network interfaces and ports that enable connectivity between devices and services.
-   Sites and locations: Logical and physical locations used to group and organize network infrastructure.
-   Links, circuits, and connections: Physical and logical connections that describe how network elements communicate and exchange data.

## Benefits

By providing a consistent way to model telecom infrastructure and relationships, the Telecom data model enables accurate network inventory, impact analysis, and operational insight. The shared structure supports integration across systems, improves data consistency, and simplifies analysis of network topology and dependencies. This common modeling approach helps teams manage complex networks more effectively and supports use cases such as service visibility, operational monitoring, and lifecycle management.

## Domain‑specific data models

Domain‑specific data models build on the Telecom data model by refining and specializing its classes for particular network technologies. These models reuse the core structure of the Telecom data model while introducing domain‑specific attributes and relationships as needed. The SD‑WAN data model is one example of a domain‑specific data model. It focuses on the subset of Telecom data model concepts that are relevant to SD‑WAN environments and applies them to represent SD‑WAN topology, services, and operations, while remaining consistent with the broader Telecom data model.

**Related topics**  


[SD-WAN data model](sd-wan-data-model.md)

[Data model](https://www.servicenow.com/docs/access?context=uses-for-network-inventory-data&version=australia&pubname=australia-telecom-network-inventory&ft:locale=en-US)

