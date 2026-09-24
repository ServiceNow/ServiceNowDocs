---
title: MPN health status rule reference
description: Default rule set \(version 0.0.11\) for calculating health status for MPN radio and core server components, including error codes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/mpn-rag-status-rule-reference.html
release: brazil
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [RAG status, error codes, reference, MPN]
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# MPN health status rule reference

Default rule set \(version 0.0.11\) for calculating health status for MPN radio and core server components, including error codes.

## Rule structure

Rules are organized by component type. Health status uses a RAG \(Red, Amber, Green\) indicator system. For radio and core server components, each condition is a simple field-and-value match tied to an error code. A green result requires all conditions in the component's green rule to match simultaneously. If no rule matches, the status is unknown.

## Default rules for radio components

|Health status|Field|Value|Error code|
|-------------|-----|-----|----------|
|Red|`alarm_status`|MAJOR|EC2002|
|Red|`alarm_status`|CRITICAL|EC2003|
|Red|`operational_status`|DISABLED|EC2004|
|Red|`operational_status`|NOT\_AVAILABLE|EC2001|
|Red|`cell_status`|INACTIVE|EC2005|
|Red|`cell_status`|NOT\_AVAILABLE|EC2006|
|Red|`mme_status`|DISCONNECTED|EC2001|
|Red|`mme_status`|NOT\_AVAILABLE|EC2001|
|Red|`ap_connection_status`|DISCONNECTED|EC2001|
|Red|`ap_connection_status`|NOT\_AVAILABLE|EC2001|
|Amber|`alarm_status`|MINOR|EC2101|
|Amber|`alarm_status`|INDETERMINATE|EC2102|
|Amber|`alarm_status`|WARNING|EC2103|
|Amber|`operational_status`|UNKNOWN|EC2104|
|Amber|`cell_status`|UNKNOWN|EC2105|
|Amber|`cell_status`|PARTIALLY\_ACTIVE|EC2106|
|Amber|`mme_status`|UNKNOWN|EC2107|
|Amber|`ap_connection_status`|UNKNOWN|EC2107|
|Green|`alarm_status AND operational_status AND cell_status`|NORMAL, ENABLED, ACTIVE \(all three required\)|—|
|Unknown|\(no rule matched\)|—|EC2108|

## Default rules for core server components

|Health status|Field|Value|Error code|
|-------------|-----|-----|----------|
|Red|`edge_connection`|EDGE\_CONN\_STATUS\_UNAVAILABLE|EC3001|
|Red|`edge_connection`|OFFLINE|EC3002|
|Green|`edge_connection`|ONLINE|—|
|Unknown|\(no rule matched\)|—|EC3101|

## Default health rules for network-level aggregation

|Health status|Condition|Error code|
|-------------|---------|----------|
|Red|All radio components are red|EC1001|
|Red|All core server components are red|EC1002|
|Amber|Not all radio components are green|EC1101|
|Amber|Not all core server components are green|EC1102|
|Green|All radio and core server components are green|—|
|Unknown|\(no rule matched\)|EC1103|

**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

**Related topics**  


[Mobile private network health status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/rag-status-overview.md)

[MPN Formula Engine processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formula-engine.md)

