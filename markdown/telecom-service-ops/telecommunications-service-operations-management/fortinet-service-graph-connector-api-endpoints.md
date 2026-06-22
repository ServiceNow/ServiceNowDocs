---
title: Fortinet Service Graph Connector API Endpoints
description: The Service Graph Connector for Fortinet integrates Fortinet Dashboard API data into ServiceNow AI PlatformConfiguration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/fortinet-service-graph-connector-api-endpoints.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Fortinet Service Graph Connector API Endpoints

The Service Graph Connector for Fortinet integrates Fortinet Dashboard API data into ServiceNow AI PlatformConfiguration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.

**Note:** The `meta fields` values in the ADOM and device requests are configurable. Define the meta field names that match your Fortinet deployment. If you don't configure any meta fields, the connector omits the `meta fields` parameter from the request, and Fortinet returns standard data. The values shown in the following examples are sample meta fields and are required for discovery.

<table id="table_akk_j2d_phc"><thead><tr><th>

Description

</th><th>

API response

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
</table>**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

