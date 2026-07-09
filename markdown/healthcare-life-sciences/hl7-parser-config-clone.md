---
title: Clone and customize a parser configuration
description: Clone a demo parser configuration to create a customizable copy that you can modify for hospital-specific field variations and relabeling.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-parser-config-clone.html
release: australia
topic_type: task
last_updated: "2026-05-11"
reading_time_minutes: 1
keywords: [parser configuration, clone parser config, customize parser]
breadcrumb: [Connect your integration engine to ServiceNow, HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# Clone and customize a parser configuration

Clone a demo parser configuration to create a customizable copy that you can modify for hospital-specific field variations and relabeling.

## Before you begin

Role required: `sn_hl7_v2.admin`

## About this task

The demo parser configurations are editable records. You can edit one in place or, to keep the original example intact, clone it and modify the copy — for example, to add hospital-specific field labels, include additional fields, or adjust field positions. Cloning is also a quick way to create a variant for a different sending facility.

**Important:** Programmatic field keys in your clone remain stable even if you change field labels. Existing scripts and flows that reference field keys by name continue to work after relabeling.

## Procedure

1.  Navigate to **All** &gt; **HL7 Integration** &gt; **Parser Configurations**.

2.  Open the demo configuration you want to clone.

3.  Click **Clone**.

4.  In the **Name** field, enter a descriptive name for your configuration that identifies the sending facility or customization purpose.

5.  Update the **Sending application** and **Sending facility** fields to match the values in MSH-3 and MSH-4 of the messages sent by your integration engine.

    The combination of sending application, sending facility, HL7 version, message type, and trigger event must be unique across all active configurations.

6.  Click **Save**.

7.  To add, remove, or modify segment definitions, open the **Segments** related list and make changes as needed.

8.  To modify field labels or required and optional designations, open a segment record and update the field map entries in its **Field Maps** related list.

    **Note:** Changing a field label does not change the field's programmatic key. Flows and scripts that reference the key continue to work without modification.

9.  Set the configuration to **Active** and click **Save**.


## Result

Your custom parser configuration is active. When ServiceNow receives a message matching its sending application, sending facility, HL7 version, message type, and trigger event, it uses your configuration to extract fields into the message log's parsed data.

**Related topics**  


[Parser config fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-parser-config-fields.md)

[Test a parser configuration with a sample payload](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/hl7-parse-sample-payload.md)

