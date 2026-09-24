---
title: Update associated Decision tables for HAM flows
description: Update associated Decision tables for Hardware Asset Management \(HAM\) flows to trigger a new or customized HAM flow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/trigger-flow-ham.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Update associated Decision tables for HAM flows

Update associated Decision tables for Hardware Asset Management \(HAM\) flows to trigger a new or customized HAM flow.

## Before you begin

Role required: admin, decision\_table\_admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  Open a decision table that you want to update.

3.  On the flow page, select the Add icon \(\[Omitted image "add\_content\_icon.png"\] Alt text: Add icon\) in the Decision table section.

4.  Select **Add condition column**.

5.  In the NEW CONDITION COLUMN dialog box, fill in the conditions according to the conditions that you want to trigger the flow.

6.  Select **Done**.

    A new row is created and the condition shows up in the Decision table section.

7.  In the Flow column, select the flow that you have created.

8.  Select **Save**.

9.  Navigate to the Decisions \(sys\_decision\_question\) table and search the updated Decision table that you updated.

10. Update the **Order** field with a value less than 100.


**Parent Topic:**[Configuring Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/configuring-ham.md)

