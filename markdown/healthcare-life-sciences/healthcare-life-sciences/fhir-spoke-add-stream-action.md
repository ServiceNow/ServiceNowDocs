---
title: Add a FHIR stream action to a flow
description: Add an HL7 FHIR Spoke stream action to a flow to search a FHIR resource and process each matching record as it streams in, with pagination handled automatically by the spoke.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [data stream, pagination, Flow Designer, FHIR search]
---

# Add a FHIR stream action to a flow

Add an HL7 FHIR Spoke stream action to a flow to search a FHIR resource and process each matching record as it streams in, with pagination handled automatically by the spoke.

## Before you begin

Role required: a  authoring role, such as `flow_designer`.

The `HL7 FHIR` connection and credentials must be configured. See [Configure the HL7 FHIR connection and credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

## About this task

Stream actions use the data stream action template, which retrieves results page by page. You process the streamed items inside a "For Each" flow logic block so that the flow handles each resource without buffering the entire result set.

## Procedure

1.  In , open your flow or subflow and add an action step.

2.  Search for the stream action for the resource you want — for example, **Look up Organizations Stream** — and add it to the flow.

3.  Set the required **Page size** input.

    Page size controls how many resources the spoke requests per FHIR page. The spoke continues to request pages until the FHIR server returns no `next` link.

4.  Set any optional FHIR R4 search parameters to filter the results — for example, **name** or **active**.

    For the full set of search parameters per resource, see [HL7 FHIR Spoke actions reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

5.  Add a **For Each** flow logic block that iterates over the action's stream output.

6.  Inside the loop, map the resource data pills into your downstream steps — for example, to create or update records in your application.

7.  After the loop, check the action's **status code**, **error code**, and **error message** outputs to detect transport failures.


