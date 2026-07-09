---
title: Test a parser configuration with a sample payload
description: Run a parser configuration against a sample HL7 v2.x message to confirm that it extracts the segments and fields you expect before you use it in a workflow. The parsed values appear on the configuration's field maps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hl7-parse-sample-payload.html
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [parse sample payload, parser configuration, field map, test parser, HL7 v2.x]
breadcrumb: [Connect your integration engine to ServiceNow, HL7 v2.x Integration, Healthcare Integrations, Healthcare and Life Sciences]
---

# Test a parser configuration with a sample payload

Run a parser configuration against a sample HL7 v2.x message to confirm that it extracts the segments and fields you expect before you use it in a workflow. The parsed values appear on the configuration's field maps.

## Before you begin

Role required: HL7 Integration Administrator \(`sn_hl7_v2.admin`\).

The parser configuration you want to test, including its segment and field-map definitions, must already exist.

## About this task

A parser configuration defines which HL7 segments and fields to extract from a message and the output path for each value in the parsed data. Before relying on a configuration, test it against a representative sample message to verify that each field map resolves to the value you expect. The test reads the sample payload stored on the configuration and populates the parsed value on each field map, without affecting any live message processing.

## Procedure

1.  Navigate to **All** &gt; **HL7 Integration** &gt; **Parser Configurations** and open the parser configuration you want to test.

2.  Confirm that the configuration has a sample payload defined.

    If no sample payload is present, add a representative HL7 v2.x message in ER7 format before testing.

3.  In **Related Links** at the bottom of the form, click **Parse Sample Payload**.

4.  Open a segment's field-map related list — for example, the PID segment — and verify that the **Parsed value** on each field map matches the corresponding value in the sample message.

    \[Omitted image "sn\_hl7\_v2-04-parse-sample-payload-04-pid-field-maps-parsed.png"\] Alt text: PID segment field maps showing populated parsed values after running Parse Sample Payload


## Result

The field maps display the values parsed from the sample payload, confirming that the configuration extracts the expected fields. If a parsed value is empty or incorrect, adjust the segment or field-map definition and parse the sample payload again.

