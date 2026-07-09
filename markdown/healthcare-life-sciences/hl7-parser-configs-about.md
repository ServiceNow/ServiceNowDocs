---
title: Parser configurations
description: Parser configurations define which HL7 segments and fields ServiceNow extracts from a received message and the output path where each value is written in the message log's parsed data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-parser-configs-about.html
release: australia
topic_type: concept
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [parser configuration, HL7 parser, parser config]
breadcrumb: [HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# Parser configurations

Parser configurations define which HL7 segments and fields ServiceNow extracts from a received message and the output path where each value is written in the message log's parsed data.

The HL7 parser is message-type agnostic — it does not know in advance what fields a given message contains. A parser configuration tells ServiceNow which segments to extract and the output path for each field. When a message is received, ServiceNow looks up the active configuration whose sending application, sending facility, HL7 version, message type, and trigger event match the incoming message header, then uses that configuration to drive parsing. Because each message type gets its own configuration, the same parser engine can handle ADT, ORU, ORM, or any other HL7 message type without modification.

## Configuration hierarchy

Parser configurations use a three-level hierarchy:

-   **Parser configuration \(`sn_hl7_v2_parser_config`\)**

    The top-level record. Identifies the HL7 version, message type, and trigger event the configuration applies to, along with the sending application and sending facility. An active-uniqueness business rule allows at most one active configuration per combination of these five fields.

-   **Parser segment \(`sn_hl7_v2_parser_segment`\)**

    Each segment record defines one HL7 segment to extract \(for example, PV1\). Segments have a human-readable label and an HL7 segment code. A parser configuration contains one or more segment records.

-   **Field map \(`sn_hl7_v2_parser_field_map`\)**

    Each field map record maps one HL7 field position within a segment to a dotted output path \(`field_name`\) in the parsed data, with an optional human-readable label. The field position is written in `field` or `field.component` notation — for example, `PV1.3.2` for the room within the patient location.


## Runtime lookup

The message log has no foreign key to the parser configuration table. Instead, ServiceNow performs a lookup at reception, matching the message's MSH fields \(sending application, sending facility, HL7 version, message type, trigger event\) against the parser configuration table to find the single active configuration for that key. If exactly one active configuration matches, the message is parsed with it; if none or more than one matches, the message is staged with status Failed and an AR acknowledgment.

## Demo configurations and cloning

Four demo parser configurations are available for ADT A01 \(Admit\), A02 \(Transfer\), A03 \(Discharge\), and A08 \(Update\), each covering the EVN, PID, and PV1 segments. They are installed only when you load demo data, and they are ordinary editable records. Edit one in place — replacing the placeholder sending application and facility with your interface's values — or use **Clone** to create a copy for hospital-specific field variations and relabeling.

