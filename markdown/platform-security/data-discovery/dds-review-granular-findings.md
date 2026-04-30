---
title: Review granular findings
description: Review granular findings in Data Discovery Store
locale: en-US
release: zurich
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data Discovery scheduled discovery, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Review granular findings

Review granular findings in Data Discovery Store

## Before you begin

Role required: discovery.admin

## Procedure

1.  Navigate to **All** &gt; **Data Discovery** &gt; **Scheduled Discovery**.

2.  Select **Granular Findings** in the right side navigation pane.

3.  Review the table entries.

<table id="table_m35_cwt_dcc"><thead><tr><th>

Column label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record

</td><td>

Discovered record.

</td></tr><tr><td>

Table

</td><td>

Parent table of record.

</td></tr><tr><td>

Data Patterns

</td><td>

Pattern used to discover record.

</td></tr><tr><td>

Action

</td><td>

Action to take on findings. Select to change**Important:** The data\_privacy\_admin role is required to take the Anonymize action on a record.

-   **Review**

Record is pending review. This is assigned to new granular discoveries.

-   **Ignore**

No action will be taken on the record

-   **Anonymize**

Record will be anonymized.

</td></tr><tr><td>

Status

</td><td>

Status of record.-   **New**

Status assigned to finding when it is first reported

-   **Processed**

When user chosen action has been successfully applied on the finding

**Note:** Processed findings are store for 3 days in the Granular Findings table before deletion

-   **Manual Review**

When applying user chosen action has failed.

**Warning:** Findings in Manual Review should be deleted by users after taking appropriate actions.

</td></tr></tbody>
</table>    **Warning:**

    Rollback is not supported for anonymization triggered from Granular Findings.


