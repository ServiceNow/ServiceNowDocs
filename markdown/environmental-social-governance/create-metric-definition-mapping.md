---
title: Create a metric definition mapping
description: Create a metric definition mapping to map the imported data from Urjanet with the correct metric definitions.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management \(formerly ESG\) with Urjanet, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create a metric definition mapping

Create a metric definition mapping to map the imported data from Urjanet with the correct metric definitions.

## Before you begin

Role required: sn\_esg.metrics\_manager

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Urjanet** &gt; **Metric Definition Mapping**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_inv_xk2_fvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record identifier

</td><td>

Name of the record that will be used to map data. For example, `Electric - Demand usage`.

</td></tr><tr><td>

Related record

</td><td>

Metric definition to which the record is mapped.

</td></tr><tr><td>

Additional information

</td><td>

Any notes or comments.

</td></tr><tr><td>

State

</td><td>

Review state. This field is used to provide information to sn\_esg.admin that there are a few entity mapping records to be reviewed and those records require the missing information. The choices are as follows.-   **No review required**: Use this option when there are no fields to be filled in the entity form by the admin.
-   **Review required**: Use this option if the admin must fill some fields in the record.
-   **Reviewed**: Use this option if the admin has already provided the information in fields.
 This field is automatically set to **No review required**.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Integrating ESG Management \(formerly ESG\) with Urjanet](../concept/integrating-esg-management-with-urjanet.md)

