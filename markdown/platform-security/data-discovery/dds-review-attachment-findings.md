---
title: Review attachment findings
description: Review attachment findings in Data Discovery Store
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/dds-review-attachment-findings.html
release: brazil
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Discovery scheduled discovery, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Review attachment findings

Review attachment findings in Data Discovery Store

## Before you begin

Role required: discovery.admin

## Procedure

1.  Navigate to **All** &gt; **Data Discovery** &gt; **Scheduled Discovery**.

2.  Select **Attachment Findings** in the right side navigation pane.

3.  Review the table entries.

<table id="table_m35_cwt_dcc"><thead><tr><th>

Column label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record

</td><td>

Discovered incident record. Each file scanned as part of a job generates a unique report.

</td></tr><tr><td>

Attachment

</td><td>

The attachment scanned as part of the job.

</td></tr><tr><td>

Attachment updated

</td><td>

The date the scanned attachment was last updated.

</td></tr><tr><td>

Job

</td><td>

The ID of the discovery job associated with this record.

</td></tr><tr><td>

Status

</td><td>

Status of the record.-   **No data**

No sensitive data was found.

-   **Data discovered**

Sensitive data was found.

**Note:** Refer to the **Discovery pattern** column for information on which specific data patterns were identified.

-   **Failed discovery**

The discovery job failed.

-   **Retry failed**

A retry of the discovery job failed.

</td></tr><tr><td>

Discovered pattern

</td><td>

Which, if any, established [Default data patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-discovery/default-data-patterns.md) or [Default NER data patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-discovery/default-ner-data-patterns.md) were discovered in the scan.

</td></tr></tbody>
</table>    **Warning:**

    Rollback is not supported for anonymization triggered from Attachment Findings.


