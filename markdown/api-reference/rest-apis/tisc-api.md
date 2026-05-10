---
title: TISC API
description: The TISC API provides endpoints to add and retrieve threat intelligence data in the Threat Intelligence Security Center \(TISC\) application.Adds observable source records to the Threat Intelligence Security Center \(TISC\) application.Retrieves observables data, including relationships between observables and other threat intelligence data such as Structured Threat Information Expression \(STIX\) objects.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 24
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# TISC API

The TISC API provides endpoints to add and retrieve threat intelligence data in the Threat Intelligence Security Center \(TISC\) application.

Data retrieved by this API can be used by other security tools such as Security Information Event Management \(SIEM\) systems. SIEM systems can integrate with TISC using this API to retrieve observables related to threats in TISC and automatically detect and monitor these threats within an organization’s network. This API enables bidirectional sharing of observables from security tools. SIEM systems observe anomalous activity in the environment and can provide a list of observables associated with the anomalous activity to TISC.

This API can also be used to enrich SIEM alerts with threat intelligence context. For example, if a SIEM alert is generated based on unusually high traffic from an IP address, TISC can provide additional information such as whether the IP address or domain involved is linked to known malicious activities. This enrichment data enables security analysts to triage the alerts and use the contextual information for efficient remediation.

This API requires the Threat Intelligence Security Center application, which is available on the ServiceNow Store.

For additional information about TISC, see [Threat Intelligence Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-landing-page.md).

This API runs in the `sn_sec_tisc` namespace.

The current version of this API is `v1`.

For information about API authentication, see the REST API security section in [REST APIs](c_RESTAPI.md).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## TISC API - POST /sn\_sec\_tisc/threat\_intel\_data/add\_observables

Adds observable source records to the Threat Intelligence Security Center \(TISC\) application.

The [observable source records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-observables-source-records.md) are created in the Observable Source \[sn\_sec\_tisc\_observable\_source\] table and are processed through de-duplication and aggregation in the [TISC data flow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-data-processing-functional-flow.md).

**Note:** Observable source records can't be directly updated using this endpoint. Only new records can be created. Therefore, even if only a few fields require an update, all fields must still be included in the request.

To access this endpoint, the caller must have the sn\_sec\_tisc.api\_obs\_write\_access role, which by default is included in the Threat Intelligence administrator role \(sn\_sec\_tisc.admin\).

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/threat_intel_data/add_observables`

Default URL: `/api/sn_sec_tisc/threat_intel_data/add_observables`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

observables

</td><td>

Required. List of observable objects to add to TISC. For each observable object, an observable source record is created if all validations are passed, with the source as defined by the **source** parameter in the request body.Data type: Array of Objects

```
"observables": [
   {
      "attributes": {Object},
      "<field>": "String"
   }
]
```

</td></tr><tr><td>

observables.attributes

</td><td>

Field-value pairs containing attribute data about the observable. Attributes are specific to an observable type, such as the AS number for an IP address or the socket type for a network. All attributes for all observable types are supported. For a complete list of valid attributes, see the Observable attributes section below.

Data type: Object

```
"attributes": {
   "<field>": "<value>"
}
```

</td></tr><tr><td>

observables.&lt;field&gt;

</td><td>

Name-value pairs containing general data about the observable. The fields that can be provided in this parameter are common to all observable types.The **type** and **value** fields are required for all observables.

**Note:** Follow these guidelines for providing values:

-   All dates must be in ISO format in the UTC timezone.
-   Some fields require values from a specified table or have a list of possible values. If invalid values are provided for these fields, the observable source record is still created but the invalid values are skipped.

Valid fields:

-   **additional\_context**

Additional context about the observable.

-   **attack\_phases**

List of attack phase names as a comma separated value. For a complete list of valid attack phases, see the **Kill Chain Phase Name** field in the Kill Chain Phase \[sn\_sec\_tisc\_kill\_chain\_phase\] table.

For example:

    ```
"attack_phases": "Lockheed Martin: Reconnaissance,Lockheed Martin: Installation"
    ```

-   **author**

Author for the observable.

-   **confidence**

The confidence that the source system has in the correctness of the observable data. Must be a number from 0–100.

-   **description**

Description of the observable.

-   **expiration\_time**

Expiration date of the observable record.

-   **external\_source\_id**

External ID of the observable from the source system.

-   **first\_observed**

Date the data was first seen.

-   **first\_seen**

Date this observable was first seen performing malicious activities.

-   **last\_observed**

Date the data was last seen.

-   **last\_seen**

Date this observable was last seen performing malicious activities.

-   **notes**

Any additional notes for the observable. Can be formatted as HTML.

-   **reputation**

Reputation of the observable.

Possible values:

    -   clear
    -   malicious
    -   suspicious
    -   unknown
-   **source\_reported\_score**

Maliciousness score of the observable reported by the source system. Must be a number from 0–100.

-   **tags**

List of tags as a comma-separated value. For a complete list of valid tags, see the **Name** field in the Tag \[sn\_sec\_tisc\_tag\] table. If the provided tag doesn’t exist, the tag is automatically created and associated with the observable.

-   **taxonomies**

List of taxonomies as a comma-separated value. For a complete list of valid taxonomies, see the **Taxonomy Value** field in the Taxonomy Value \[sn\_sec\_tisc\_taxonomy\_value\] table.

-   **threat\_level**

Threat level of the observable.

Possible values:

    -   low
    -   medium
    -   high
-   **threat\_severity**

Threat severity of the observable.

Possible values:

    -   low
    -   medium
    -   high
    -   critical
-   **tlp**

Data sensitivity level for the observable using the traffic light protocol \(TLP\).

Possible values:

    -   CLEAR
    -   GREEN
    -   AMBER
    -   AMBER+STRICT
    -   RED
Table: In the Label field in the TLP Label \[sn\_sec\_tisc\_tlp\_label\] table.

-   **type**

Required. Type of observable.

For a complete list of valid observable types, see the **Value** field in the Observable Type \[sn\_sec\_tisc\_observable\_type\] table, or the Observable attributes section below.

-   **usage\_categories**

List of usage categories as a comma-separated value. For a complete list of valid usage categories, see the **Usage Category** field in the Usage Category \[sn\_sec\_tisc\_usage\_category\] table.

-   **value**

Required. Value associated with the observable, such as an IP address or URL.


Data type: String

Table: Observable Source \[sn\_sec\_tisc\_observable\_source\]

</td></tr><tr><td>

source

</td><td>

Required. Source that originally detected the observables, such as a SIEM system.The source is used for all observables listed in the API request.

Data type: String

Stored in: Sources provided in the request body are added to the API Integration \[sn\_sec\_tisc\_api\_integration\] table.

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_gcj_124_xbc"><thead><tr><th>

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

Bad request. The request parameters are invalid or the request body JSON has a syntactical error.To view details about the error, see the **error** parameter in the response body.

</td></tr><tr><td>

401

</td><td>

Unauthorized. The user authentication is invalid. Check the user name and password or OAuth token.

</td></tr><tr><td>

403

</td><td>

Forbidden. The calling user is missing a required role. The sn\_sec\_tisc.api\_obs\_write\_access role is required to access this endpoint.

</td></tr><tr><td>

429

</td><td>

Too many requests. The number of API requests exceeds the rate limit for the API. By default, the limit is 100 requests per hour.

</td></tr><tr><td>

500

</td><td>

Internal server error. Check application logs in the Log \[syslog\] table for more information about the error.

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

error\_records

</td><td>

Details about the observables included in the request that couldn't be added to TISC.Data type: Array of Objects

```
"error_records": [
  {
    "error_message": "String",
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

error\_records.error\_message

</td><td>

Error message that explains why a record couldn't be created for the observable.Data type: String

</td></tr><tr><td>

error\_records.type

</td><td>

Type of observable.For a complete list of valid observable types, see the **Value** field in the Observable Type \[sn\_sec\_tisc\_observable\_type\] table, or the Observable attributes section below.

Data type: String

</td></tr><tr><td>

error\_records.value

</td><td>

Value associated with the observable, such as an IP address or URL.Data type: String

</td></tr><tr><td>

metadata

</td><td>

Metadata about the number of records created by the API request. ```
"metadata": {
  "error_records": Number,
  "success_records": Number,
  "total_records": Number
}
```

Data type: Object

</td></tr><tr><td>

metadata.error\_records

</td><td>

Number of observables included in the request that couldn't be added to TISC.Data type: Number

</td></tr><tr><td>

metadata.success\_records

</td><td>

Number of observable records that were successfully created in TISC.Data type: Number

</td></tr><tr><td>

metadata.total\_records

</td><td>

Total number of observables included in the request.Data type: Number

</td></tr><tr><td>

status

</td><td>

Status of the API request.Possible values:

-   `error`: No observables successfully added to TISC.
-   `failure`: The request failed due to a bad request or system error. See the **error** parameter in the response body for more information about the error.
-   `partial_success`: Some observables successfully added to TISC.
-   `success`: All observables successfully added to TISC.

Data type: String

</td></tr><tr><td>

success\_records

</td><td>

Details about the observable records that were successfully created.Data type: Array of Objects

```
"success_records": [
  {
    "sys_id": "String",
    "type": "String",
    "value": "String"
  }
]
```

</td></tr><tr><td>

success\_records.sys\_id

</td><td>

Sys\_id of the observable record.Data type: String

</td></tr><tr><td>

success\_records.type

</td><td>

Type of observable. For a complete list of valid observable types, see the **Value** field in the Observable Type \[sn\_sec\_tisc\_observable\_type\] table, or the Observable attributes section below.

Data type: String

</td></tr><tr><td>

success\_records.value

</td><td>

Value associated with the observable, such as an IP address or URL.Data type: String

</td></tr></tbody>
</table>### Observable attributes

The following table lists valid attributes for each observable type.

**Note:** All dates must be in ISO format in the UTC timezone.

<table id="table_tfq_rbn_zbc"><thead><tr><th>

Observable type

</th><th>

Attributes

</th><th>

Data type

</th></tr></thead><tbody><tr><td rowspan="8">

artifact

</td><td>

decryption\_key

</td><td>

String

</td></tr><tr><td>

encryption\_algorithm

</td><td>

String

</td></tr><tr><td>

md5\_hash

</td><td>

String

</td></tr><tr><td>

mime\_type

</td><td>

String

</td></tr><tr><td>

sha1\_hash

</td><td>

String

</td></tr><tr><td>

sha256\_hash

</td><td>

String

</td></tr><tr><td>

sha512\_hash

</td><td>

String

</td></tr><tr><td>

url

</td><td>

String

</td></tr><tr><td rowspan="2">

autonomous\_system\_number

</td><td>

name

</td><td>

String

</td></tr><tr><td>

rir

</td><td>

String

</td></tr><tr><td rowspan="4">

directory

</td><td>

directory\_creation\_time

</td><td>

Date

</td></tr><tr><td>

directory\_last\_accessed\_time

</td><td>

Date

</td></tr><tr><td>

directory\_last\_modified\_time

</td><td>

Date

</td></tr><tr><td>

encoded\_path

</td><td>

String

</td></tr><tr><td rowspan="2">

domain\_name

</td><td>

is\_fqdn\(Fully qualified domain name\)

</td><td>

Boolean

</td></tr><tr><td>

resolves\_to

</td><td>

String

</td></tr><tr><td>

email\_address

</td><td>

display\_name

</td><td>

String

</td></tr><tr><td rowspan="7">

email\_message

</td><td>

email\_body

</td><td>

String

</td></tr><tr><td>

email\_recipients\_bcc

</td><td>

String

</td></tr><tr><td>

email\_recipients\_cc

</td><td>

String

</td></tr><tr><td>

email\_recipients\_to

</td><td>

String

</td></tr><tr><td>

email\_sender

</td><td>

String

</td></tr><tr><td>

email\_subject

</td><td>

String

</td></tr><tr><td>

sent\_date

</td><td>

Date

</td></tr><tr><td>

email\_subject

</td><td>

None

</td><td>

 

</td></tr><tr><td rowspan="11">

file

</td><td>

encoded\_file\_name

</td><td>

String

</td></tr><tr><td>

file\_created\_time

</td><td>

Date

</td></tr><tr><td>

file\_last\_accessed\_time

</td><td>

Date

</td></tr><tr><td>

file\_last\_modified\_time

</td><td>

Date

</td></tr><tr><td>

file\_name

</td><td>

String

</td></tr><tr><td>

magic\_number

</td><td>

String

</td></tr><tr><td>

md5\_hash

</td><td>

String

</td></tr><tr><td>

mime\_type

</td><td>

String

</td></tr><tr><td>

sha1\_hash

</td><td>

String

</td></tr><tr><td>

sha256\_hash

</td><td>

String

</td></tr><tr><td>

sha512\_hash

</td><td>

String

</td></tr><tr><td rowspan="2">

ip\_v4\_address

</td><td>

as\_number

</td><td>

String

</td></tr><tr><td>

mac\_address

</td><td>

String

</td></tr><tr><td rowspan="2">

ip\_v4\_cidr

</td><td>

as\_number

</td><td>

String

</td></tr><tr><td>

mac\_address

</td><td>

String

</td></tr><tr><td rowspan="2">

ip\_v6\_address

</td><td>

as\_number

</td><td>

String

</td></tr><tr><td>

mac\_address

</td><td>

String

</td></tr><tr><td rowspan="2">

ip\_v6\_cidr

</td><td>

as\_number

</td><td>

String

</td></tr><tr><td>

mac\_address

</td><td>

String

</td></tr><tr><td>

mac\_address

</td><td>

None

</td><td>

 

</td></tr><tr><td>

md5\_hash

</td><td>

None

</td><td>

 

</td></tr><tr><td>

mutex\_name

</td><td>

None

</td><td>

 

</td></tr><tr><td rowspan="28">

network

</td><td>

destination\_bytes\_count

</td><td>

Integer

</td></tr><tr><td>

destination\_packets\_count

</td><td>

Integer

</td></tr><tr><td>

destination\_port

</td><td>

 

</td></tr><tr><td>

end\_time

</td><td>

Date

</td></tr><tr><td>

http\_message\_body\_length

</td><td>

Integer

</td></tr><tr><td>

http\_request\_header

</td><td>

String

</td></tr><tr><td>

http\_request\_method

</td><td>

String

</td></tr><tr><td>

http\_request\_value

</td><td>

String

</td></tr><tr><td>

http\_request\_version

</td><td>

String

</td></tr><tr><td>

network\_source

</td><td>

String

</td></tr><tr><td>

network\_destination

</td><td>

String

</td></tr><tr><td>

icmp\_code\_byte

</td><td>

String

</td></tr><tr><td>

icmp\_type\_byte

</td><td>

String

</td></tr><tr><td>

is\_network\_active

</td><td>

Boolean

</td></tr><tr><td>

is\_socket\_blocking

</td><td>

Boolean

</td></tr><tr><td>

is\_socket\_listening

</td><td>

Boolean

</td></tr><tr><td>

network\_protocols

</td><td>

String

</td></tr><tr><td>

socket\_address\_family

</td><td>

StringPossible values:

-   af\_unspec
-   af\_inet
-   af\_ipx
-   af\_appletalk
-   af\_netbios
-   af\_inet6
-   af\_irda
-   af\_bth

</td></tr><tr><td>

socket\_descriptor

</td><td>

Integer

</td></tr><tr><td>

socket\_handle

</td><td>

Integer

</td></tr><tr><td>

socket\_options

</td><td>

String

</td></tr><tr><td>

socket\_type

</td><td>

StringPossible values:

-   service\_kernel\_driver
-   service\_file\_system\_driver
-   service\_win32\_own\_process
-   service\_win32\_share\_process

</td></tr><tr><td>

source\_bytes\_count

</td><td>

Integer

</td></tr><tr><td>

source\_packets\_count

</td><td>

Integer

</td></tr><tr><td>

source\_port

</td><td>

String

</td></tr><tr><td>

start\_time

</td><td>

Date

</td></tr><tr><td>

tcp\_destination\_flags

</td><td>

String

</td></tr><tr><td>

tcp\_source\_flags

</td><td>

String

</td></tr><tr><td>

other

</td><td>

None

</td><td>

 

</td></tr><tr><td rowspan="20">

process

</td><td>

aslr\_enabled

</td><td>

Boolean

</td></tr><tr><td>

command\_line

</td><td>

String

</td></tr><tr><td>

cwd\(Current Working Directory\)

</td><td>

String

</td></tr><tr><td>

dep\_enabled

</td><td>

Boolean

</td></tr><tr><td>

environment\_variables

</td><td>

String

</td></tr><tr><td>

is\_hidden

</td><td>

Boolean

</td></tr><tr><td>

owner\_sid

</td><td>

String

</td></tr><tr><td>

pid\(Process ID\)

</td><td>

String

</td></tr><tr><td>

priority

</td><td>

String

</td></tr><tr><td>

process\_created\_time

</td><td>

Date

</td></tr><tr><td>

service\_descriptions

</td><td>

String

</td></tr><tr><td>

service\_display\_name

</td><td>

String

</td></tr><tr><td>

service\_group\_name

</td><td>

String

</td></tr><tr><td>

service\_name

</td><td>

String

</td></tr><tr><td>

service\_start\_type

</td><td>

StringPossible values:

-   service\_auto\_start
-   service\_boot\_start
-   service\_demand\_start
-   service\_disabled
-   service\_system\_alert

</td></tr><tr><td>

service\_status

</td><td>

StringPossible values:

-   service\_continue\_pending
-   service\_pause\_pending
-   service\_paused
-   service\_running
-   service\_start\_pending
-   service\_stop\_pending
-   service\_stopped

</td></tr><tr><td>

service\_type

</td><td>

StringPossible values:

-   service\_kernel\_driver
-   service\_file\_system\_driver
-   service\_win32\_own\_process
-   service\_win32\_share\_process

</td></tr><tr><td>

startup\_info

</td><td>

String

</td></tr><tr><td>

windows\_integrity\_level

</td><td>

StringPossible values:

-   low
-   medium
-   high
-   system

</td></tr><tr><td>

window\_title

</td><td>

String

</td></tr><tr><td>

sha1\_hash

</td><td>

None

</td><td>

 

</td></tr><tr><td>

sha256\_hash

</td><td>

None

</td><td>

 

</td></tr><tr><td>

sha512\_hash

</td><td>

None

</td><td>

 

</td></tr><tr><td rowspan="5">

software

</td><td>

cpe\(Common Platform Enumeration\)

</td><td>

String

</td></tr><tr><td>

supported\_languages

</td><td>

String

</td></tr><tr><td>

swid\(Software Identification\)

</td><td>

String

</td></tr><tr><td>

vendor

</td><td>

String

</td></tr><tr><td>

version

</td><td>

String

</td></tr><tr><td>

url

</td><td>

None

</td><td>

 

</td></tr><tr><td rowspan="13">

user\_account

</td><td>

account\_created\_time

</td><td>

Date

</td></tr><tr><td>

account\_expiry\_time

</td><td>

Date

</td></tr><tr><td>

account\_type

</td><td>

String

</td></tr><tr><td>

can\_escalate\_privileges

</td><td>

Boolean

</td></tr><tr><td>

credentials\_last\_changed\_time

</td><td>

Date

</td></tr><tr><td>

display\_name

</td><td>

String

</td></tr><tr><td>

first\_login\_time

</td><td>

Date

</td></tr><tr><td>

is\_account\_disabled

</td><td>

Boolean

</td></tr><tr><td>

is\_privileged

</td><td>

Boolean

</td></tr><tr><td>

is\_service\_account

</td><td>

Boolean

</td></tr><tr><td>

last\_login\_time

</td><td>

Date

</td></tr><tr><td>

account\_login

</td><td>

String

</td></tr><tr><td>

user\_id

</td><td>

String

</td></tr><tr><td rowspan="3">

windows\_registry\_key

</td><td>

key\_modified\_time

</td><td>

Date

</td></tr><tr><td>

registry\_value

</td><td>

String

</td></tr><tr><td>

subkeys\_count

</td><td>

Integer

</td></tr><tr><td rowspan="26">

x509\_certificate

</td><td>

authority\_key\_identifier

</td><td>

String

</td></tr><tr><td>

basic\_constraints

</td><td>

String

</td></tr><tr><td>

certificate\_policies

</td><td>

String

</td></tr><tr><td>

crl\_distribution\_points

</td><td>

String

</td></tr><tr><td>

extended\_key\_usage

</td><td>

String

</td></tr><tr><td>

inhibit\_any\_policy

</td><td>

String

</td></tr><tr><td>

issuer

</td><td>

String

</td></tr><tr><td>

issuer\_alternative\_name

</td><td>

String

</td></tr><tr><td>

is\_self\_signed

</td><td>

Boolean

</td></tr><tr><td>

key\_usage

</td><td>

String

</td></tr><tr><td>

name\_constraints

</td><td>

String

</td></tr><tr><td>

policy\_constraints

</td><td>

String

</td></tr><tr><td>

policy\_mappings

</td><td>

String

</td></tr><tr><td>

private\_key\_usage\_valid\_from

</td><td>

Date

</td></tr><tr><td>

private\_key\_usage\_valid\_until

</td><td>

Date

</td></tr><tr><td>

signature\_algorithm

</td><td>

String

</td></tr><tr><td>

subject

</td><td>

String

</td></tr><tr><td>

subject\_alternative\_name

</td><td>

String

</td></tr><tr><td>

subject\_directory\_attributes

</td><td>

String

</td></tr><tr><td>

subject\_key\_identifier

</td><td>

String

</td></tr><tr><td>

subject\_public\_key\_algorithm

</td><td>

String

</td></tr><tr><td>

subject\_public\_key\_exponent

</td><td>

Integer

</td></tr><tr><td>

subject\_public\_key\_modulus

</td><td>

String

</td></tr><tr><td>

valid\_from

</td><td>

Date

</td></tr><tr><td>

valid\_until

</td><td>

Date

</td></tr><tr><td>

version

</td><td>

String

</td></tr></tbody>
</table>### cURL request

This example request contains three observables to create records for in TISC.

```
curl 'http://instance.servicenow.com/api/sn_sec_tisc/v1/threat_intel_data/add_observables' \
--request POST \
--header 'Content-Type: application/json' \
--header 'Authorization: Basic YWRtaW46YWRtaW4=' \
--data '{
   "source": "Sentinel",
   "observables": [
      {
         "value": "1.2.1.45",
         "type": "ip_v4_address",
         "reputation": "malicious",
         "confidence": "90",
         "tags": "critical,important",
         "taxonomies": "MITRE: T121",
         "attack_phases": "Lockheed Martin: Reconnaissance",
         "usage_categories": "Infected Bot",
         "first_seen": "2023-10-14T18:01:34.000Z",
         "attributes": {
            "as_number": "14280"
         }
      },
      {
         "value": "https://example.com",
         "type": "url",
         "tags": "important",
         "confidence": "50",
         "reputation": "malicious"
      },
      {
         "value": "1.1.1.1",
         "type": "ip_add",
         "confidence": "50",
         "reputation": "malicious"
      }
   ]
}'
```

Two of the three observables were successfully added to TISC. One record wasn't created because the observable type is invalid.

```
{
   "status": "partial_success",
   "metadata": {
      "total_records": 3,
      "success_records": 2,
      "error_records": 1
   },
   "success_records": [
      {
         "value": "1.2.1.45",
         "type": "ip_v4_address",
         "sys_id": "e519392643e642102164e0ea78b8f29d"
      },
      {
         "value": "https://example.com",
         "type": "url",
         "sys_id": "ad1979ae43ea42102164e0ea78b8f241"
      }
   ],
   "error_records": [
      {
         "value": "1.1.1.1",
         "type": "ip_va",
         "error_message": "The 'type' field value is invalid"
      }
   ]
}
```

## TISC API - POST /sn\_sec\_tisc/threat\_intel\_data/observables

Retrieves observables data, including relationships between observables and other threat intelligence data such as Structured Threat Information Expression \(STIX\) objects.

Observables returned in the response are sorted by **sys\_id** in ascending order.

For more information about observables and STIX objects, see [IoC Repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/ioc-repository.md).

To access this endpoint, the caller must have the sn\_sec\_tisc.api\_obs\_read\_access role, which by default is included in the Threat Intelligence administrator role \(sn\_sec\_tisc.admin\).

### URL format

Versioned URL: `/api/sn_sec_tisc/{api_version}/threat_intel_data/observables`

Default URL: `/api/sn_sec_tisc/threat_intel_data/observables`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

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

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

included\_fields

</td><td>

Fields to return for observables, observable references, and STIX objects in the response. Different fields can be returned for observables, references, and each type of STIX object.ServiceNow system fields, except for sys\_created\_on, sys\_updated\_on, and sys\_id, aren't returned in the response.

Data type: Object

```
"included_fields": { 
   "observable": {Object},
   "reference": {Object},
   "<stix_object>": {Object}
} 
```

</td></tr><tr><td>

included\_fields.observable

</td><td>

Fields to return for observables. Data type: Object

```
"observable": { 
   "attributes": {Object},
   "common_fields": {Object}
}
```

Default: Returns the fields syd\_id, type, and value for all observable types.

</td></tr><tr><td>

included\_fields.observable.attributes

</td><td>

Fields to return for specified observable types. Data type: Object

```
"attributes": { 
   "<observable_type>": {Object}
}
```

Default: No fields specific to an observable type are returned. Only the fields syd\_id, type, and value are returned.

</td></tr><tr><td>

included\_fields.observable.attributes.&lt;observable\_type&gt;

</td><td>

Fields to return for an observable type.Data type: Object

```
"<observable_type>": { 
   "include_all_fields": Boolean, 
   "values": [Array] 
}
```

Replace `<observable_type>` with the name of the observable type, such as `artifact`. For a complete list of valid observable types, see the Value field in the Observable Type \[sn\_sec\_tisc\_observable\_type\] table.

</td></tr><tr><td>

included\_fields.observable.attributes.&lt;observable\_type&gt;.include\_all\_fields

</td><td>

Flag that indicates whether to return all available fields for the observable type.Valid values:

-   true: Return all fields for the observable type.
-   false: Only return fields specified in the **values** parameter for the observable type.

Data type: Boolean

</td></tr><tr><td>

included\_fields.observable.attributes.&lt;observable\_type&gt;.values

</td><td>

List of fields to return for the observable type. Only use this parameter if the value of **include\_all\_fields** is false.Data type: Array of Strings

```
"values": [
   "String"
]
```

The fields provided must be column\_names from the table for the observable type. The following tables are used for observable types.

-   Artifact \[sn\_sec\_tisc\_artifact\]
-   AS Number \[sn\_sec\_tisc\_as\_number\]
-   Directory \[sn\_sec\_tisc\_directory\]
-   Domain Name \[sn\_sec\_tisc\_domain\_name\]
-   Email Address \[sn\_sec\_tisc\_email\_address\]
-   Email Message \[sn\_sec\_tisc\_email\_message\]
-   Email Subject \[sn\_sec\_tisc\_email\_subject\]
-   File \[sn\_sec\_tisc\_file\]
-   IPv4 Address \[sn\_sec\_tisc\_ipv4\_address\]
-   IPv4 CIDR \[sn\_sec\_tisc\_ipv4\_cidr\]
-   IPv6 Address \[sn\_sec\_tisc\_ipv6\_address\]
-   IPv6 CIDR \[sn\_sec\_tisc\_ipv6\_cidr\]
-   MAC Address \[sn\_sec\_tisc\_mac\_address\]
-   MD5 Hash \[sn\_sec\_tisc\_md5\_hash\]
-   Mutex Name \[sn\_sec\_tisc\_mutex\_name\]
-   Network \[sn\_sec\_tisc\_network\]
-   Other Observable \[sn\_sec\_tisc\_other\_observable\]
-   Process \[sn\_sec\_tisc\_process\]
-   SHA1 Hash \[sn\_sec\_tisc\_sha1\_hash\]
-   SHA256 Hash \[sn\_sec\_tisc\_sha256\_hash\]
-   SHA512 Hash \[sn\_sec\_tisc\_sha512\_hash\]
-   Software \[sn\_sec\_tisc\_software\]
-   URL \[sn\_sec\_tisc\_url\]
-   User Account \[sn\_sec\_tisc\_user\_account\]
-   Windows Registry Key \[sn\_sec\_tisc\_windows\_registry\_key\]
-   X.509 Certificate \[sn\_sec\_tisc\_x\_509\_certificate\]

</td></tr><tr><td>

included\_fields.observable.common\_fields

</td><td>

Fields to return for all observable types.The fields must be from the Observable \[sn\_sec\_tisc\_observable\] table because they must be common to all observable types.

Data type: Object

```
"common_fields": { 
   "include_all_fields": Boolean, 
   "values": [Array] 
}
```

Default: Returns the fields syd\_id, type, and value for all observable types.

</td></tr><tr><td>

included\_fields.observable.common\_fields.include\_all\_fields

</td><td>

Flag that indicates whether to return all fields from the Observable \[sn\_sec\_tisc\_observable\] table for all observable types.Valid values:

-   true: Return all fields from the Observable \[sn\_sec\_tisc\_observable\] table.
-   false: Only return fields specified in the **common\_fields.values** parameter.

Data type: Boolean

</td></tr><tr><td>

included\_fields.observable.common\_fields.values

</td><td>

List of fields to return for all observable types. Only use this parameter if the value of **common\_fields.include\_all\_fields** is false.Data type: Array of Strings

```
"values": [
   "String"
]
```

The fields provided must be column names from the Observable \[sn\_sec\_tisc\_observable\] table.

</td></tr><tr><td>

included\_fields.reference

</td><td>

Fields to return for observable references. Observable references are external references used to describe pointers to information represented outside of STIX.Data type: Object

```
"reference": { 
   "include_all_fields": Boolean, 
   "values": [Array] 
}
```

Default: Returns the fields reference\_source, sys\_id, and url.

</td></tr><tr><td>

included\_fields.reference.include\_all\_fields

</td><td>

Flag that indicates whether to return all available fields for observable references.Valid values:

-   true: Return all fields for observable references.
-   false: Only return fields specified in the **reference.values** parameter.

Data type: Boolean

</td></tr><tr><td>

included\_fields.reference.values

</td><td>

List of fields to return for observable references. Only use this parameter if the value of **reference.include\_all\_fields** is false.Data type: Array of Strings

```
"values": [
   "String"
]
```

The fields provided must be column names from the Observable Reference \[sn\_sec\_tisc\_observable\_reference\] table.

</td></tr><tr><td>

included\_fields.&lt;stix\_object&gt;

</td><td>

Object containing fields to return for a STIX object type.Data type: Object

```
"<stix_object>": { 
  "include_all_fields": Boolean, 
  "values": [Array] 
}
```

Replace `<stix_object>` with the name of the STIX object type, such as `attack_pattern`.

Valid STIX object types:

-   attack\_pattern
-   campaign
-   course\_of\_action
-   data\_component
-   data\_source
-   grouping
-   identity
-   incident
-   indicator
-   infrastructure
-   intrusion\_set
-   location
-   malware
-   malware\_analysis
-   note
-   observed\_data
-   opinion
-   report
-   threat\_actor
-   tool
-   vulnerability

Default: Returns the fields id, name, and sys\_id.

</td></tr><tr><td>

included\_fields.&lt;stix\_object&gt;.include\_all\_fields

</td><td>

Flag that indicates whether to return all available fields for the STIX object type.Valid values:

-   true: Return all fields for the STIX object type.
-   false: Only return fields specified in the **values** parameter for the STIX object type.

Data type: Boolean

</td></tr><tr><td>

included\_fields.&lt;stix\_object&gt;.values

</td><td>

List of fields to return for the STIX object type. Only use this parameter if the value of **include\_all\_fields** is false.Data type: Array of Strings

```
"values": [
   "String"
]
```

The fields provided must be column\_names from the table for the STIX object type. The following tables are used for STIX objects.

-   Attack Pattern \[sn\_sec\_tisc\_attack\_pattern\]
-   Campaign \[sn\_sec\_tisc\_campaign\]
-   Course of Action \[sn\_sec\_tisc\_course\_of\_action\]
-   Data Component \[sn\_sec\_tisc\_aggregated\_data\_component\]
-   Data Source \[sn\_sec\_tisc\_aggregated\_data\_source\]
-   Grouping \[sn\_sec\_tisc\_threat\_grouping\]
-   Identity \[sn\_sec\_tisc\_identity\]
-   Incident \[sn\_sec\_tisc\_threat\_event\]
-   Indicator \[sn\_sec\_tisc\_indicator\]
-   Infrastructure \[sn\_sec\_tisc\_infrastructure\]
-   Intrusion Set \[sn\_sec\_tisc\_intrusion\_set\]
-   Location \[sn\_sec\_tisc\_location\]
-   Malware \[sn\_sec\_tisc\_malware\]
-   Malware Analysis \[sn\_sec\_tisc\_malware\_analysis\]
-   Note \[sn\_sec\_tisc\_threat\_note\]
-   Observed Data \[sn\_sec\_tisc\_observed\_data\]
-   Opinion \[sn\_sec\_tisc\_threat\_opinion\]
-   Report \[sn\_sec\_tisc\_threat\_report\]
-   Threat Actor \[sn\_sec\_tisc\_threat\_actor\]
-   Tool \[sn\_sec\_tisc\_tool\]
-   Vulnerability \[sn\_sec\_tisc\_vulnerability\]

</td></tr><tr><td>

observable\_filters

</td><td>

Filters to apply to the observables. Only observables that match the filter criteria are returned in the response.Data type: Object

```
"observable_filters": {
   "boolean_operator": "String", 
   "filters": [Array]
}
```

Default: Empty object \(no filters applied\)

</td></tr><tr><td>

observable\_filters.boolean\_operator

</td><td>

Boolean operator to use for the filter conditions.Valid values:

-   AND: Return observables that meet all filter conditions.
-   OR: Return observables that meet at least one of the filter conditions.

Data type: String

</td></tr><tr><td>

observable\_filters.filters

</td><td>

Filters to apply to the observables. Each filter object can be simple or complex.

-   Simple filters contain a field name, operator, and value.
-   Complex filters contain a Boolean operator and an array of simple filters. The Boolean operator is applied to the array of simple filters.

Data type: Array of Objects

```
"filters": [ 
   //Simple filter 
   { 
      "field_name": "String", 
      "operator": "String", 
      "field_value": "String" 
   }, 
   //Complex filter 
   {
      "boolean_operator": "String", 
      "filters": [
         {
	     "field_name": "String",
	     "operator": "String",
	     "field_value": "String"
         }  
      ]
   }
]
```

</td></tr><tr><td>

observable\_filters.filters.field\_name

</td><td>

Name of the field to use to filter the observables. Valid values:

-   confidence
-   reputation
-   security\_type
-   status
-   sys\_created\_on
-   sys\_updated\_on
-   tags
-   taxonomies
-   threat\_score
-   type
-   value
-   watch\_list

Data type: String

</td></tr><tr><td>

observable\_filters.filters.operator

</td><td>

Operator to use for the filter.For more information about operators, see [Operators available for filters and queries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/r_OpAvailableFiltersQueries.md).

The data type of the filter field determines the valid operators. The following operators are valid for each data type.

-   **Boolean**

Applicable field: watch\_list

    -   !=
    -   =
    -   ISEMPTY
    -   ISNOTEMPTY
-   **Choice**

Applicable fields: reputation, security\_type, status

    -   !=
    -   =
    -   ENDSWITH
    -   IN
    -   LIKE
    -   NOT IN
    -   NOT LIKE
    -   STARTSWITH
-   **Date-time**

Applicable fields: sys\_created\_on, sys\_updated\_on

    -   &lt;
    -   &lt;=
    -   &gt;
    -   &gt;=
    -   ISEMPTY
    -   ISNOTEMPTY
    -   NOTON
    -   ON
-   **GlideList**

Applicable fields: tags, taxonomies

    -   IN
    -   NOT IN

**Note:** Must use a single valid, existing value for the filter condition, and empty observable field values aren't considered a match.

    -   ISEMPTY
    -   ISNOTEMPTY
    -   LIKE

**Note:** Must use a single value for the filter condition.

    -   NOT LIKE

**Note:** Must use a single value for the filter condition, and empty observable field values aren't considered a match.

-   **Number**

Applicable fields: confidence, threat\_score

    -   !=
    -   &lt;=
    -   =
    -   &gt;=
    -   ISEMPTY
    -   ISNOTEMPTY
-   **Reference**

Applicable field: type

    -   !=
    -   =
    -   IN
    -   ISEMPTY
    -   ISNOTEMPTY
-   **String**

Applicable field: value

    -   !=
    -   &lt;=
    -   =
    -   &gt;=
    -   ENDSWITH
    -   IN
    -   ISEMPTY
    -   ISNOTEMPTY
    -   LIKE
    -   NOT LIKE
    -   STARTSWITH

Data type: String

</td></tr><tr><td>

observable\_filters.filters.field\_value

</td><td>

Value of the field.For choice fields, the value must be the internal value, not the display value. For date-time fields, the value must be in ISO format in the UTC timezone.

**Note:** This parameter isn’t required when using the ISEMPTY or ISNOTEMPTY operators.

Data type: String

</td></tr><tr><td>

page\_size

</td><td>

Limits the number of observables that are returned in the API response. Used for pagination.Data type: String

Default: 100

Maximum value: 1000

</td></tr><tr><td>

page\_token

</td><td>

Used to get observables data for the current page.To get the first page, this parameter can be omitted or the value for this parameter must be an empty string. To get the next page in the following request, use the **next\_page\_token** value from the response body as the value for this parameter.

Data type: String

Default: Empty string

</td></tr><tr><td>

relationships

</td><td>

Relationship types to return for each observable in the response. The relationships can be with another observable, an observable reference, or a Structured Threat Information Expression \(STIX\) object.

Valid values:

-   attack\_pattern
-   campaign
-   course\_of\_action
-   data\_component
-   data\_source
-   grouping
-   identity
-   incident
-   indicator
-   infrastructure
-   intrusion\_set
-   location
-   malware
-   malware\_analysis
-   note
-   observable
-   observed\_data
-   opinion
-   reference
-   report
-   threat\_actor
-   tool
-   vulnerability

For example, passing the array `["observable", "threat_actor"]` returns all related observables and threat actors for each observable in the response.

Data type: Array

Default: Empty array \(no relationships returned\)

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

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

Bad request. The request parameters are invalid or the request body JSON has a syntactical error.To view details about the error, see the **error** parameter in the response body.

</td></tr><tr><td>

401

</td><td>

Unauthorized. The user authentication is invalid. Check the user name and password or OAuth token.

</td></tr><tr><td>

403

</td><td>

Forbidden. The calling user is missing a required role. The sn\_sec\_tisc.api\_obs\_read\_access role is required to access this endpoint.

</td></tr><tr><td>

429

</td><td>

Too many requests. The number of API requests exceeds the rate limit for the API. By default, the limit is 500 requests per hour.

</td></tr><tr><td>

500

</td><td>

Internal server error. Check application logs in the Log \[syslog\] table for more information about the error.

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

is\_last\_page

</td><td>

Flag that indicates whether this is the last page of observables data.Valid values:

-   true: This response contains the last page of data.
-   false: There are additional pages that can be returned.

Data type: Boolean

</td></tr><tr><td>

next\_page\_token

</td><td>

Use this value in the next API request to get the next page of observables data. Provide this value in the **page\_token** parameter in the request body.Data type: String

</td></tr><tr><td>

observables

</td><td>

Observables objects. Data type: Array of Objects

```
"observables": [
  {
    "attributes": {Object},
    "relationships": {Object},
    "sys_id": "String",
    "type": "String",
    "value": "String"
  }
]
```

Each observables object also includes the fields specified by the **included\_fields.observable.common\_fields** parameter in the request body.

</td></tr><tr><td>

observables.attributes

</td><td>

Name-value pairs for the fields specified by the **included\_fields.observable.attributes.&lt;observable\_type&gt;** parameter in the request body.Data type: Object

```
"attributes": {
   "<field>": "<value>"
}
```

</td></tr><tr><td>

observables.relationships

</td><td>

Relationships for the observable. The types of relationships returned are specified by the **relationships** parameter in the request body, and the fields returned for each relationship are specified by the **included\_fields** parameter in the request body.This example shows the basic structure of this parameter. However, the relationship types and fields returned vary based on the request body parameters.

Data type: Object

```
"relationships": {
   "observable": [
      {
         "sys_id": "String",
         "type": "String",
         "value": "String"
      }
   ],
   "indicator": [
      {
         "id": "String",
         "name": "String",
         "sys_id": "String"
      }
   ],
   "attack_pattern": [
      {
         "id": "String",
         "name": "String",
         "sys_id": "String"
      }
   ]
}
```

</td></tr><tr><td>

observables.sys\_id

</td><td>

Sys\_id of the observable.Data type: String

Table: Observable \[sn\_sec\_tisc\_observable\]

</td></tr><tr><td>

observables.type

</td><td>

Type of observable. For a complete list of valid observable types, see the **Value** field in the Observable Type \[sn\_sec\_tisc\_observable\_type\] table.Data type: String

</td></tr><tr><td>

observables.value

</td><td>

Value associated with the observable, such as an IP address or URL.Data type: String

</td></tr><tr><td>

origin

</td><td>

Origin application of the response, which is Threat Intelligence Security Center \(TISC\). The value of this parameter is `sn_sec_tisc`.This value can optionally be used by SIEMs consuming the API response to trace whether the intelligence from TISC resulted in the creation of security incidents.

Data type: String

</td></tr><tr><td>

page\_size

</td><td>

Maximum number of observables returned in the response. Used for pagination.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the API request.Possible values:

-   failure
-   success

If the request failed, see the **error** parameter in the response body for more information about the error.

Data type: String

</td></tr></tbody>
</table>### cURL request

This example returns the first page of observables data. The **observable\_filters** parameter specifies to return only observables that match the condition `status = active AND [threat_score >= 70 OR confidence >= 50]`.

```
curl 'http://instance.servicenow.com/api/sn_sec_tisc/v1/threat_intel_data/observables' \
--request POST \
--header 'Content-Type: application/json' \
--header 'Authorization: Basic YWRtaW46YWRtaW4=' \
--data '{
   "page_size": "100",
   "page_token": "",
   "relationships": [
      "observable",
      "threat_actor",
      "indicator",
      "reference",
      "attack_pattern"
   ],
   "included_fields": {
      "observable": {
         "common_fields": {
            "include_all_fields": false,
            "values": [
               "value",
               "reputation",
               "confidence"
            ]
         },
         "attributes": {
            "ip_v4_address": {
               "include_all_fields": false,
               "values": [
                  "as_number"
               ]
            },
            "artifact": {
               "include_all_fields": false,
               "values": [
                  "mime_type",
                  "encryption_algorithm"
               ]
            }
         }
      },
      "threat_actor": {
         "include_all_fields": false,
         "values": [
            "name",
            "aliases",
            "description",
            "threat_actor_roles"
         ]
      },
      "attack_pattern": {
         "include_all_fields": true
      },
      "indicator": {
         "include_all_fields": false,
         "values": [
            "name",
            "pattern",
            "pattern_type",
            "indicator_types"
         ]
      },
      "reference": {
         "include_all_fields": true,
         "values": [
            "description"
         ]
      }
   },
   "observable_filters": {
      "boolean_operator": "AND",
      "filters": [
         {
            "field_name": "status",
            "operator": "=",
            "field_value": "active"
         },
         {
            "boolean_operator": "OR",
            "filters": [
               {
                  "field_name": "threat_score",
                  "operator": ">=",
                  "field_value": "70"
               },
               {
                  "field_name": "confidence",
                  "operator": ">=",
                  "field_value": "50"
               }
            ]
         }
      ]
   }
}'
```

Response body.

```
{
   "status": "success",
   "observables": [
      {
         "sys_id": "792e3d1543a0421060eee0ea78b8f227",
         "type": "url",
         "value": "https://www.example.com",
         "confidence": "60",
         "reputation": "",
         "relationships": {
            "observable": [
               {
                  "sys_id": "ccadb19143a0421060eee0ea78b8f25a",
                  "type": "ip_v4_address",
                  "value": "1.1.1.1",
                  "confidence": "20",
                  "reputation": "malicious"
               }
            ],
            "indicator": [
               {
                  "id": "indicator--294d97754364c21060eee0ea78b8f2ae",
                  "indicator_types": "",
                  "name": "Poison Ivy",
                  "pattern": "",
                  "pattern_type": "sigma",
                  "sys_id": "a54d97754364c21060eee0ea78b8f2ae",
                  "type": "indicator"
               }
            ],
            "attack_pattern": [
               {
                  "name": "Phishing",
                  "sys_id": "010d5bf14364c21060eee0ea78b8f2ac",
                  "id": "attack-pattern--810d5bf14364c21060eee0ea78b8f2ac",
                  "type": "attack-pattern"
               }
            ],
            "reference": [
               {
                  "description": "phishing",
                  "reference_source": "CAPEC-98",
                  "sys_created_on": "2024-02-25T03:34:45.000Z",
                  "sys_id": "a42d97354364c21060eee0ea78b8f28c",
                  "sys_updated_on": "2024-02-25T03:34:45.000Z",
                  "url": " https://capec.mitre.org/data/98.html "
               }
            ]
         },
         "attributes": {
            "encryption_algorithm": "mime-type-indicated",
            "mime_type": "application/zip"
         }
      },
      {
         "sys_id": "ccadb19143a0421060eee0ea78b8f2242",
         "type": "ip_v4_address",
         "value": "1.2.2.1",
         "confidence": "70",
         "reputation": "",
         "relationships": {}
      },
      {
         "sys_id": "7ccd359143a0421060eee0ea78b8f264",
         "type": "artifact",
         "value": "pom.xml",
         "confidence": "",
         "reputation": "",
         "relationships": {}
      }
   ],
   "page_size": "100",
   "next_page_token": "drejvfgbresg|7ccd359143a0421060eee0ea78b8f264",
   "is_last_page": true,
   "origin": "sn_sec_tisc"
}
```

