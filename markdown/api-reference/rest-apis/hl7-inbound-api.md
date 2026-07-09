---
title: HL7 Inbound API
description: The HL7 Inbound API receives inbound HL7 v2.x ADT messages from EHR systems over HTTP and returns standard HL7 acknowledgment responses. It implements the HAPI HL7-over-HTTP convention, accepting raw pipe-delimited ER7 message bodies and processing them against configured parser profiles.Accepts a raw pipe-delimited HL7 v2.x message in ER7 format, validates the MSH segment, resolves a matching parser profile, and creates an sn\_hl7\_v2\_message\_log record for downstream processing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/hl7-inbound-api.html
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-05-12"
reading_time_minutes: 8
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# HL7 Inbound API

The HL7 Inbound API receives inbound HL7 v2.x ADT messages from EHR systems over HTTP and returns standard HL7 acknowledgment responses. It implements the HAPI HL7-over-HTTP convention, accepting raw pipe-delimited ER7 message bodies and processing them against configured parser profiles.

The HL7 Inbound API is supported under the ServiceNow® Healthcare and Life Sciences application. The API accepts HTTP POST requests containing a raw HL7 v2.x message body and performs these operations:

-   Validates the MSH segment for required fields \(MSH.3, MSH.4, MSH.7, MSH.9, MSH.10, MSH.12\) and encoding characters \(`^~\&`\).
-   Resolves a matching active parser profile using the composite key: Sending Application \(MSH.3\), Sending Facility \(MSH.4\), HL7 Version \(MSH.12\), Message Type \(MSH.9\), and Message Event \(MSH.9\).
-   Parses configured HL7 fields per the matched profile's segment and field map definitions, storing the result as a JSON blob \(`parsed_data`\) on the message log record.
-   Creates an `sn_hl7_v2_message_log` record for only the messages with an active parser configuration. If the parser configuration isn't detected, an ACK is sent back to the sender.
-   Returns an HL7 v2.x ACK response \(MSH + MSA segments in ER7 format\) with one of the following ACK codes:
    -   `AA`: accepted
    -   `AR`: rejected, no matching profile found
    -   `AE`: error

Consider using the HL7 Inbound API for these common use cases:

-   EHR systems sending ADT discharge notifications \(ADT^A03\) to trigger downstream workflows such as Environmental Services \(EVS\) case creation in ServiceNow.
-   Any HL7 v2.x message type for which a matching active parser profile is configured.
-   Integration testing and parser profile validation before go-live.

For more information about these features, see [HL7 v2.x Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-integration-overview.md).

## Requirements

The HL7 Inbound API is supported by the HL7 V2.x Integration application and requires the sn\_hl7\_v2 plugin.

The sn\_hl7\_v2.admin role is required to invoke the API.

Before sending messages to this API, an active parser profile must be configured in ServiceNow. The parser profile tells the API how to read and extract data from incoming HL7 messages. Without a matching active profile, the API still accepts the message but returns an Application Reject \(AR\) acknowledgment and doesn't parse the payload. A complete parser profile consists of three records:

1.  Parser configuration \(sn\_hl7\_v2\_parser\_config table\): The top-level profile record. Must be set to active and uniquely identify the sending system using the following fields:

    -   Sending Application
    -   Sending Facility
    -   HL7 Version
    -   Message Type
    -   Message Event
    These values must match the corresponding MSH segment fields in the incoming message exactly.

2.  Segment definitions \(sn\_hl7\_v2\_parser\_segment table\): One or more records defining which HL7 segments the API should extract from the message.
3.  Field mappings \(sn\_hl7\_v2\_parser\_field\_map table\): Records that map specific field positions within each segment to output field names stored on the message log record. For setup instructions, see Extending the API.

## Downstream processing

This is a standalone endpoint. Downstream processing, such as EVS case creation, is triggered asynchronously by a record insert on `sn_hl7_v2_message_log` from a separate consumer-scope application \(`app-ind-cto-evs`\) and not by a subsequent API call.

## Extending the API

The HL7 Inbound API accepts any HL7 v2.x message type in the base system. Processing behavior is driven entirely by parser profiles; no code changes are required to support a new message type or EHR system. To add support, an administrator creates a new [parser configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-parser-configs-about.md).

To add support for a new sending system or message type:

1.  In the app navigator, open **HL7 Parser Configurations**.
2.  Create a new parser profile \(`sn_hl7_v2_parser_config`\) with a composite key that matches the sending system's MSH fields: Sending Application, Sending Facility, HL7 Version, Message Type, and Message Event.
3.  Add segment records \(`sn_hl7_v2_parser_segment`\) for each HL7 segment you want to extract.
4.  Add field map records \(`sn_hl7_v2_parser_field_map`\) to define the field position-to-output field name mappings for each segment.
5.  Use the **Parse Sample Payload** UI action to validate the profile against a real HL7 message before activating it.

To clone from existing parser configuration, see the instructions in [Clone and customize a parser configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-parser-config-clone.md).

**Parent Topic:**[REST API reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/api-rest.md)

## HL7 Inbound - POST /api/sn\_hl7\_v2/hl7/message

Accepts a raw pipe-delimited HL7 v2.x message in ER7 format, validates the MSH segment, resolves a matching parser profile, and creates an sn\_hl7\_v2\_message\_log record for downstream processing.

The response is an HL7 ACK message body. Inspect both the HTTP status code and the MSA segment ACK code to determine the outcome.

Call this endpoint whenever an external system, such as an EHR or integration engine, needs to deliver an inbound HL7 v2.x message to ServiceNow.

### URL format

Versioned URL: `/api/sn_hl7_v2/{api_version}/hl7/message`

Default URL: `/api/sn_hl7_v2/hl7/message`

### Supported request parameters

<table id="table_ahh_z4h_gjc" class="rest_api_path_parameters"><thead><tr><th>

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

### Request body parameters \(ER7 segments\)

The following fields are transmitted as segments and field positions within the raw HL7 v2.x pipe-delimited \(ER7\) message body, not as JSON or XML parameters. Each field is identified by its MSH position number.

<table id="table_dhh_z4h_gjc" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MSH.2

</td><td>

Required. Encoding characters. Must be exactly `^~\&` or the message is rejected.Data type: String

</td></tr><tr><td>

MSH.3

</td><td>

Required. Sending Application. Used in the parser profile composite key and to address the ACK response.Data type: String

</td></tr><tr><td>

MSH.4

</td><td>

Required. Sending Facility. Used in the parser profile composite key and to address the ACK response.Data type: String

</td></tr><tr><td>

MSH.7

</td><td>

Required. Date/time of message in `YYYYMMDDHHmmss` format. Stored on the message log record.Table: Message Log \[sn\_hl7\_v2\_message\_log\]

Data type: String

</td></tr><tr><td>

MSH.9

</td><td>

Required. Message type and event. For example, `ADT^A03^ADT_A03`. Used in the parser profile composite key.**Note:** Both the message type and message event components are used separately in the lookup, since MSH.9 is a composite field.

Data type: String

</td></tr><tr><td>

MSH.10

</td><td>

Required. Message Control ID. Echoed back in the `MSA.2` field of the ACK response.Data type: String

</td></tr><tr><td>

MSH.12

</td><td>

Required. Version ID. For example, `2.5.1`. Used in the parser profile composite key.Data type: String

</td></tr><tr><td>

Additional segments

</td><td>

Optional. HL7 segments, such as `EVN`, `PID`, `PV1`. Parsed per the matched parser profile's segment and field map configuration. Extracted fields are stored as JSON in the message log record.Table: Message Log \[sn\_hl7\_v2\_message\_log\], Field: `parsed_data`

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Content-Type: x-application/hl7-v2+er7|Required. Identifies the body as a raw HL7 v2.x pipe-delimited \(ER7\) message. Any other content type returns an error.|
|Authorization: Basic &lt;base64\(user:password\)&gt;|Required. ServiceNow Basic Auth credentials for the calling user or any ServiceNow supported authentication types, such as OAuth.|

|Header|Description|
|------|-----------|
|Content-Type: x-application/hl7-v2+er7|Always set by the endpoint. Indicates the response body is a raw HL7 ACK message in ER7 format.|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Message was processed. Inspect MSA segment ACK code for outcome:

-   `AA`: Accepted and staged successfully.
-   `AR`: Rejected, no matching active parser profile found.
-   `AE`: Application error, field parsing failed.

In all three cases an sn\_hl7\_v2\_message\_log record is created.

</td></tr><tr><td>

422

</td><td>

MSH structural validation failed. Possible errors:

-   Request body is empty,
-   MSH segment missing or malformed,
-   Encoding characters wrong,
-   Required MSH field is empty.

ACK code in body will be AE. No message log record is created.

</td></tr><tr><td>

500

</td><td>

Unexpected server-side error. ACK code in body returns `AE` with "Internal server error" detail.

</td></tr></tbody>
</table>### Response body parameters \(ER7 segments\)

The response body is a raw HL7 v2.x ACK message in pipe-delimited ER7 format containing two segments: MSH and MSA.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MSH segment

</td><td>

ACK message header in pipe-delimited ER7 format. Key fields:

-   `MSH.3`: Responding application \(`sn_hl7_v2`\).
-   `MSH.5`: Original sending application.
-   `MSH.6`: Original sending facility.
-   `MSH.7`: Response timestamp in `YYYYMMDDHHmmss` format.
-   `MSH.9`: Message type and event \(`ACK^A01^ACK`\).
-   `MSH.10`: New GUID-derived control ID.
-   `MSH.12`: Version ID \(`2.5`\).

Data type: String \(pipe-delimited HL7 segment\)

</td></tr><tr><td>

MSA segment

</td><td>

Message acknowledgment.Possible values:

-   `MSA.1`: ACK code. For example, AA, AR, or AE.
-   `MSA.2`: Original message control ID from inbound MSH.10.
-   `MSA.3`: Error detail. Present only when ACK code isn't AA.

Data type: String \(pipe-delimited HL7 segment\)

</td></tr></tbody>
</table>### cURL request

This example sends an ADT^A03 \(patient discharge\) message from an EHR system to the HL7 Inbound API. The message originates from the `EPIC` application at `GENERAL_HOSPITAL`. The API validates the MSH segment, resolves a matching active parser profile using the composite key \(`EPIC` + `GENERAL_HOSPITAL` + `2.5.1` + `ADT` + `A03`\), parses the configured fields from the EVN, PID, and PV1 segments, and creates an `sn_hl7_v2_message_log` record. The response is an HL7 ACK message addressed back to the originating system.

**Request:**

```
curl 'https://<instance>.service-now.com/api/sn_hl7_v2/v1/hl7/message' \
  --request POST \
  --header 'Content-Type: x-application/hl7-v2+er7' \
  --user 'username:password' \
  --data-binary $'MSH|^~\\&|EPIC|GENERAL_HOSPITAL|sn_hl7_v2||20260421120000||ADT^A03^ADT_A03|CTRL001|P|2.5.1\rEVN|A03|20260421120000\rPID|1||MRN001^^^GENERAL_HOSPITAL||Doe^John\rPV1|1|I|WEST_WING^ROOM1'
```

**Response body: Success \(HTTP 200, ACK AA\)**

```
MSH|^~\&|sn_hl7_v2||EPIC|GENERAL_HOSPITAL|20260421120005||ACK^A01^ACK|A1B2C3D4E5F6|P|2.5 
MSA|AA|CTRL001
```

The message was accepted and fully parsed. The ACK is addressed back to the originating system \(`EPIC` at `GENERAL_HOSPITAL`\). `MSA.1` returns `AA` and `MSA.2` echoes the original Message Control ID \(`CTRL001`\).

**Response body: No profile match \(HTTP 200, ACK AR\)**

```
MSH|^~\&|sn_hl7_v2||EPIC|GENERAL_HOSPITAL|20260421120005||ACK^A01^ACK|G7H8I9J0K1L2|P|2.5 
MSA|AR|CTRL001|No active parser profile found for the inbound message.
```

The MSH segment was valid but no active parser profile matched the composite key. Because no matching parser configuration is found, the record isn't staged on sn\_hl7\_v2\_message\_log. MSA.1 returns AR and MSA.3 contains the rejection detail. To resolve this, verify that an active parser profile exists for the sending system and message type. See Requirements.

**Response body: MSH validation failure \(HTTP 422, ACK AE\)**

```
MSH|^~\&|sn_hl7_v2||||20260421120005||ACK^A01^ACK|M3N4O5P6Q7R8|P|2.5 
MSA|AE||Request body is empty.
```

The request failed MSH validation before processing could begin. Note that `MSH.5` and `MSH.6` are empty in the response — because the sending application and facility could not be read from the inbound message, the ACK cannot be addressed back to the originator. `MSA.1` returns `AE` and `MSA.3` contains the error detail.

