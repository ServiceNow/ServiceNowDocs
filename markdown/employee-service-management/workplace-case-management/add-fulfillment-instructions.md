---
title: Add Fulfillment instructions
description: Provide instructions to workplace agents on how to fulfill a workplace case. Add instructions for new workplace agents and for complicated workplace cases.
locale: en-US
release: xanadu
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Workplace Case Management, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Add Fulfillment instructions

Provide instructions to workplace agents on how to fulfill a workplace case. Add instructions for new workplace agents and for complicated workplace cases.

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## About this task

Add instructions for fulfilling a workplace case.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Fulfillment instructions**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_cpt_z4g_knb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the fulfillment instruction.

</td></tr><tr><td>

Table

</td><td>

Table containing workplace cases. The field is automatically set to the `Workplace Case` table.

</td></tr><tr><td>

Condition

</td><td>

Conditions that a workplace case should satisfy before you implement the fulfillment instruction. The instruction appears in the workplace case records which match this condition.-   To add a condition, select **Add Filter Condition**.
-   To add an "OR" condition, select **Add "OR" Clause**.


</td></tr><tr><td>

Active

</td><td>

Option to activate the fulfillment instruction.

</td></tr><tr><td>

Order

</td><td>

The order in which the instruction is followed when there are multiple fulfillment instructions for a workplace case record.

</td></tr><tr><td>

Instruction

</td><td>

Fulfillment instructions to follow. Use the formatting options to change the style of the content.

</td></tr><tr><td>

Knowledge articles

</td><td>

Knowledge article to support the instructions.Select the unlock knowledge articles icon \(![Unlock Knowledge articles icon.](../../wsd-reservation-management/image/unlock-icon.png)\) to add an article. Select the lookup icon \(![Lookup icon.](../image/search-icon.png)\) to search for an article.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Result

The fulfillment instruction is added. The instruction is displayed in the workplace case records that match the specified conditions.

**Parent Topic:**[Configure Workplace Case Management](../concept/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management](install-workplace-case-mgmt.md)

[Create a Workplace case template](wsd-case-template.md)

[Create a Workplace task template](wsd-task-template.md)

[Configure Approval options](config-approval-optns.md)

[Configure a Record producer](wsd-create-record-producer.md)

[Configuring a record producer for request edit](../concept/config-case-edit-rp.md)

[Configuring a record producer for reservation](../concept/config-reservation-rp.md)

[Configure workplace services topic](configure-workplace-services.md)

[Create an SLA Definition](create-sla-defn-case-mgmt.md)

[Create a Workplace service](create-workplace-service.md)

[Add a workplace service item to a workplace service](add-workplace-service-items.md)

[Create a workplace template configuration](create-workplace-template-confguration.md)

[Create a workplace field mapping](create-workplace-field-mapping.md)

[Configure an escalation rule](configure-escalation-rule.md)

[Group similar workplace cases under a parent case](group-similar-workplace-cases.md)

