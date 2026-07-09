---
title: HL7 ACK codes
description: ServiceNow returns one of three HL7 acknowledgment codes in the MSA segment of every ACK response, indicating whether the message was accepted, rejected at the application level, or resulted in an error.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-ack-codes.html
release: australia
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [ACK code, AA, AE, AR, acknowledgment]
breadcrumb: [Components installed with HL7 v2.x Integration, HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# HL7 ACK codes

ServiceNow returns one of three HL7 acknowledgment codes in the MSA segment of every ACK response, indicating whether the message was accepted, rejected at the application level, or resulted in an error.

|Code|Meaning|When it occurs and what to do|
|----|-------|-----------------------------|
|`AA`|Application Accept|ServiceNow received the message, validated its MSH header, matched a parser configuration, and parsed and staged it. The message log record is created with status Pending for downstream processing. No action required.|
|`AE`|Application Error|ServiceNow could not process the message, either because its MSH header failed structural validation or because a field could not be parsed against the matched configuration. The message log record is created with status Failed. Review the **Error message** field for detail, then reprocess the message after the underlying issue is resolved.|
|`AR`|Application Rejection|ServiceNow received a structurally valid message but could not match it to exactly one active parser configuration — either no active configuration matches the message's sending application, sending facility, HL7 version, message type, and trigger event, or more than one active configuration matches. The message log record is created with status Failed. Review the **Error message** field for the rejection reason, then add or correct the parser configuration.|

## ACK delivery and HTTP status codes

ServiceNow returns HTTP 200 when the message is structurally valid and a message log record is staged — this includes the AA, AR, and parse-error AE outcomes. A structurally invalid message \(a missing or malformed MSH header\) returns HTTP 422, and an unexpected server error returns HTTP 500. The integration engine should inspect the acknowledgment code to determine the application-level outcome, not the HTTP status alone. The acknowledgment is returned as a standards-compliant HL7 v2.x \(ER7\) message in the response body, with the acknowledgment code in the MSA-1 field.

