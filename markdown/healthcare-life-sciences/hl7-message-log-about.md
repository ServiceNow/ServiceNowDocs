---
title: HL7 message log
description: The HL7 message log stores every inbound HL7 v2.x message received by ServiceNow, along with its ACK response, extracted metadata, and processing status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-message-log-about.html
release: australia
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [HL7 message log, message log, ACK]
breadcrumb: [HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# HL7 message log

The HL7 message log stores every inbound HL7 v2.x message received by ServiceNow, along with its ACK response, extracted metadata, and processing status.

When ServiceNow receives an HL7 v2.x message, it immediately creates a record in the HL7 message log \(`sn_hl7_v2_message_log`\). The log record captures the complete inbound message, the ACK response sent back to the integration engine, and key metadata fields extracted from the MSH segment.

## What the message log stores

Each message log record stores:

-   The complete raw inbound HL7 message \(`raw_payload`\)
-   The complete raw ACK response body \(`ack_response`\)
-   The ACK code: AA \(Application Accept\), AE \(Application Error\), or AR \(Application Rejection\) \(`ack_code`\)
-   Message type \(MSH-9.1\), trigger event \(MSH-9.2\), HL7 version \(MSH-12\), sending application \(MSH-3\), sending facility \(MSH-4\), message control ID \(MSH-10\), and message timestamp \(MSH-7\)
-   The time the message was received by ServiceNow and the processing duration
-   Processing status: Pending, Processing, Processed, or Failed
-   An error message field for failure detail text and an additional notes field for non-MSH segment data
-   The parsed message body as structured JSON \(`parsed_data`\), shaped by the matched parser configuration

## Message log metadata as Flow Designer trigger conditions

All metadata fields on the message log record are queryable, sortable, and available as Flow Designer trigger conditions. A flow author in a consuming application can configure a flow to trigger when a message log record is created and filter it with a condition such as "ACK code = AA AND message type = ADT AND trigger event = A03 AND sending facility = MAIN" — so routing logic lives in the flow's trigger condition, not in custom scripts.

## Parsing happens at reception

When a message is received, ServiceNow looks up the active parser configuration that matches the message and parses the configured segment fields into the `parsed_data` JSON on the message log record — automatically, with no flow or action required. Downstream flows in consuming applications read `parsed_data` directly from the record rather than re-parsing the raw payload.

## PHI and access control

The `raw_payload` field may contain protected health information \(PHI\). Access to this field is restricted by a column-level access control list \(ACL\) to the minimum necessary, consistent with HIPAA requirements. All tables in the HL7 integration application are restricted to the `sn_hl7_v2.admin` role, the only role the application defines.

