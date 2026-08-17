---
title: How HL7 integration works in ServiceNow
description: HL7 v2.x messages flow through four stages in ServiceNow: reception and acknowledgment, message logging, parsing, and workflow execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-integration-how-it-works.html
release: australia
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [HL7, HL7 workflow, ADT, Flow Designer]
breadcrumb: [HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# How HL7 integration works in ServiceNow

HL7 v2.x messages flow through four stages in ServiceNow: reception and acknowledgment, message logging, parsing, and workflow execution.

## End-to-end message flow

The following describes the path of an inbound HL7 v2.x message from the integration engine through to workflow execution:

1.  **Integration engine sends a message.** The integration engine \(for example, Epic's integration engine\) POSTs a raw ER7-formatted HL7 message to the ServiceNow REST endpoint over HTTPS. The integration engine requires no custom configuration beyond the endpoint URL and credentials. For the endpoint URL, authentication, and message schema, see the [HL7 Inbound API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/hl7-inbound-api.md) reference.
2.  **ServiceNow validates and acknowledges.** ServiceNow validates the MSH header and returns an acknowledgment indicating the outcome — AA \(accept\), AE \(error\), or AR \(reject\). For acknowledgment codes and HTTP status behavior, see [HL7 ACK codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-ack-codes.md).
3.  **ServiceNow parses and stages the message.** ServiceNow looks up the single active parser configuration whose sending application, sending facility, HL7 version, message type, and trigger event match the message, and extracts the configured segment fields into the `parsed_data` JSON on a new HL7 message log record. On success the record is created with status **Pending**; if no single configuration matches, or a field cannot be parsed, the record is created with status **Failed**. Parsing happens automatically at reception — no flow or action is required.
4.  **A downstream flow runs.** A Flow Designer flow in a consuming application triggers when the message log record is created. The flow's trigger condition can filter on the record's metadata \(for example, message type = ADT, trigger event = A03, sending facility = MAIN\), and the flow reads the parsed values from `parsed_data` to drive downstream work — such as room turnover tasks, care team notifications, or encounter updates.

## North star scenario: ADT^A03 discharge to room turnover

A patient is discharged from room 4B-401-A. The EHR system sends an ADT^A03 message to the integration engine, which POSTs it to ServiceNow. ServiceNow validates the message, parses it against the matching ADT^A03 parser configuration into `parsed_data`, stages a message log record with status Pending, and returns ACK\(AA\). A Flow Designer flow in the room turnover application triggers on the new record, reads the PV1 location values \(unit, room, bed\) from `parsed_data`, marks the room as Needs Cleaning, creates and assigns an EVS task, and notifies the charge nurse — all without manual intervention. The room turnover flow lives in a downstream Healthcare Operations application, not in the HL7 integration application.

## What ServiceNow does not do

ServiceNow does not listen for HL7 messages over MLLP or TCP/IP. Your existing integration engine handles transport and delivers messages to ServiceNow over HTTPS. ServiceNow does not write back to the EHR — the integration is inbound only.

