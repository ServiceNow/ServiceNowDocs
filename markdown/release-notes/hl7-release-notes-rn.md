---
title: HL7 v2.x Integration release notes
description: The ServiceNow HL7 v2.x Integration application works alongside the HL7 v2.x Inbound REST API to provide a standards-compliant endpoint for receiving HL7 v2.x messages from integration engines, a configurable parser for converting raw messages into structured workflow data, and out-of-the-box support for common ADT message types. HL7 v2.x Integration is a new application in the Australia release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/hl7-release-notes-rn.html
release: australia
topic_type: reference
last_updated: "2026-05-11"
reading_time_minutes: 2
keywords: [HL7, HL7 v2, integration, ADT, parser, message log]
breadcrumb: [Healthcare and Life Sciences release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# HL7 v2.x Integration release notes

The ServiceNow® HL7 v2.x Integration application works alongside the HL7 v2.x Inbound REST API to provide a standards-compliant endpoint for receiving HL7 v2.x messages from integration engines, a configurable parser for converting raw messages into structured workflow data, and out-of-the-box support for common ADT message types. HL7 v2.x Integration is a new application in the Australia release.

## HL7 v2.x Integration highlights for the Australia release

-   Works alongside the HL7 v2.x Inbound REST API to receive HL7 v2.x messages from EHR systems over HTTP and return standards-compliant acknowledgment responses.
-   Receive raw HL7 v2.x messages directly in ServiceNow and automatically return standards-compliant ACK responses — with no custom scripting on the integration engine side.
-   Parse raw HL7 v2.x messages into structured JSON on the message log using a configurable, no-code parser, enabling hospital workflow automation without HL7 v2.x expertise.
-   Demo parser configurations for ADT A01 \(Admit\), A02 \(Transfer\), A03 \(Discharge\), and A08 \(Update\) provide ready-to-edit starting points for the most common hospital ADT workflows.

## HL7 v2.x Integration features

-   **[HL7 v2.x Inbound REST API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/hl7-inbound-api.md)**

    The HL7 v2.x Inbound REST API receives inbound HL7 v2.x ADT messages from EHR systems over HTTP and returns standard HL7 v2.x acknowledgment responses. It implements the HAPI HL7-over-HTTP convention, accepting raw pipe-delimited ER7 message bodies and processing them against configured parser profiles.

-   **HL7 message log**

    Every inbound HL7 v2.x message is stored with its raw payload, ACK response, message metadata \(type, trigger event, sending application and facility, message control ID\), and processing status. Metadata fields are queryable and available as Flow Designer trigger conditions.

-   **Parser configurations**

    When a message is received, ServiceNow parses it with the matching parser configuration and writes the extracted values to the message log record's structured JSON \(`parsed_data`\). Parser configurations define which segments and fields to extract and the output path for each value.

-   **Demo parser configurations**

    Demo parser configurations for ADT A01, A02, A03, and A08 are available when you load demo data, covering the EVN, PID, and PV1 segments. They are editable, and you can clone them for hospital-specific customization.


## Activation information

HL7 v2.x Integration is distributed as a separate application through the ServiceNow Store. Request the application from the ServiceNow Store and install it to activate it on your instance.

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    HL7 v2.x Integration \(`com.sn_hl7_v2`\): Provides native HL7 v2.x message reception, parsing, and workflow integration capabilities for ServiceNow Healthcare Operations.


## Related ServiceNow applications and features

-   ****

    HL7 v2.x message data parsed by HL7 v2.x Integration can drive workflows in Healthcare Operations applications such as bed management, room turnover, equipment coordination, and scheduling.

-   ****

    Provides the core Healthcare and Life Sciences data model and service management framework that HL7 v2.x Integration extends. Parsed HL7 v2.x message data can trigger and update healthcare service records within the Healthcare and Life Sciences Service Management platform.


**Parent Topic:**[Healthcare and Life Sciences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/healthcare-life-sciences-rn-landing.md)

