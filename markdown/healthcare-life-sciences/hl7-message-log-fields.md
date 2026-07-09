---
title: HL7 message log fields
description: Field reference for the HL7 Message Log table \(sn\_hl7\_v2\_message\_log\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-message-log-fields.html
release: australia
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [message log fields, HL7 message log]
breadcrumb: [Components installed with HL7 v2.x Integration, HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# HL7 message log fields

Field reference for the HL7 Message Log table \(`sn_hl7_v2_message_log`\).

<table><thead><tr><th>

Field

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`number`

</td><td>

String

</td><td>

Auto-generated unique identifier for the message log record. Uses the HL7 prefix.

</td></tr><tr><td>

`raw_payload`

</td><td>

MultiLine String

</td><td>

The complete raw inbound HL7 v2.x message as received. **Caution:**

This field may contain protected health information \(PHI\). Access is restricted by a column-level ACL to the `sn_hl7_v2.admin` role, consistent with HIPAA minimum-necessary requirements.

</td></tr><tr><td>

`status`

</td><td>

Choice

</td><td>

Processing status of the message. Values: Pending, Processing, Processed, Failed.

</td></tr><tr><td>

`message_type`

</td><td>

String \(20\)

</td><td>

HL7 message type extracted from MSH-9.1 \(for example, `ADT`\).

</td></tr><tr><td>

`message_event`

</td><td>

String \(20\)

</td><td>

HL7 trigger event extracted from MSH-9.2 \(for example, `A03`\).

</td></tr><tr><td>

`hl7_version`

</td><td>

String \(20\)

</td><td>

HL7 version extracted from MSH-12 \(for example, `2.5.1`\).

</td></tr><tr><td>

`sending_application`

</td><td>

String \(100\)

</td><td>

Sending application extracted from MSH-3.

</td></tr><tr><td>

`sending_facility`

</td><td>

String \(100\)

</td><td>

Sending facility extracted from MSH-4.

</td></tr><tr><td>

`message_control_id`

</td><td>

String \(100\)

</td><td>

Message control ID extracted from MSH-10. Used for correlation between the original message and its ACK response.

</td></tr><tr><td>

`message_datetime`

</td><td>

DateTime

</td><td>

Message timestamp extracted from MSH-7 and converted to ServiceNow format.

</td></tr><tr><td>

`ack_code`

</td><td>

Choice

</td><td>

The acknowledgment code returned to the integration engine. Values: AA \(Application Accept\), AE \(Application Error\), AR \(Application Rejection\).

</td></tr><tr><td>

`ack_response`

</td><td>

MultiLine String

</td><td>

The complete raw HL7 ACK response body returned to the integration engine.

</td></tr><tr><td>

`error_message`

</td><td>

String \(1000\)

</td><td>

Failure detail text populated when processing results in an AE or AR ACK code or a Failed status.

</td></tr><tr><td>

`additional_notes`

</td><td>

String \(4000\)

</td><td>

Non-MSH segment data captured during processing.

</td></tr><tr><td>

`parsed_data`

</td><td>

JSON

</td><td>

The structured result of parsing the message against the matched parser configuration. Its shape is determined by the `field_name` dotted paths on the configuration's active field maps. Values are raw HL7 strings; HL7 fields absent from the message are stored as `null`.

</td></tr></tbody>
</table>