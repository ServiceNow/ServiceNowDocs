---
title: View and filter the HL7 message log
description: Use the HL7 message log to review inbound messages, inspect raw message content and ACK responses, and filter by status, message type, or sending facility.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-message-log-view.html
release: australia
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [message log, HL7 message log, view messages]
breadcrumb: [HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# View and filter the HL7 message log

Use the HL7 message log to review inbound messages, inspect raw message content and ACK responses, and filter by status, message type, or sending facility.

## Before you begin

Role required: `sn_hl7_v2.admin`

## Procedure

1.  Navigate to **All** &gt; **HL7 Integration** &gt; **Message Log**.

2.  To filter the message list, use the filter bar to set conditions on any of the following fields:

    -   **Status**: Pending, Processing, Processed, or Failed
    -   **ACK code**: AA, AE, or AR
    -   **Message type**: for example, ADT or ORU
    -   **Trigger event**: for example, A03
    -   **Sending facility**
    -   **Sending application**
3.  Click a message row to open the message record.

4.  In the message record, review the **Raw HL7 Payload** field for the inbound HL7 message and the **Parsed Data** field for the extracted JSON output.

5.  To view the full ACK response sent back to the integration engine, expand the **ACK response** field.


**Related topics**  


[HL7 message log fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-message-log-fields.md)

[Investigate failed messages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-failed-messages-investigate.md)

