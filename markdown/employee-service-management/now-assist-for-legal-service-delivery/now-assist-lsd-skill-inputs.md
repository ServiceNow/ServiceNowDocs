---
title: Skill inputs for Now Assist for Legal Service Delivery \(LSD\)
description: Get a quick overview of the skill inputs for Now Assist for Legal Service Delivery \(LSD\) so that you can configure how and when a skill is used.
locale: en-US
release: yokohama
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Now Assist, generative AI]
breadcrumb: [Configure, Now Assist for Legal Service Delivery \(LSD\), Legal Service Delivery, Employee Service Management]
---

# Skill inputs for Now Assist for Legal Service Delivery \(LSD\)

Get a quick overview of the skill inputs for Now Assist for Legal Service Delivery \(LSD\) so that you can configure how and when a skill is used.

Depending on the selected skill, you can configure inputs. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a summary.

Configure the variables of practice areas to be considered as inputs for legal request or matter summarization. To add variables, see [Configure variables for Now Assist summarization](../task/configure-variables-for-now-assist-summarization.md).

## Legal Request summarization

The Legal Request summarization skill includes the inputs that identify the table and fields that are used when a summary is generated.

**Note:** These fields are read-only.

<table id="table_case_summary_inputs"><thead><tr><th>

Input table

</th><th>

Input fields

</th></tr></thead><tbody><tr><td>

Legal Request \[sn\_lg\_ops\_request\]

</td><td>

-   Short description
-   Description
-   Priority
-   State
-   Additional comments
-   Work notes
-   Opened by

</td></tr></tbody>
</table>For requests in the Work in progress or closed state, the following additional related tables and fields are considered for summarization.

<table id="id_ljc_tfj_ycc"><thead><tr><th>

Input table

</th><th>

Input fields

</th></tr></thead><tbody><tr><td>

Task SLA-&gt;Task

</td><td>

-   Has breached
-   Breach time
-   SLA definition
-   Stage
-   Business time left
-   Condition for Stage

</td></tr></tbody>
</table>## Legal Matter summarization

The Legal Matter summarization includes the inputs that identify the table and fields that are used when a summary is generated.

**Note:** These fields are read-only.

<table id="table_pyv_15d_ddc"><thead><tr><th>

Input table

</th><th>

Input fields

</th></tr></thead><tbody><tr><td>

Legal Matter \[sn\_lg\_matter\_matter\]

</td><td>

-   Short description
-   Description
-   Priority
-   State
-   Additional comments
-   Work notes
-   Parent request

</td></tr><tr><td>

Legal Matter Task-&gt;Matter

</td><td>

-   Name
-   State
-   Order
-   Priority
-   Requested by
-   Phase
-   Matter
-   Event name
-   Assigned to
-   Due date
-   Additional comments
-   Work notes
-   Short description

</td></tr><tr><td>

Legal Request

</td><td>

Legal Request

</td></tr><tr><td>

Approvers

</td><td>

-   State
-   Approver
-   Comments
-   Approving

</td></tr></tbody>
</table>**Parent Topic:**[Configure Now Assist for Legal Service Delivery \(LSD\)](now-assist-lsd-configuring.md)

