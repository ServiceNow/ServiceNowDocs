---
title: TISC Intel Exchange API
description: Enables external systems to share threat intelligence data with the Threat Intelligence Security Center \(TISC\) application.Shares threat intelligence data from an external source with the Threat Intelligence Security Center \(TISC\) application.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# TISC Intel Exchange API

Enables external systems to share threat intelligence data with the Threat Intelligence Security Center \(TISC\) application.

This API requires the Threat Intelligence Security Center application, which is available on the ServiceNow Store.

For additional information about TISC, see Threat Intelligence Security Center.

This API runs in the `sn_sec_tisc` namespace. The calling user must have the sn\_sec\_tisc.api\_post\_intel role.

The current version of this API is `v1`.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## TISC Intel Exchange - POST /sn\_sec\_tisc/tisc\_intel\_sharing\_api/post\_intel

Shares threat intelligence data from an external source with the Threat Intelligence Security Center \(TISC\) application.

This endpoint creates an inbound intelligence record, as well as records for indicators, objects, and observables.

Indicator records are created in the Indicator Source \[sn\_sec\_tisc\_indicator\_source\] table.

Object records are created in the following tables that extend Object Source \[sn\_sec\_tisc\_object\_source\].

-   Attack Pattern Source \[sn\_sec\_tisc\_attack\_pattern\_source\]
-   Campaign Source \[sn\_sec\_tisc\_campaign\_source\]
-   Course of Action Source \[sn\_sec\_tisc\_course\_of\_action\_source\]
-   Data Component \[sn\_sec\_tisc\_data\_component\]
-   Data Source \[sn\_sec\_tisc\_data\_source\]
-   Identity Source \[sn\_sec\_tisc\_identity\_source\]
-   Infrastructure Source \[sn\_sec\_tisc\_infrastructure\_source\]
-   Intrusion Set Source \[sn\_sec\_tisc\_intrusion\_set\_source\]
-   Location Source \[sn\_sec\_tisc\_location\_source\]
-   Malware Analysis Source \[sn\_sec\_tisc\_malware\_analysis\_source\]
-   Malware Source \[sn\_sec\_tisc\_malware\_source\]
-   Marking Definition Source \[sn\_sec\_tisc\_marking\_definition\_source\]
-   Object Sighting Source \[sn\_sec\_tisc\_object\_sighting\_source\]
-   Observed Data Source \[sn\_sec\_tisc\_observed\_data\_source\]
-   Threat Actor Source \[sn\_sec\_tisc\_threat\_actor\_source\]
-   Threat Event Source \[sn\_sec\_tisc\_threat\_event\_source\]
-   Threat Grouping Source \[sn\_sec\_tisc\_threat\_grouping\_source\]
-   Threat Note Source \[sn\_sec\_tisc\_threat\_note\_source\]
-   Threat Opinion Source \[sn\_sec\_tisc\_threat\_opinion\_source\]
-   Threat Report Source \[sn\_sec\_tisc\_threat\_report\_source\]
-   Tool Source \[sn\_sec\_tisc\_tool\_source\]
-   Vulnerability Source \[sn\_sec\_tisc\_vulnerability\_source\]

Observable records are created in the following tables that extend Observable Source \[sn\_sec\_tisc\_observable\_source\].

-   Artifact Source \[sn\_sec\_tisc\_artifact\_source\]
-   AS Number Source \[sn\_sec\_tisc\_as\_number\_source\]
-   Directory Source \[sn\_sec\_tisc\_directory\_source\]
-   Domain Name Source \[sn\_sec\_tisc\_domain\_name\_source\]
-   Email Address Source \[sn\_sec\_tisc\_email\_address\_source\]
-   Email Message Source \[sn\_sec\_tisc\_email\_message\_source\]
-   Email Subject Source \[sn\_sec\_tisc\_email\_subject\_source\]
-   File Source \[sn\_sec\_tisc\_file\_source\]
-   IPv4 Address Source \[sn\_sec\_tisc\_ipv4\_address\_source\]
-   IPv4 CIDR Source \[sn\_sec\_tisc\_ipv4\_cidr\_source\]
-   IPv6 Address Source \[sn\_sec\_tisc\_ipv6\_address\_source\]
-   IPv6 CIDR Source \[sn\_sec\_tisc\_ipv6\_cidr\_source\]
-   MAC Address Source \[sn\_sec\_tisc\_mac\_address\_source\]
-   MD5 Hash Source \[sn\_sec\_tisc\_md5\_hash\_source\]
-   Mutex Name Source \[sn\_sec\_tisc\_mutex\_name\_source\]
-   Network Source \[sn\_sec\_tisc\_network\_source\]
-   Other Observable Source \[sn\_sec\_tisc\_other\_observable\_source\]
-   Process Source \[sn\_sec\_tisc\_process\_source\]
-   SHA1 Hash Source \[sn\_sec\_tisc\_sha1\_hash\_source\]
-   SHA256 Hash Source \[sn\_sec\_tisc\_sha256\_hash\_source\]
-   SHA512 Hash Source \[sn\_sec\_tisc\_sha512\_hash\_source\]
-   Software Source \[sn\_sec\_tisc\_software\_source\]
-   URL Source \[sn\_sec\_tisc\_url\_source\]
-   User Account Source \[sn\_sec\_tisc\_user\_account\_source\]
-   Windows Registry Key Source \[sn\_sec\_tisc\_windows\_registry\_key\_source\]
-   X.509 Certificate Source \[sn\_sec\_tisc\_x\_509\_certificate\_source\]

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/tisc_intel_sharing_api/post_intel`

Default URL: `/api/sn_sec_tisc/tisc_intel_sharing_api/post_intel`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|&lt;Object&gt;|[STIX 2.1](https://docs.oasis-open.org/cti/stix/v2.1/os/stix-v2.1-os.html) or MISP payload containing the threat intelligence data to share with TISC. When using MISP, it must be an array of [MISP event payloads](https://www.misp-project.org/openapi/#tag/Events/operation/getEvents).|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Profile-GUID

</td><td>

Unique identifier of the inbound intelligence profile configured in the receiving instance that data is being shared with.To obtain the unique identifier, navigate to the **Administration** tab of **Threat Intelligence Security Center**, then go to **Inbound Intelligence Profiles** and click the profile you want to use. On the profile page, select **Copy Profile ID** or **Email Profile Details**.

</td></tr><tr><td>

Shared-Intel-Format

</td><td>

Format of the data being shared.Possible values:

-   STIX 2.1
-   MISP

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Only supports **application/json**.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. Possible errors:

-   Missing `Shared-Intel-Format` in request header.
-   Missing `Profile-GUID` in request header.
-   `Shared-Intel-Format` header contains unsupported values.
-   `Profile-GUID` header refers to a profile that isn't enabled or doesn't exist.
-   Profile doesn't support intelligence sharing in the format specified by the `Shared-Intel-Format` header.
-   Authenticated user doesn't have permission to submit intelligence to the specified profile.

</td></tr><tr><td>

422

</td><td>

Unprocessable Content. The request body doesn't follow the format specified by the `Shared-Intel-Format` request header.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Error information. This parameter is only returned if the request failed.Data type: Object

```
"error": {
   "message": "String",
   "detail": "String"
}
```

</td></tr><tr><td>

error.message

</td><td>

Error message containing the reason the request failed.Data type: String

</td></tr><tr><td>

error.detail

</td><td>

Additional details about why the request failed.Data type: String

</td></tr><tr><td>

result

</td><td>

Details about the records that were successfully created.```
"result": {
    "createdEntitiesCount": {Object}, 
    "receivedIntelligenceRecord": "String" 
}
```

Data type: Object

</td></tr><tr><td>

result.createdEntitiesCount

</td><td>

Count of each type of created entity.```
"createdEntitiesCount": {
    "indicators": Number,
    "objects": Number,  
    "observables": Number  
}
```

Data type: Object

</td></tr><tr><td>

result.createdEntitiesCount.indicators

</td><td>

Count of created indicators.Data type: Number

</td></tr><tr><td>

result.createdEntitiesCount.objects

</td><td>

Count of created objects.Data type: Number

</td></tr><tr><td>

result.createdEntitiesCount.observables

</td><td>

Count of created observables.Data type: Number

</td></tr><tr><td>

result.receivedIntelligenceRecord

</td><td>

Identification number of the created inbound intelligence record.Data type: String

Table: Inbound Intelligence \[sn\_sec\_tisc\_inbound\_intelligence\]

Column: Number

</td></tr></tbody>
</table>### cURL request

This example creates records for an indicator, object \(malware\), and observable \(domain name\) based on data in STIX 2.1 format.

```

curl "https://instancename.service-now.com/api/sn_sec_tisc/v1/tisc_intel_sharing_api/post_intel" \
  --request POST \
  --header 'Shared-Intel-Format: STIX 2.1' \
  --header 'Profile-GUID: a87febc22b80b210ceeaf5486e91bfdb' \
  --header 'Content-Type: application/json' \
  --user 'username:password' \
  --data '{
    "type": "bundle",
    "objects": [
      {
        "id": "domain-name--4b5f73f2-1bf2-5250-8926-55f0604bcb0c",
        "type": "domain-name",
        "defanged": false,
        "value": "testdomain.com",
        "object_marking_refs": [
          "marking-definition--f88d31f6-486f-44da-b317-01333bde0b82"
        ]
      },
      {
        "id": "indicator--64c35f36-1b32-4250-8926-55f0604bcbaf",
        "type": "indicator",
        "spec_version": "2.1",
        "revoked": false,
        "confidence": 74,
        "object_marking_refs": [
          "marking-definition--f88d31f6-486f-44da-b317-01333bde0b82"
        ],
        "pattern": "[ domain-name:value = 'testdomain.com' ]",
        "name": "Test Indicator",
        "description": "References to this domain are indicative of the presence of the Test malware in the environment",
        "valid_from": "2011-02-11T00:00:00.000Z",
        "kill_chain_phases": [
          {
            "kill_chain_name": "lockheed-martin-cyber-kill-chain",
            "phase_name": "exploit"
          }
        ]
      },
      {
        "id": "malware--1ec31776-1b7a-4610-8f18-cb31604bcb36",
        "type": "malware",
        "spec_version": "2.1",
        "revoked": false,
        "confidence": 60,
        "object_marking_refs": [
          "marking-definition--f88d31f6-486f-44da-b317-01333bde0b82"
        ],
        "name": "Test Malware",
        "description": "Once infected with this malware, a host becomes part of the Test Botnet",
        "is_family": false,
        "last_seen": "2023-06-26T08:04:17.000Z",
        "aliases": [
          "Alias1"
        ],
        "kill_chain_phases": [
          {
            "kill_chain_name": "lockheed-martin-cyber-kill-chain",
            "phase_name": "control"
          }
        ],
        "capabilities": [
          "anti-vm"
        ]
      }
    ]
  }'
```

Response body.

```
{
    "result": {
        "receivedIntelligenceRecord": "IBTI0001001",
        "createdEntitiesCount": {
            "observables": 1.0,
            "indicators": 1.0,
            "objects": 1.0
        }
    }
}
```

### cURL request

This example creates records for objects and observables based on data in MISP format.

```

curl "https://instancename.service-now.com/api/sn_sec_tisc/v1/tisc_intel_sharing_api/post_intel" \
  --request POST \
  --header 'Shared-Intel-Format: MISP' \
  --header 'Profile-GUID: a87febc22b80b210ceeaf5486e91bfdb' \
  --header 'Content-Type: application/json' \
  --user 'username:password' \
  --data '[
    {
      "Event": {
        "id": "134",
        "orgc_id": "3",
        "org_id": "1",
        "date": "2016-03-28",
        "threat_level_id": "3",
        "info": "OSINT - TREASUREHUNT: A CUSTOM POS MALWARE TOOL",
        "published": true,
        "uuid": "56f92df0-24f0-4c6e-a297-6f2402de0b81",
        "attribute_count": "54",
        "analysis": "2",
        "timestamp": "1459171202",
        "distribution": "3",
        "proposal_email_lock": false,
        "locked": false,
        "publish_timestamp": "1727129707",
        "sharing_group_id": "0",
        "disable_correlation": false,
        "extends_uuid": "",
        "protected": null,
        "event_creator_email": "user.name@email.com",
        "Org": {
          "id": "1",
          "name": "ORGNAME",
          "uuid": "ed6dd3f3-f4a9-4109-974c-4b8da8795b96",
          "local": true
        },
        "Orgc": {
          "id": "3",
          "name": "EXAMPLE",
          "uuid": "55f6ea5e-2c60-40e5-964f-47a8950d210f",
          "local": false
        },
        "Attribute": [
          {
            "id": "17426",
            "type": "link",
            "category": "External analysis",
            "to_ids": false,
            "uuid": "56f92e2a-1be0-4a3a-a3b6-3f2a02de0b81",
            "event_id": "134",
            "distribution": "5",
            "timestamp": "1459170858",
            "comment": "",
            "sharing_group_id": "0",
            "deleted": false,
            "disable_correlation": false,
            "object_id": "0",
            "object_relation": null,
            "value": "https://www.example.html",
            "Galaxy": [],
            "ShadowAttribute": []
          },
          {
            "id": "17429",
            "type": "md5",
            "category": "Payload delivery",
            "to_ids": true,
            "uuid": "56f92ea5-2d50-4fc9-92ef-6f2302de0b81",
            "event_id": "134",
            "distribution": "5",
            "timestamp": "1459170981",
            "comment": "TREASUREHUNT 0.1",
            "value": "cec2810556c63e9c225afb6a5ca58bc1",
            "Galaxy": [],
            "ShadowAttribute": []
          },
          {
            "id": "17430",
            "type": "md5",
            "category": "Payload delivery",
            "to_ids": true,
            "uuid": "56f92ea6-2890-41b3-8059-6f2302de0b81",
            "event_id": "134",
            "distribution": "5",
            "timestamp": "1459170982",
            "comment": "TREASUREHUNT 0.1",
            "value": "cb75de605c171e36c8a593e337275d8f",
            "Galaxy": [],
            "ShadowAttribute": []
          },
          {
            "id": "17431",
            "type": "md5",
            "category": "Payload delivery",
            "to_ids": true,
            "uuid": "56f92ea6-009c-4348-a0b2-6f2302de0b81",
            "event_id": "134",
            "distribution": "5",
            "timestamp": "1459170982",
            "comment": "TREASUREHUNT 0.1",
            "value": "6a9348f582b2e121a5d9bff1e8f0935f",
            "Galaxy": [],
            "ShadowAttribute": []
          }
        ],
        "Tag": [
          {
            "id": "35",
            "name": "tlp:white",
            "colour": "#ffffff",
            "exportable": true
          }
        ]
      }
    },
    {
      "Event": {
        "id": "646",
        "orgc_id": "3",
        "org_id": "1",
        "date": "2017-03-10",
        "threat_level_id": "2",
        "info": "OSINT - Wikileaks Vault7 JQJSNICKER code leak",
        "published": true,
        "uuid": "58c2fcf1-283c-45fa-b289-45ae02de0b81",
        "attribute_count": "14",
        "analysis": "2",
        "timestamp": "1489174168",
        "distribution": "3",
        "event_creator_email": "user.name@example.com",
        "Org": {
          "id": "1",
          "name": "ORGNAME",
          "uuid": "ed6dd3f3-f4a9-4109-974c-4b8da8795b96",
          "local": true
        },
        "Orgc": {
          "id": "3",
          "name": "CIRCL",
          "uuid": "55f6ea5e-2c60-40e5-964f-47a8950d210f",
          "local": false
        },
        "Attribute": [
          {
            "id": "140266",
            "type": "link",
            "category": "External analysis",
            "to_ids": false,
            "uuid": "58c2fd63-b1a4-4f74-aa79-41a602de0b81",
            "value": "http://example.com/",
            "Tag": [
              {
                "id": "35",
                "name": "tlp:white",
                "colour": "#ffffff"
              }
            ]
          },
          {
            "id": "140268",
            "type": "filename|sha1",
            "category": "Payload delivery",
            "to_ids": true,
            "uuid": "58c2fdc4-e6d8-4f6e-9eb5-4dbb02de0b81",
            "comment": "JQJSNICKER",
            "value": "Installer.dll.embedded.core.dll.file|02aa4d3712f324aa4b125056b52a5200691eb62b"
          },
          {
            "id": "140269",
            "type": "filename|sha256",
            "category": "Payload delivery",
            "to_ids": true,
            "uuid": "58c2fdc6-5064-49be-b39a-429402de0b81",
            "comment": "JQJSNICKER",
            "value": "Installer.dll.embedded.core.dll.file|ea042bd3a7df11273e233c423e9740e6b51001911139855ef39501472a1e5fb0"
          }
        ],
        "Tag": [
          {
            "id": "35",
            "name": "tlp:white",
            "colour": "#ffffff"
          }
        ]
      }
    }
  ]'
```

Response body.

```
{
    "result": {
        "receivedIntelligenceRecord": "IBTI0001005",
        "createdEntitiesCount": {
            "observables": 9,
            "indicators": 0,
            "objects": 2
        }
    }
}
```

