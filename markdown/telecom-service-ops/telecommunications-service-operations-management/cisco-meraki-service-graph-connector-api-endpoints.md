---
title: Cisco Meraki Service Graph Connector API Endpoints
description: The Service Graph Connector for Meraki integrates Cisco Meraki Dashboard API data into ServiceNow AI PlatformConfiguration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Cisco Meraki Service Graph Connector API Endpoints

The Service Graph Connector for Meraki integrates Cisco Meraki Dashboard API data into ServiceNow AI Platform®Configuration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.

<table><thead><tr><th>

Description

</th><th>

API response

</th></tr></thead><tbody><tr><td>

Organizations API response`URL:/organizations`

</td><td>

```json
{                                                                    │
│    "id": "123456",                                                    │
│    "name": "My Organization",                                         │
│    "management": {                                                    │
│      "details": {                                                     │
│        "MSP ID": "...",                                               │
│        "customer number": "...",                                      │
│        "IP restriction mode for API": "..."                           │
│      }                                                                │
│    }                                                                  │
│  }              
```

</td></tr></tbody>
</table><table><thead><tr><th>

Description

</th><th>

Endpoint

</th></tr></thead><tbody><tr><td>

Networks API response`URL:/organizations/{orgId}/networks`

</td><td>

```json
{                                                                    │
│    "id": "N_123456",                                                  │
│    "organizationId": "123456",                                        │
│    "name": "My Network",                                              │
│    "notes": "Network description"                                     │
│  } 
```

</td></tr></tbody>
</table><table><thead><tr><th>

Description

</th><th>

Endpoint

</th></tr></thead><tbody><tr><td>

Devices API response`URL: /organizations/{orgId}/devices`

</td><td>

```json
{                                                                    │
│    "serial": "Q2XX-XXXX-XXXX",                                        │
│    "name": "My Device",                                               │
│    "networkId": "N_123456",                                           │
│    "model": "MX68",                                                   │
│    "mac": "00:11:22:33:44:55",                                        │
│    "productType": "appliance",                                        │
│    "firmware": "mx-18.1",                                             │
│    "lat": 37.7749,                                                    │
│    "lng": -122.4194,                                                  │
│    "address": "123 Main St",                                          │
│    "notes": "Device description"                                      │
│  }        
```

</td></tr></tbody>
</table><table><thead><tr><th>

Description

</th><th>

Endpoint

</th></tr></thead><tbody><tr><td>

Devices statuses API response`URL: /organizations/{orgId}/devices/statuses`

</td><td>

```json
{                                                                    │
│    "serial": "Q2XX-XXXX-XXXX",                                        │
│    "status": "online",                                                │
│    "publicIp": "203.0.113.1",                                         │
│    "wan1Ip": "192.168.1.1",                                           │
│    "wan2Ip": "192.168.2.1",                                           │
│    "wan1Gateway": "192.168.1.254",                                    │
│    "wan1IpType": "dhcp",                                              │
│    "wan1PrimaryDns": "8.8.8.8",                                       │
│    "wan1SecondaryDns": "8.8.4.4"                                      │
│  }         
```

</td></tr></tbody>
</table><table><thead><tr><th>

Description

</th><th>

Endpoint

</th></tr></thead><tbody><tr><td>

Uplink statuses endpoint`URL: /organizations/{orgId}/uplinks/statuses`

</td><td>

```json
{                                                                    │
│    "serial": "Q2XX-XXXX-XXXX",                                        │
│    "networkId": "N_123456",                                           │
│    "model": "MX68",                                                   │
│    "highAvailability": {                                              │
│      "enabled": true,                                                 │
│      "role": "primary"                                                │
│    },                                                                 │
│    "uplinks": [                                                       │
│      {                                                                │
│        "interface": "wan1",                                           │
│        "status": "active",                                            │
│        "ip": "192.168.1.1",                                           │
│        "gateway": "192.168.1.254",                                    │
│        "publicIp": "203.0.113.1",                                     │
│        "primaryDns": "8.8.8.8",                                       │
│        "secondaryDns": "8.8.4.4",                                     │
│        "ipAssignedBy": "dhcp"                                         │
│      },                                                               │
│      {                                                                │
│        "interface": "cellular",                                       │
│        "status": "ready",                                             │
│        "apn": "broadband",                                            │
│        "iccid": "...",                                                │
│        "imsi": "...",                                                 │
│        "msisdn": "..."                                                │
│      }                                                                │
│    ]                                                                  │
│  }    
```

</td></tr></tbody>
</table><table><thead><tr><th>

Description

</th><th>

Endpoint

</th></tr></thead><tbody><tr><td>

Switch ports endpoint`URL: /organizations/{orgId}/switch/ports/statuses/bySwitch`

</td><td>

```json
{                                                                    │
│    "items": [                                                         │
│      {                                                                │
│        "serial": "Q2XX-XXXX-XXXX",                                    │
│        "network": { "id": "N_123456" },                               │
│        "ports": [                                                     │
│          {                                                            │
│            "portId": "1",                                             │
│            "status": "connected"                                      │
│          },                                                           │
│          {                                                            │
│            "portId": "2",                                             │
│            "status": "disconnected"                                   │
│          }                                                            │
│        ]                                                              │
│      }                                                                │
│    ]                                                                  │
│  }  
```

</td></tr></tbody>
</table><table id="table_lg2_svs_5hc"><thead><tr><th>

Description

</th><th>

Endpoint

</th></tr></thead><tbody><tr><td>

Device inventory endpoint`URL: /organizations/{orgId}/inventory/devices`

</td><td>

```json
 {                                                                    │
│    "serial": "Q2XX-XXXX-XXXX",                                        │
│    "orderNumber": "ORD-12345",                                        │
│    "licenseExpirationDate": "2025-12-31"                              │
│  }  
```

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Service Operations Management reference](components-installed-with-tsom.md)

