---
title: Create an entity mapping for Urjanet
description: Create entity mappings for Urjanet because the Operational Sustainability Integration with Urjanet considers each Urjanet account meter as an entity.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management \(formerly ESG\) with Urjanet, Integrating ESG Management \(formerly ESG\) with other applications, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create an entity mapping for Urjanet

Create entity mappings for Urjanet because the Operational Sustainability Integration with Urjanet considers each Urjanet account meter as an entity.

## Before you begin

Ensure that you activate the sn\_esg\_urjanet plugin.

Role required: sn\_esg.admin

## About this task

Before starting with the integration, if you do not have entity mappings, you can create entity mappings so that the Urjanet account meter data can be mapped to an entity. The Operational Sustainability Integration with Urjanet considers the Urjanet account meters as entities. This procedure is optional.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Urjanet** &gt; **Entity Mapping**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_inv_xk2_fvb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record identifier

</td><td>

Urjanet meter ID.

</td></tr><tr><td>

Related record

</td><td>

Entity to be mapped.

</td></tr><tr><td>

Additional information

</td><td>

Field used to specify the information that must be filled in by the administrator. Certain fields such as **Entity class** and **Entity owner** must be manually filled by the user.

</td></tr><tr><td>

State

</td><td>

Review state. Based on the information provided in the **Additional information** field, the administrator must fill in the required information and then change the state of this field. The choices are as follows.-   **No review required**: Use this option when there are no fields to be filled in the entity record by the administrator.
-   **Review required**: Use this option if the administrator must fill some fields in the entity record.
-   **Reviewed**: Use this option if the administrator has already provided the information in the specified fields in the entity records.
 This field is automatically set to **No review required**. You must change the state to **Reviewed** after you provide the information.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Integrating ESG Management \(formerly ESG\) with Urjanet](../concept/integrating-esg-management-with-urjanet.md)

