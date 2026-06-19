---
title: Modify state decision tables in Care Team Operations for Healthcare IT
description: Use Decision Builder to change the state mappings for cases and incidents in Care Team Operations for Healthcare IT.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-and-life-sciences/cto-it-modify-decision-tables.html
release: australia
product: Healthcare and Life Sciences
classification: healthcare-and-life-sciences
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Care Team Operations for Healthcare IT, Healthcare Operations, Healthcare and Life Sciences]
---

# Modify state decision tables in Care Team Operations for Healthcare IT

Use Decision Builder to change the state mappings for cases and incidents in Care Team Operations for Healthcare IT.

\[Omitted image "cto-it-state-sync-1.png"\] Alt text: HCIT state sync map

The HCIT case state sync map displays all current mappings between Healthcare IT case and incident states.

To modify these state mappings, see **.**

To learn more about decisions tables, see  and .

The source table aligns with the input state and input sub state and the destination table aligns with the output state.

For example, when the incident state is changed to Closed \(choice value 7\), a lookup is performed using this decision table to ensure that the value in the destination IT case table is also set to Closed \(choice value 3\).

These values can be found in the Dictionary Entry for the State field.

## Healthcare IT case state default values

|Label|Value|Sequence|
|-----|-----|--------|
|Open|10|3|
|Cancelled|7|8|
|Draft|0|-1|
|Awaiting info|18|4|
|Resolved|6|5|
|New|1|0|
|Closed|3|4|

## Incident state default values

|Label|Value|Sequence|
|-----|-----|--------|
|New|1|1|
|In Progress|2|2|
|On Hold|3|3|
|Resolved|6|6|
|Closed|7|7|
|Canceled|8|8|

