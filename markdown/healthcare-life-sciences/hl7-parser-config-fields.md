---
title: Parser configuration fields
description: Field reference for the parser configuration, parser segment, and field map tables that define how the HL7 parser engine extracts message data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-parser-config-fields.html
release: australia
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [parser configuration fields, parser config, field map]
breadcrumb: [Components installed with HL7 v2.x Integration, HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# Parser configuration fields

Field reference for the parser configuration, parser segment, and field map tables that define how the HL7 parser engine extracts message data.

## Parser configuration \(`sn_hl7_v2_parser_config`\)

|Field|Type|Description|
|-----|----|-----------|
|`name`|String \(200\)|Display name for the configuration. An active-uniqueness business rule allows only one active configuration per composite key.|
|`sending_application`|String \(100\)|The sending application value \(MSH-3\) this configuration applies to. Part of the composite key. Mandatory.|
|`sending_facility`|String \(100\)|The sending facility value \(MSH-4\) this configuration applies to. Part of the composite key. Mandatory.|
|`hl7_version`|String \(20\)|The HL7 version \(MSH-12\) this configuration applies to. Part of the composite key. Mandatory.|
|`message_type`|String \(20\)|The message type \(MSH-9.1\) this configuration applies to. Part of the composite key. Mandatory.|
|`message_event`|String \(20\)|The trigger event \(MSH-9.2\) this configuration applies to. Part of the composite key. Mandatory.|
|`active`|Boolean|Whether this configuration is active and available for runtime lookup. Default: true.|
|`description`|String \(255\)|Optional administrator notes.|
|`sample_payload`|String \(4000\)|A raw HL7 v2.x test message used by the **Parse Sample Payload** action to populate the parsed value on each field map.|

## Parser segment \(`sn_hl7_v2_parser_segment`\)

|Field|Type|Description|
|-----|----|-----------|
|`parser_config`|Reference|Reference to the parent parser configuration record. Mandatory.|
|`name`|String \(200\)|Human-readable display name for the segment. Mandatory.|
|`segment`|String \(10\)|The HL7 segment code to extract \(for example, `PV1`, `EVN`\). Mandatory.|
|`active`|Boolean|Whether this segment is included in parser output. Default: true.|
|`description`|MultiLine String|Optional notes.|

## Field map \(`sn_hl7_v2_parser_field_map`\)

|Field|Type|Description|
|-----|----|-----------|
|`parser_segment`|Reference|Reference to the parent parser segment record. Mandatory.|
|`field_name`|String \(200\)|The dotted output path that names where the extracted value is written in the message log's `parsed_data` JSON \(for example, `patient.mrn` or `visit.dischargeDateTime`\). Validated for syntax, depth, and uniqueness within the configuration. Mandatory.|
|`field_label`|String \(200\)|Optional human-readable description of the mapping \(for example, Patient Medical Record Number\), shown in the **Parse Sample Payload** results.|
|`field_position`|String \(10\)|The HL7 field position to extract, in `field` or `field.component` notation \(for example, `3` for PV1.3, or `3.2` for the second component of PV1.3\). Mandatory.|
|`active`|Boolean|Whether this field map is included in parsing. Default: true.|
|`parsed_value`|String \(500\)|The value extracted by the most recent **Parse Sample Payload** run. Not copied when a configuration is cloned.|

