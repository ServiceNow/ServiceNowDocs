---
title: Configure a data source for digital forensics
description: Configure a data source a requester can select in a digital forensics request as the source of potentially evidential data.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Legal Digital Forensics, Legal Digital Forensics, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Configure a data source for digital forensics

Configure a data source a requester can select in a digital forensics request as the source of potentially evidential data.

## Before you begin

Role required: sn\_lg\_forensics.forensics\_config or admin

## Procedure

1.  Navigate to **All** &gt; **Legal Administration** &gt; **Digital Forensics Admin** &gt; **Data Sources**.

2.  Create or modify a data source.

    -   To create a data source, click **New**.
    -   To modify an existing data source, open the data source from the list.
3.  On the form, fill in the fields.

<table id="table_jn3_jrx_djb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Name of the data source.

</td></tr><tr><td>

Active

</td><td>

Option for marking the data source active.Only active data sources are available on the digital forensics request intake form in the Legal Service Portal.

</td></tr><tr><td>

Source detail fields

</td><td>

Fields that are applicable for the data source.The selected fields appear on the data source details form in a digital forensics request matter. Task owners provide details in these fields based on the fulfillment activities done by them. For more information, see [Create a task for a digital forensic legal matter](create-dft-matter-task.md).

 The field options in the list are populated from the Data Source Detail \[sn\_lg\_forensics\_search\_source\_detail\] table.

</td></tr></tbody>
</table>4.  Save the data source.

    -   Save a new data source by clicking **Submit**.
    -   Save the changes to an existing data source by clicking **Update**.

## What to do next

[Add fulfillment instructions and checklist for a data source](add-fulfillments-steps-dft.md). When a matter owner creates a task for the source in a legal matter, these instructions are pre-populated in the task. The users to whom the legal matter task is assigned can follow these instructions to resolve the task.

-   **[Add fulfillment instructions and checklist for a data source](add-fulfillments-steps-dft.md)**  
Add instructions for a data source that a task owner in a legal matter can follow to resolve the task.

**Parent Topic:**[Setting up Legal Digital Forensics](../concept/setting-up-legal-dft.md)

