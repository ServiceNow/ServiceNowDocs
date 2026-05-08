---
title: Modify state decision tables in Care Team Operations for Facilities
description: Use Decision Builder to change the state mappings for cases and incidents work orders in Care Team Operations for Facilities.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Operations for Facilities, Healthcare Operations, Healthcare and Life Sciences]
---

# Modify state decision tables in Care Team Operations for Facilities

Use Decision Builder to change the state mappings for cases and incidents work orders in Care Team Operations for Facilities.

The Healthcare Facilities case state sync map displays all current mappings between Healthcare Facilities case and work order states.

To modify these state mappings, see Modify decision table structure in Workflow Studio**.**

To learn more about decisions tables, see Edit decision tables using draft authoring and Use decision tables.

The source table aligns with the input state and the destination table aligns with the output state.

These values can be found in the Dictionary Entry for the State field.

## Healthcare Facilities case state default values

|Label|Value|
|-----|-----|
|Canceled|7|
|Open|10|
|Closed|3|
|Awaiting info|18|
|New|1|
|Work in Progress|2|
|Resolved|6|

## Work Order state default values

|Label|Value|Sequence|
|-----|-----|--------|
|Canceled|7|10|
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

