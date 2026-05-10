---
title: Radware-appDirector load balancer discovery
description: Discovery of Radware load balancers is performed by SNMP.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Radware-appDirector load balancer discovery

Discovery of Radware load balancers is performed by SNMP.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Requirements

**Important:** Discovery treats load balancers as licensable entities and attempts to discover them primarily using SNMP. If a load balancer in your system, running on a Linux host, has SNMP and SSH ports open, Discovery might classify it based on the SSH port. This classification has priority over SNMP. To ensure that Discovery properly classifies your hardware load balancers, create a Discovery behavior for load balancers that includes SNMP but not SSH. Software load balancers are treated as applications.

## Credentials

Configure [SNMP credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/c_SNMPCredentials.md).

## Classifier, pattern, and probes

|Classifier|Probe|Pattern|
|----------|-----|-------|
|Radware - AppDirector - Load Balancer|Horizontal discovery probe: launches patterns|AppDirector Load Balancer|

## Data discovery

The following data is collected on the Radware Load Balancers `[cmdb_ci_lb_radware]` table.

|Label|Field name|
|-----|----------|
|Serial number|serial\_number|

The following data is collected on the DNS Name `[cmdb_ci_dns_name]` table.

|Label|Field name|
|-----|----------|
|Name|name|
|IP address|ip\_address|

The following data is collected on the Load Balancer Services `[cmdb_ci_lb_service]` table.

|Label|Field Name|
|-----|----------|
|Name|name|
|IP Address|ip\_address|
|Port|port|
|Operational Status|operational\_status|
|Install Status|install\_status|

**Parent Topic:**[Load balancer discovery](c_LoadBalancers.md)

