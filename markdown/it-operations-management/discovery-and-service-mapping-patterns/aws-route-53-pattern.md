---
title: Amazon Route 53 pattern-based discovery
description: Discovery and Service Mapping Patterns finds Amazon Route 53 domain name systems \(DNS\) and aliases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2025-12-25"
reading_time_minutes: 1
keywords: [Amazon AWS Route53, Amazon Route 53, Route 53, AWS discovery, AWS patterns, DNS discovery]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Amazon Route 53 pattern-based discovery

Discovery and Service Mapping Patterns finds Amazon Route 53 domain name systems \(DNS\) and aliases on your cloud environment. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Pattern-based discovery and mapping requirements

Verify the AWS discovery prerequisites section in [Amazon AWS Cloud components discovery using patterns](../../discovery/reference/data-discovered-aws-patterns.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Amazon AWS Route53 pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The DNS domain name for the hosted zone.|
|IP Address \[ip\_address\]|The IP address resolved from the DNS name.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The alias name for the DNS record set.|

|Field|Description|
|-----|-----------|
|Object ID \[object\_id\]|The unique identifier \(ID\) for the cloud service account.|
|Account Id \[account\_id\]|The unique ID for the cloud service account.|

## CI relationships

The Amazon AWS Route53 pattern creates these relationships to support Amazon Route 53 discovery.

|CI|Relationship|CI|
|---|------------|---|
|DNS Name \[cmdb\_ci\_dns\_name\]|Used by::Uses|DNS Alias \[cmdb\_ci\_dns\_alias\]|
|DNS Name \[cmdb\_ci\_dns\_name\]|Hosted on::Hosts|Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\]|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

