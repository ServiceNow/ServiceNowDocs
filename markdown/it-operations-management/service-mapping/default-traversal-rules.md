---
title: Predefined traversal rules for application services in Service Mapping
description: Service Mapping uses traversal rules to bring in related configuration items and expand the application service map. Several predefined rules are provided by default to help find and correctly map these relationships.
locale: en-US
release: xanadu
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2025-11-04"
reading_time_minutes: 1
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Predefined traversal rules for application services in Service Mapping

Service Mapping uses traversal rules to bring in related configuration items and expand the application service map. Several predefined rules are provided by default to help find and correctly map these relationships.

## About traversal rules

Predefined traversal rules in Service Mapping are key to identifying the relationships between configuration items \(CIs\) and building accurate application service maps. To maintain integrity and avoid issues, such as incomplete maps or service disruptions, these rules are fixed. You can't change, customize, or remove them. To create custom traversal rules to meet your organization's needs, see [Traversal Rules for Application Services form completion](traversal_rules_form_completion.md).

## Predefined traversal rules

|Parent Type|Relationship|Child Type|Priority Level|Is Reverse|
|-----------|------------|----------|--------------|----------|
|cmdb\_ci|Runs on::Runs|Hardware \[cmdb\_ci\_hardware\]|100|false|
|cmdb\_ci|Hosted on::Hosts|Logical Datacenter \[cmdb\_ci\_logical\_datacenter\]|200|false|
|cmdb\_ci\_lb\_service|Hosted on::Hosts|Cloud Load Balancer \[cmdb\_ci\_cloud\_load\_balancer\]|300|false|
|cmdb\_ci\_cluster\_node|Hosted on::Hosts|Server \[cmdb\_ci\_server\]|400|true|
|cmdb\_ci|Contains::Contained by|Tracked Configuration File \[cmdb\_ci\_config\_file\_tracked\]|500|false|
|cmdb\_ci\_cluster\_node|Cluster of::Cluster|Cluster \[cmdb\_ci\_cluster\]|600|false|
|cmdb\_ci\_cluster\_node|Cluster of::Cluster|Cluster \[cmdb\_ci\_cluster\]|700|true|
|cmdb\_ci\_cluster\_node|Hosted on::Hosts|Server \[cmdb\_ci\_server\]|800|false|

For example, the first row of the table illustrates a traversal rule that identifies and adds the hardware \(cmdb\_ci\_hardware\) supporting a given software application \(cmdb\_ci\). When **Is Reverse** is set to false, the discovery process starts with the application and identifies the hardware it runs on-traversing from the parent CI to the child CI. The relationships are then added to the application service map.

To learn more about traversal rule components and related terminology, see [Traversal rules in Service Mapping](../concept/traversal-rules-service-mapping.md).

**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

