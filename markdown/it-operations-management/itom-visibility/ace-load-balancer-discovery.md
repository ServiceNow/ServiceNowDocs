---
title: Cisco ACE load balancer discovery
description: Discovery identifies and classifies information about ACE load balancers.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Cisco ACE load balancer discovery

Discovery identifies and classifies information about ACE load balancers.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Credentials

Configure [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) and [SSH credentials](https://www.servicenow.com/docs/access?context=r_SSHCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

## Classifier, pattern, and probe

|Classifier|Trigger probes|Pattern|
|----------|--------------|-------|
|ACE Load Balancer|Horizontal discovery probe: launches patterns|ACE Load Balancer by SSH \(formerly ACE Load Balancer\)|

## Data collected

The following data is collected on the Ace Load Balancers `[cmdb_ci_lb_ace]` table.

|Label|Field Name|
|-----|----------|
|Serial Number|serial\_number|
|Operational Status|operational\_status|

The following data is collected on the Load Balancer Services \[cmdb\_ci\_lb\_service\] table.

|Label|Field Name|
|-----|----------|
|Name|name|
|IP address|ip\_address|
|Port|port|
|Operational status|operational\_status|
|Install status|install\_status|
|Short description|short\_description|

The following data is collected on the DNS \[cmdb\_ci\_dns\_name\] table.

|Label|Field name|
|-----|----------|
|Name|name|
|IP address|ip\_address|

The following data is collected on the Load Balancer Pool \[cmdb\_ci\_lb\_pool\] table.

|Label|Field name|
|-----|----------|
|Name|name|
|Context|context|
|Load balancing method|load\_balancing\_method|

The following data is collected on the Load Balancer Pool Members \[cmdb\_ci\_lb\_pool\_member\] table.

|Label|Field name|
|-----|----------|
|Name|name|
|IP address|ip\_address|
|Service port|service\_port|
|Pool|pool|
|Context|context|

The following data is collected on the Serial Number \[cmdb\_serial\_number\] table.

|Label|Field name|
|-----|----------|
|Serial number|serial\_number|
|Serial number type|serial\_number\_type|
|Valid|valid|

The following data is collected on the Load Balancer Interface table \[cmdb\_ci\_lb\_interface\] table:

|Label|Field name|
|-----|----------|
|Name|nam|
|MAC address|mac\_address|
|Operational status|operational\_status|

**Parent Topic:**[Load balancer discovery](c_LoadBalancers.md)

