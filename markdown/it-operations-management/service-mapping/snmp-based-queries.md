---
title: SNMP-based queries
description: Service Mapping accesses network infrastructure devices like load balancers and routers using Simple Network Management Protocol \(SNMP\) v1/v2c/v3. Configure SNMP community credentials to enable this type of access.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prerequisites for performing top-down discovery using Service Mapping, Configuring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# SNMP-based queries

Service Mapping accesses network infrastructure devices like load balancers and routers using Simple Network Management Protocol \(SNMP\) v1/v2c/v3. Configure SNMP community credentials to enable this type of access.

Configure SNMP community if you use SNMP v1/v2 or SNMPv3 credentials if you use SNMP v3. For operational information, see SSH credentials.

SNMP-based queries have the format of strings of integers.

## General SNMP-based queries

Make sure that the user has credentials for SNMPv3 unless read-only community string is used.

-   1.3.6.1.2.1.47.1.1.1.1.13
-   1.3.6.1.2.1.1.6
-   1.3.6.1.2.1.47.1.1.1.1
-   1.3.6.1.4.1.9.9.774.1.1.1
-   1.3.6.1.4.1.9.6

## SNMP-based queries for switches and routers

-   1.3.6.1.4.1.9.9.46.1.3.1.1
-   1.3.6.1.4.1.9.9.68.1.2.1.1
-   1.3.6.1.2.1.17.1.4.1
-   1.3.6.1.2.1.17.4.3.1
-   1.3.6.1.2.1.17.7.1.2.2.1
-   1.3.6.1.2.1.17.2.15.1
-   1.3.6.1.4.1.9.9.23.1.2.1.1
-   1.3.6.1.4.1.45.1.6.13.2.1.1
-   1.0.8802.1.1.2.1.4.2.1
-   1.0.8802.1.1.2.1.4.1.1

## A10 Thunder Series

-   1.3.6.1.4.1.1872.2.5.1.1.1.11
-   1.3.6.1.4.1.1872.2.5.3.1.3.2.1
-   1.3.6.1.4.1.1872.2.5.3.1.2.4.1
-   1.3.6.1.4.1.1872.2.5.1.3.1.10
-   1.3.6.1.4.1.1872.2.5.4.1.1.4.2.1
-   1.3.6.1.4.1.1872.2.5.3.1.6.3.1
-   1.3.6.1.4.1.22610.2.4.1.1.1
-   1.3.6.1.4.1.22610.2.4.1.6.2
-   1.3.6.1.4.1.22610.2.4.3.4.1.2.1
-   1.3.6.1.4.1.22610.2.4.3.2.1.2.1
-   1.3.6.1.4.1.22610.2.4.3.3.1.2.1
-   1.3.6.1.4.1.22610.2.4.3.4.3.1.1
-   1.3.6.1.4.1.22610.2.4.3.3.3.1.1

## BIG-IP Local Traffic Manager \(LTM \) F5 \(on F5 BIG-IP\) and BIG-IP Global Traffic Manager \(GTM\) F5

-   1.3.6.1.4.1.3375.2.1.6.3
-   1.3.6.1.4.1.3375.2.1.4.1
-   1.3.6.1.4.1.3375.2.1.3.3.3
-   1.3.6.1.4.1.3375.2.1.6.2
-   1.3.6.1.4.1.3375.2.1.2.1.1.2.1
-   1.3.6.1.4.1.3375.2.2.10.1.2.1
-   1.3.6.1.4.1.3375.2.3.12.4.2.1
-   1.3.6.1.4.1.3375.2.3.12.1.2.1
-   1.3.6.1.4.1.3375.2.1.4.1
-   1.3.6.1.4.1.3375.2.1.6.2
-   1.3.6.1.4.1.3375.2.1.4.2
-   1.3.6.1.4.1.3375.2.2.10.1.2.1
-   1.3.6.1.4.1.3375.2.2.5.6.2.1
-   1.3.6.1.4.1.3375.2.2.10.8.2.1
-   1.3.6.1.4.1.3375.2.2.5.6.2.1
-   1.3.6.1.4.1.3375.2.2.10.1.2.1
-   1.3.6.1.4.1.3375.2.1.4.1
-   1.3.6.1.4.1.3375.2.1.4.2
-   1.3.6.1.4.1.3375.2.1.6.2
-   1.3.6.1.4.1.3375.2.3.11.1.2.1
-   1.3.6.1.4.1.3375.2.3.12.3.2.1
-   1.3.6.1.4.1.3375.2.3.12.4.2.1
-   1.3.6.1.4.1.3375.2.2.5.6.2.1
-   1.3.6.1.4.1.3375.2.3.12.3.2.1
-   1.3.6.1.4.1.3375.2.3.12.4.2.1
-   1.3.6.1.4.1.3375.2.3.12.5.2.1
-   1.3.6.1.4.1.3375.2.3.6.7.2.1
-   1.3.6.1.4.1.3375.2.3.11.4.2.1
-   1.3.6.1.4.1.3375.2.3.3.1.2.1
-   1.3.6.1.4.1.3375.2.3.3.3.2.1
-   1.3.6.1.4.1.3375.2.3.9.1.2.1
-   1.3.6.1.4.1.3375.2.3.9.3.2.1

## Cisco Content Services Switch \(CSS\)

-   1.3.6.1.4.1.2467.1.16.4.1
-   1.3.6.1.4.1.2467.1.31.3
-   1.3.6.1.2.1.1.2
-   1.3.6.1.4.1.2467.4.1
-   1.3.6.1.4.1.2467.4.2
-   1.3.6.1.4.1.2467.4.3
-   1.3.6.1.4.1.2467.4.4
-   1.3.6.1.2.1.1.1
-   1.3.6.1.4.1.2467.1.15.2.1
-   1.3.6.1.4.1.2467.1.16.4.1
-   1.3.6.1.4.1.2467.1.18.2.1

## Cisco Global Site Selector \(GSS\)

-   1.3.6.1.2.1.1.5 – to get the hostname.
-   1.3.6.1.2.1.1.1 – to get product name.

## Citrix Netscaler

-   1.3.6.1.4.1.5951.4.1.3.6.1
-   1.3.6.1.4.1.5951.4.1.3.2.1
-   1.3.6.1.4.1.5951.4.1.3.1.1
-   1.3.6.1.4.1.5951.4.1.2.7.1
-   1.3.6.1.4.1.5951.4.1.2.2.1
-   1.3.6.1.4.1.5951.4.1.2.11.1
-   1.3.6.1.4.1.5951.4.1.2.1.1
-   1.3.6.1.4.1.5951.4.1.1.6
-   1.3.6.1.4.1.5951.4.1.1.26.1
-   1.3.6.1.4.1.5951.4.1.1.24.1
-   1.3.6.1.4.1.5951.4.1.1.14
-   1.3.6.1.2.1.55.1.8.1
-   1.3.6.1.2.1.47.1.1.1.1
-   1.3.6.1.2.1.4.20.1
-   1.3.6.1.2.1.2.2.1
-   1.3.6.1.2.1.2.2.1
-   1.3.6.1.2.1.1.5

## Citrix Netscaler Global Server Load Balancer

-   1.3.6.1.4.1.5951.4.1.1.51.3.1.1
-   1.3.6.1.4.1.5951.4.1.2.1.1

## HPE BladeSystem Enclosure

-   1.3.6.1.4.1.232.22.2.3.1
-   1.3.6.1.4.1.11.5.7.1.2

## IBM WebSphere DataPower

-   For horizontal discovery of the Data Power Hosting Server \[cmdb\_ci\_datapower\_server\]:
    -   1.3.6.1.2.1.1.1
    -   1.3.6.1.2.1.1.5
    -   1.3.6.1.2.1.4.20.1
    -   1.3.6.1.2.1.2.2.1
    -   1.3.6.1.4.1.14685.3.1.196.1
    -   1.3.6.1.4.1.14685.3.1.11.1
    -   1.3.6.1.4.1.14685.3.1.112.1
-   For top-down discovery of the Data Power \[cmdb\_ci\_datapower\_server\]:
    -   1.3.6.1.2.1.1.1
    -   1.3.6.1.2.1.1.5
    -   1.3.6.1.4.1.14685.3.1.11.1

## Juniper Junos

1.3.6.1.4.1.2636.3.1.3

## Network Appliance Filer Storage Array

-   1.3.6.1.4.1.789.1.1.2
-   1.3.6.1.4.1.789.1.1.9

## Radware Alteon NG

-   1.3.6.1.4.1.1872.2.5.4.2.32.1
-   1.3.6.1.4.1.1872.2.5.1.1.1.11
-   1.3.6.1.4.1.1872.2.5.3.1.3.2.1
-   1.3.6.1.4.1.1872.2.5.3.1.2.4.1
-   1.3.6.1.4.1.1872.2.5.1.3.1.10
-   1.3.6.1.4.1.1872.2.5.4.1.1.4.2.1
-   1.3.6.1.4.1.1872.2.5.3.1.6.3.1
-   1.3.6.1.4.1.1872.2.5.4.1.1.4.2.1
-   1.3.6.1.2.1.1.1
-   1.3.6.1.4.1.1872.2.5.4.1.1.4.5.1
-   1.3.6.1.4.1.1872.2.5.4.1.1.3.3.1
-   1.3.6.1.4.1.1872.2.5.4.1.1.2.2.1
-   1.3.6.1.2.1.4.24.4.1
-   1.3.6.1.4.1.89.35.1.13.1.2
-   1.3.6.1.4.1.89.2.12
-   1.3.6.1.4.1.89.2.4
-   1.3.6.1.4.1.89.35.1.40.52.1.1
-   1.3.6.1.4.1.89.35.1.13.1
-   1.3.6.1.4.1.89.35.1.30.1
-   1.3.6.1.2.1.68.1.3.1
-   1.3.6.1.4.1.89.35.1.13.1
-   1.3.6.1.4.1.89.35.1.11.1
-   1.3.6.1.4.1.89.35.1.40.52.1.1

**Parent Topic:**[Prerequisites for performing top-down discovery using Service Mapping](prerequisites-service-mapping.md)

**Related topics**  


[ITOM Content Service reference](../../discovery/reference/itom-content-service-classifiers.md)

