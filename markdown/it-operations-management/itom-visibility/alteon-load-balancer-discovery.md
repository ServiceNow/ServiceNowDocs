---
title: Radware Alteon load balancer discovery
description: Discovery identifies and classifies information about Alteon load balancers.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Radware Alteon load balancer discovery

Discovery identifies and classifies information about Alteon load balancers.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Credentials

Configure [SNMP credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/c_SNMPCredentials.md).

## Classifier, pattern, and probe

|Classifier|Trigger probe|Pattern|
|----------|-------------|-------|
|Alteon Load Balancer|Horizontal pattern|Alteon Load Balancer by SNMP \(formerly Alteon Load Balancer\)|

## Data collected

The following data is collected on the Alteon `[cmdb_ci_lb_alteon]` table.

|Label|Field Name|
|-----|----------|
|Serial Number|serial\_number|
|Operational Status|operational\_status|

The following data is collected on the Load Balancer Interface table \[cmdb\_ci\_lb\_interface\] table:

|Label|Field name|
|-----|----------|
|Name|nam|
|MAC address|mac\_address|
|Operational status|operational\_status|
|Index|index|

The following data is collected on the Load Balancer Pool \[cmdb\_ci\_lb\_pool\] table.

|Label|Field name|
|-----|----------|
|Name|name|
|Index|index|
|Load balancing method|load\_balancing\_method|

The following data is collected on the Load Balancer Pool Member \[cmdb\_ci\_pool\_member\] table:

|Label|Field name|
|-----|----------|
|IP address|ip\_address|
|Service port|service\_port|

The following data is collected on the Load Balancer Services \[cmdb\_ci\_lb\_service\] table.

|Label|Field Name|
|-----|----------|
|Name|name|
|IP address|ip\_address|
|Port|port|
|Operational status|operational\_status|
|Install status|install\_status|
|Hit count|hit\_count|

The following data is collected on the DNS \[cmdb\_ci\_dns\_name\] table.

|Label|Field name|
|-----|----------|
|Name|name|
|IP address|ip\_address|

**Parent Topic:**[Load balancer discovery](c_LoadBalancers.md)

