---
title: Fortinet Service Graph Connector API Endpoints
description: The Service Graph Connector for Fortinet integrates Fortinet Dashboard API data into ServiceNow AI PlatformConfiguration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Fortinet Service Graph Connector API Endpoints

The Service Graph Connector for Fortinet integrates Fortinet Dashboard API data into ServiceNow AI Platform®Configuration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.

<table id="table_akk_j2d_phc"><thead><tr><th>

Example description

</th><th>

Example schema values

</th></tr></thead><tbody><tr><td>

Authenticate JSON-RPC session

</td><td>

```json
{ "method": "exec", "params": [ { "url": "/sys/login/user", "data": { "user": "user", "passwd": "abc1123" } } ], "verbose": 1 }
```

</td></tr><tr><td>

Logout JSON-RPC session

</td><td>

```json
{ "method": "exec", "params": [ { "url": "/sys/logout" } ], "verbose": 1, "session": "TxMw/zbjw+tVZ/JL3bhmYg0vTUpVguYHIQesJXpye4j2vvsqtZaSgKWa+0iLqug+3/074jq8QqmI/KOx4GHkwQ==" }
```

</td></tr><tr><td>

GET ADOMs

</td><td>

```json
{ "method": "get", "params": [ { "url": "/dvmdb/adom", "meta fields": [ "VF SDWAN Service Provided", "VF OpCo Name", "VF Customer ID", "SERVICE_ID", "SDN_MS" ] } ], "verbose": 1, "session": "TxMw/zbjw+tVZ/JL3bhmYg0vTUpVguYHIQesJXpye4j2vvsqtZaSgKWa+0iLqug+3/074jq8QqmI/KOx4GHkwQ==" }
```

</td></tr><tr><td>

GET ADOM devices

</td><td>

```json
{ "method": "get", "params": [ { "url": "/dvmdb/adom/{ADOM_NAME}/device", "meta fields": [ "Company/Organization", "VF 3C Ref", "Address", "Contact Email", "Contact Phone Number", "VF Order Ref" ] } ], "verbose": 1, "session": "TxMw/zbjw+tVZ/JL3bhmYg0vTUpVguYHIQesJXpye4j2vvsqtZaSgKWa+0iLqug+3/074jq8QqmI/KOx4GHkwQ==" }
```

</td></tr><tr><td>

GET interfaces by device name

</td><td>

```json
{ "method": "get", "params": [ { "url": "/dbcache/system/interface", "option": [ "scope member" ], "scope member": [ { "name": "{DEVICE_NAME}", "vdom": "global" } ], "fields": [ "name", "alias", "comments", "speed", "mediatype", "ip", "mode", "type", "mtu", "interface", "vlanid", "member", "vdom", "role", "allowaccess", "zone", "mac", "status" ], "current_adom": "{ADOM_NAME}" } ], "verbose": 1, "session": "TxMw/zbjw+tVZ/JL3bhmYg0vTUpVguYHIQesJXpye4j2vvsqtZaSgKWa+0iLqug+3/074jq8QqmI/KOx4GHkwQ==" }
```

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Service Operations Management reference](components-installed-with-tsom.md)

