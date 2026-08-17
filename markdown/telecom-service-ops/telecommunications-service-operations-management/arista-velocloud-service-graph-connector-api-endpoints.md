---
title: Arista VeloCloud Service Graph Connector API Endpoints
description: The Service Graph Connector for Arista VeloCloud integrates VeloCloud Orchestrator API data into ServiceNow AI Platform Configuration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/arista-velocloud-service-graph-connector-api-endpoints.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: reference
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Service Operations Management]
---

# Arista VeloCloud Service Graph Connector API Endpoints

The Service Graph Connector for Arista VeloCloud integrates VeloCloud Orchestrator API data into ServiceNow AI Platform Configuration Management Database \(CMDB\). This document details the API endpoints used and how data flows through the system.

<table id="table_akk_j2d_phc"><thead><tr><th>

Description

</th><th>

API response

</th></tr></thead><tbody><tr><td>

MSP details`URL:/portal/rest/enterpriseProxy/getEnterpriseProxy`

</td><td>

```json
{
  "id": 1,
  "created": "2020-02-25T14:13:13.000Z",
  "networkId": 1,
  "proxyType": "MSP",
  "operateGateways": 1,
  "logicalId": "084265a7-96dd-4dd4-9e9f-d8e924850663",
  "name": "Vodafone Group POC",
  "domain": "VFGroupPoc",
  "contactName": "Samsul Arefin",
  "contactPhone": "+1",
  "contactMobile": "+44",
  "contactEmail": "samsul.arefin@vodafone.com",
  "streetAddress": "",
  "streetAddress2": "The Connection",
  "city": "Newbury",
  "state": "Berkshire",
  "postalCode": "RG14 2FN",
  "country": "United Kingdom",
  "lat": 37.402866,
  "lon": -122.117332,
  "modified": "2024-11-21T14:32:30.000Z"
}
```

</td></tr><tr><td>

Gateway pools and details`URL:/portal/rest/enterpriseProxy/getEnterpriseProxyGatewayPools`

</td><td>

```json

[
  {
    "id": 2,
    "networkId": 1,
    "logicalId": "4f19ad54-06b7-11ec-b96c-026628323786",
    "name": "Vodafone VCC Pool 1",
    "gateways": [],
    "enterprises": []
  }
]
```

</td></tr><tr><td>

Enterprises`URL:/portal/rest/enterpriseProxy/getEnterpriseProxyEnterprises`

</td><td>

```json
[
  {
    "id": 1,
    "created": "2020-03-05T14:56:45.000Z",
    "networkId": 1,
    "gatewayPoolId": 2,
    "alertsEnabled": 1,
    "operatorAlertsEnabled": 1,
    "endpointPkiMode": "CERTIFICATE_DISABLED",
    "name": "UseCase1",
    "domain": "domain-test",
    "logicalId": "135c30c3-90a7-499c-b778-942794c205e5",
    "accountNumber": "WAT-4N6RVGN",
    "modified": "2025-05-29T14:51:03.000Z"
  }
]
```

</td></tr><tr><td>

Network enterprises \(Operator mode\)`URL:/portal/rest/network/getNetworkEnterprises`

</td><td>

```json
[
  {
    "id": 43,
    "created": "2019-03-11T13:38:01.000Z",
    "networkId": 1,
    "gatewayPoolId": 3,
    "alertsEnabled": 1,
    "operatorAlertsEnabled": 1,
    "endpointPkiMode": "CERTIFICATE_REQUIRED",
    "name": "DAWN WING/TIME FREIGHT",
    "domain": null,
    "prefix": null,
    "logicalId": "550b0770-23ce-4884-889c-fadb21d72acb",
    "accountNumber": "DAW-WIN-5EQ",
    "description": null,
    "contactName": null,
    "contactPhone": null,
    "contactMobile": null,
    "contactEmail": null,
    "streetAddress": null,
    "streetAddress2": null,
    "city": null,
    "state": null,
    "postalCode": null,
    "country": null,
    "lat": 37.402866,
    "lon": -122.117332,
    "timezone": "America/Los_Angeles",
    "locale": "en-US",
    "bastionState": "UNCONFIGURED",
    "modified": "2022-08-18T18:14:09.000Z",
    "enterpriseProxyId": 11,
    "enterpriseProxyName": "DAWN WING"
  }
]
```

</td></tr><tr><td>

Edges`URL:/portal/rest/enterprise/getEnterpriseEdges`

</td><td>

```json
[
  {
    "id": 4523,
    "enterpriseId": 1552,
    "logicalId": "2b16c0a6-1d22-4a2f-861d-3994e43f7982",
    "name": "610-05-08",
    "serialNumber": "2937V43",
    "modelNumber": "edge610-lte",
    "edgeState": "OFFLINE"
  }
]
```

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Service Operations Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/components-installed-with-tsom.md)

