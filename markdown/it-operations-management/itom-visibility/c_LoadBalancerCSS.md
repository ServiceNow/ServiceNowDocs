---
title: Cisco CSS load balancer
description: Discovery of Cisco CSS load balancers is performed by SNMP.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Load balancers, Network device discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Cisco CSS load balancer

Discovery of Cisco CSS load balancers is performed by SNMP.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

## Classifiers

Discovery uses the Cisco CSS Load Balancer classifier, which contains the OID Classification: 1.3.6.141.9.9.368.4.5.

## Probes

The following probes are triggered:

|Probe|Description|Type|
|-----|-----------|----|
|SNMP - Load Balancer - Identity|A multiprobe that identifies load balancers.|Java-SNMP|
|Cisco CSS - Get Services|A Java probe that includes the Cisco CSS sensor to identify services defined on the load balancer in the Load Balancer Services \[cmdb\_ci\_lb\_service\] table. For every service, Discovery populates **Name**, **ip\_address**, and **port**.|Java-SNMP|

## Tables

Discovery creates a record for each CSS device in the Cisco CSS \[cmdb\_ci\_lb\_cisco\_css\] table, which includes the device's **Name**, **Model**, **Serial Number**, **Manufacture**, and **NIC** \(ip\_address\). It also creates a record for each service in the Load Balancer Services \[cmdb\_ci\_lb\_service\] table.

.

**Parent Topic:**[Load balancer discovery](c_LoadBalancers.md)

