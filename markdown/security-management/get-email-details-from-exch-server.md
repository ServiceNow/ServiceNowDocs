---
title: Create Compliance Search Action
description: The Create Compliance Search action creates a compliance search for emails in the designated Exchange server\(s\) using the search queries defined and returns the name of compliance search created.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Create Compliance Search Action

The Create Compliance Search action creates a compliance search for emails in the designated Exchange server\(s\) using the search queries defined and returns the name of compliance search created.

## Input variables

Input variables determine the initial behavior of the action.

<table id="table_pgm_tfy_jr"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

search\_query

</td><td>

Mandatory search query used to find emails in the Exchange Server across all mailboxes.

</td></tr><tr><td>

exchange Location

</td><td>

Mandatory location field used to search across location defined. Values are:-   All
-   Name of specific mailbox

</td></tr><tr><td>

targetId

</td><td>

Mandatory target host identifier field where the Exchange Server is located.

</td></tr></tbody>
</table>## Output variables

The output variables contain data that can be used in subsequent actions.

|Variable|Description|
|--------|-----------|
|response|Name of the compliance search created.|

## Exit Conditions

Possible exit conditions for this action are:

|Variable|Description|
|--------|-----------|
|Search Creation Failed|When search creation fails due to exception in exchange server.|
|Search Created Successfully|When search creation is successful.|
|Search Creation Failed due to a Parsing Error|When search creation fails due to parsing issue.|
|Error|When exception occurs in flow action.|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](../../../security-operations-common/concept/common-wf-activities.md)

