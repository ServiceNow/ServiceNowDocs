---
title: View and verify the import sets
description: Verify if your data is imported correctly from an external source. This verification enables you to identify if there were any errors during the data import.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management \(formerly ESG\) with Watershed, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# View and verify the import sets

Verify if your data is imported correctly from an external source. This verification enables you to identify if there were any errors during the data import.

## Before you begin

Role required: sn\_esg.program\_manager

## About this task

After the data is loaded to the ESG Management application from an external source, such as a spreadsheet, import sets are created where the state of each row is available. If there are errors during import, the state is updated as **Error**. If the data is imported, the state is updated as **Inserted**. You can also view the cause of the error in the error log. If the metric data is overridden, then the state is set to **Ignore**.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Import Sets**.

2.  Open the import set you want to verify.

3.  In the Import Set Rows section, view the state of each row.

    If you want to reload the data to check for errors, you must import your data again. Do not select **Reprocess** under Related Links in the Import set.

4.  To view the error log, select the Import Log section.


## What to do next

[Create a transform map](create-a-transform-map.md).

**Parent Topic:**[Integrating ESG Management \(formerly ESG\) with Watershed](../concept/integrate-esg-with-watershed.md)

