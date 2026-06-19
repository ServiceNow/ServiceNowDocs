---
title: Modify state decision tables in Care Team Operations for Biomed
description: Use Decision Builder to change the state mappings for cases and work orders in Care Team Operations for Biomed .
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-and-life-sciences/cto-biomed-modify-states.html
release: australia
product: Healthcare and Life Sciences
classification: healthcare-and-life-sciences
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Operations for Biomed, Healthcare Operations, Healthcare and Life Sciences]
---

# Modify state decision tables in Care Team Operations for Biomed

Use Decision Builder to change the state mappings for cases and work orders in Care Team Operations for Biomed .

\[Omitted image "cto-biomed-case-tstate.png"\] Alt text: Healthcare biomed case state sync map.

The Healthcare Biomed case state sync map displays all current mappings between Healthcare Biomed case and work order states.

To modify these state mappings, see **.**

To learn more about decisions tables, see  and .

The source table aligns with the input state and the destination table aligns with the output state.

These values can be found in the Dictionary Entry for the State field.

## Healthcare Biomed case state default values

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

