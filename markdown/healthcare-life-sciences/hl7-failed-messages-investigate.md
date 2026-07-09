---
title: Investigate failed HL7 messages
description: Identify and diagnose inbound HL7 messages that resulted in an application error \(AE\), application rejection \(AR\), or failed processing status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-failed-messages-investigate.html
release: australia
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [failed messages, AE, AR, troubleshoot HL7]
breadcrumb: [View and filter the HL7 message log, HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# Investigate failed HL7 messages

Identify and diagnose inbound HL7 messages that resulted in an application error \(AE\), application rejection \(AR\), or failed processing status.

## Before you begin

Role required: `sn_hl7_v2.admin`

## Procedure

1.  Navigate to the HL7 message log and filter for failed messages using one or both of the following conditions:

    -   **Status** = Failed
    -   **ACK code** = AE or AR
    AE \(Application Error\) indicates ServiceNow encountered an error processing the message. AR \(Application Rejection\) indicates the message was structurally valid but rejected by the application. A Failed status indicates processing did not complete.

2.  Open a failed message record.

3.  Read the **Error message** field for the failure detail text.

4.  Expand the **ACK response** field to see the full ACK body returned to the integration engine, including the MSA-3 text description of the error.

5.  Review the **Work notes** field for any audit trail entries added during processing.

6.  If the failure was due to a transient error, reprocess the message after the issue is resolved.


**Related topics**  


[ACK codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-ack-codes.md)

[View and filter the message log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-message-log-view.md)

