---
title: IBM WebSphere DataPower discovery
description: ITOM Visibility discovers IBM WebSphere DataPower. The Discovery feature uses the DataPower Server pattern for horizontal discovery. The Service Mapping feature uses the DataPower pattern for top-down discovery.
locale: en-US
release: zurich
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Network device discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# IBM WebSphere DataPower discovery

ITOM Visibility discovers IBM WebSphere DataPower. The Discovery feature uses the DataPower Server pattern for horizontal discovery. The Service Mapping feature uses the DataPower pattern for top-down discovery.

## Prerequisites

Configure the following credentials before discovering the IBM WebSphere DataPower devices:

-   **[SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    SNMP credentials are necessary for using the following SNMP queries:

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
-   **[Applicative credentials](https://www.servicenow.com/docs/access?context=applicative-creds&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Together with SNMP credentials, applicative credentials are required to discover DataPower application domains, otherwise known as logical CIs.

    In addition, SNMP and applicative credentials are used for top-down discovery of applicative relationships \(corresponding application DataPower domain\).

-   **User with permissions to run SOAP**

    Permissions to run SOAP queries are necessary for top-down discovery of the DataPower Web Service and MQ connection.


## Data collected by Discovery during horizontal discovery

By default, Discovery uses the DataPower Server pattern to perform the discovery.

**Note:** For information on Probe to Pattern migration see the knowledge article [KB0694477](https://support.servicenow.com/kb_view.do?sysparm_article=KB0694477).

|Table and field|Description|
|---------------|-----------|
|Data Power Hosting Server \[cmdb\_ci\_datapower\_server\]|
|Model number \[model\_number\]|The model of the server hosting the WebSphere DataPower.|
|Host name \[host\_name\]|The host name of the server hosting the WebSphere DataPower.|
|Serial number \[serial\_number\]|The serial number of the server hosting the WebSphere DataPower.|
|IP Address \[cmdb\_ci\_ip\_address\]|
|IP Address \[ip\_address\]|The IP address of the server hosting the WebSphere DataPower.|
|Netmask \[netmask\]|The netmask of the server hosting the WebSphere DataPower.|
|Network Adapters \[cmdb\_ci\_network\_adapter\]|
|MAC address \[mac\_address\]|The MAC address of the network adapter.|
|Name \[name\]|The name of the network adapter.|

## CI Relationships

|CI|Relationship/Reference|CI|
|---|----------------------|---|
|Data Power Hosting Server \[cmdb\_ci\_datapower\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|Network Adapters \[cmdb\_ci\_network\_adapter\]|Owns::Owned by|Data Power Hosting Server \[cmdb\_ci\_datapower\_server\]|

## Data collected by Service Mapping during top-down discovery

|Table and field|Description|
|---------------|-----------|
|Data Power \[cmdb\_ci\_app\_server\_datapower\]|
|Host name \[host\_name\]|The attributes of the DataPower application.|
|SOAP URL \[soap\_url\]|
|Version \[version\]|
|IP address \[ip\_address\]|
|Name \[name\]|
|Domain \[domain\]|

**Parent Topic:**[Network device discovery](../concept/c_NetworkDevices.md)

