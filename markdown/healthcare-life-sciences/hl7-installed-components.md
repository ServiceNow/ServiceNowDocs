---
title: Components installed with HL7 v2.x Integration
description: Several types of components are installed with activation of the HL7 v2.x Native Integration plugin, including tables, user roles, and Flow Designer actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-installed-components.html
release: australia
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [installed components, HL7 tables, HL7 roles]
breadcrumb: [HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# Components installed with HL7 v2.x Integration

Several types of components are installed with activation of the HL7 v2.x Native Integration plugin, including tables, user roles, and Flow Designer actions.

## Roles installed

<table><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HL7 Integration Administrator

 \[`sn_hl7_v2.admin`\]

</td><td>

Manages HL7 integration configuration, including parser configurations and message log access. Required for all administrative tasks in the HL7 integration application.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HL7 Message Log

 \[`sn_hl7_v2_message_log`\]

</td><td>

Stores every inbound HL7 v2.x message received by ServiceNow, including the raw payload, ACK response, extracted MSH metadata fields, and processing status. The `raw_payload` field is protected by a column-level ACL.

</td></tr><tr><td>

HL7 Parser Configuration

 \[`sn_hl7_v2_parser_config`\]

</td><td>

Defines parser configurations that map HL7 message types and sending system identities to segment and field extraction rules. Extends `sys_metadata`.

</td></tr><tr><td>

HL7 Parser Segment

 \[`sn_hl7_v2_parser_segment`\]

</td><td>

Defines individual HL7 segments \(for example, PV1, PID\) within a parser configuration, including the segment code and human-readable label. Extends `sys_metadata`.

</td></tr><tr><td>

HL7 Parser Field Map

 \[`sn_hl7_v2_parser_field_map`\]

</td><td>

Maps an HL7 field position within a parser segment to a dotted output path \(`field_name`\) in the message log's `parsed_data`, with an optional human-readable label. Supports field and component extraction. Extends `sys_metadata`.

</td></tr></tbody>
</table>## UI actions installed

The application installs two UI actions on the parser configuration form: **Parse Sample Payload**, which parses the configuration's sample payload and populates the parsed value on each field map; and **Clone**, which deep-copies a configuration and its segments and field maps to a new, inactive configuration.

## Demo parser configurations installed

The following parser configurations are installed only when you select **Load demo data** during installation. They are editable examples, not read-only records.

|Configuration|Description|
|-------------|-----------|
|HL7 v2.8 ADT^A01 — Admit|Demo parser configuration for ADT^A01 \(patient admit\) messages. Covers the EVN, PID, and PV1 segments.|
|HL7 v2.8 ADT^A02 — Transfer|Demo parser configuration for ADT^A02 \(patient transfer\) messages. Covers the EVN, PID, and PV1 segments.|
|HL7 v2.8 ADT^A03 — Discharge|Demo parser configuration for ADT^A03 \(patient discharge\) messages. Covers the EVN, PID, and PV1 segments.|
|HL7 v2.8 ADT^A08 — Update|Demo parser configuration for ADT^A08 \(patient information update\) messages. Covers the EVN, PID, and PV1 segments.|

## Scheduled jobs installed

None.

## System properties installed

None.

