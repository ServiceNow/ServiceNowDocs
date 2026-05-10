---
title: Modify state decision tables in Care Team Operations for Environmental Services
description: Use Decision Builder to change the state mappings for cases and incidents work orders in Care Team Operations for Environmental Services.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Operations for Environmental Services, Healthcare Operations, Healthcare and Life Sciences]
---

# Modify state decision tables in Care Team Operations for Environmental Services

Use Decision Builder to change the state mappings for cases and incidents work orders in Care Team Operations for Environmental Services.

The Healthcare Environmental Services case state sync map displays all current mappings between Healthcare Environmental Services case and work order states.

To modify these state mappings, see [Modify decision table structure in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/format-decision-table-in-decision-designer.md)**.**

To learn more about decisions tables, see [Edit decision tables using draft authoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/edit-decision-tables-using-draft-authoring.md) and [Use decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/use-decision-tables.md).

The source table aligns with the input state and the destination table aligns with the output state.

These values can be found in the Dictionary Entry for the State field.

## Healthcare Environmental Services case state default values

|Label|Value|
|-----|-----|
|Cancelled|7|
|Open|10|
|Closed|3|
|Awaiting info|18|
|New|1|
|Work in Progress|2|
|Resolved|6|

## Work Order state default values

|Label|Value|Sequence|
|-----|-----|--------|
|Cancelled|7|10|
|Assigned|16|6|
|Awaiting Approval|11|1|
|Draft|1|0|
|Closed Incomplete|4|9|
|Qualified|10|4|
|Closed Complete|3|8|
|Awaiting Qualification|15|3|
|Scheduled|12|5|
|Approved|13|2|
|Work in Progress|18|7|

