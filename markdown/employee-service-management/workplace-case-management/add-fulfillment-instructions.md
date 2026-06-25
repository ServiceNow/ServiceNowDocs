---
title: Add Fulfillment instructions
description: Provide instructions to workplace agents on how to fulfill a workplace case. Add instructions for new workplace agents and for complicated workplace cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/workplace-case-management/add-fulfillment-instructions.html
release: australia
product: Workplace Case Management
classification: workplace-case-management
topic_type: task
last_updated: "2026-03-23"
reading_time_minutes: 4
breadcrumb: [Configure, Workplace Case Management, Workplace Service Delivery, Employee Service Management]
---

# Add Fulfillment instructions

Provide instructions to workplace agents on how to fulfill a workplace case. Add instructions for new workplace agents and for complicated workplace cases.

## Before you begin

Role required: sn\_wsd\_case.admin or sn\_wsd\_case.manager

## About this task

Add instructions for fulfilling a workplace case.

## Procedure

1.  Navigate to **All** &gt; **Workplace Case Management** &gt; **Workplace Case Management - Setup** &gt; **Fulfillment instructions**.

2.  Select **New**.

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

Knowledge article to support the instructions.Select the unlock knowledge articles icon \(\[Omitted image "unlock-icon.png"\] Alt text: Unlock Knowledge articles icon.\) to add an article. Select the lookup icon \(\[Omitted image "search-icon.png"\] Alt text: Lookup icon.\) to search for an article.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Result

The fulfillment instruction is added. The instruction is displayed in the workplace case records that match the specified conditions.

**Parent Topic:**[Configuring Workplace Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-case-management/workplace-case-mgmt-setup.md)

**Related topics**  


[Install Workplace Case Management]()

[Create a Workplace case template]()

[Create a Workplace task template]()

[Smart Assessment for Workplace Case and Task]()

[Automating seat assignment for new hires]()

[Configure Approval options]()

[Configure a Record producer]()

[Configuring a record producer for request edit]()

[Configuring a record producer for reservation]()

[Create an SLA Definition]()

[Create a Workplace service]()

[Add a workplace service item to a workplace service]()

[Create a workplace template configuration]()

[Create a workplace field mapping]()

[Configure an escalation rule]()

[Group similar workplace cases under a parent case]()

