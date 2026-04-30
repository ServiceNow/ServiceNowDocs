---
title: Components installed with Case lines and workflows
description: Several types of components are installed with the Case lines and workflows application, including tables and roles.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Case lines and workflows, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Components installed with Case lines and workflows

Several types of components are installed with the Case lines and workflows application, including tables and roles.

## Tables installed with Case lines and workflows

<table id="table_vxx_wrp_lcc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

[Case Line](case-line-form.md)\[sn\_case\_line\]

</td><td>

The Case Line table stores case line item records that are created for parent cases. This table extends the Case table.The prefix for case line records is **CSL**.

</td></tr><tr><td>

[Case Line Task](case-line-task-form.md)\[sn\_case\_line\_task\]

</td><td>

The Case Line Task table stores the tasks related to case line items. This table extends the Case Task table.The prefix for case line task records is **CSLTASK**.

</td></tr><tr><td>

[Case Line Characteristic](case-line-characteristics-form.md)\[sn\_case\_line\_characteristic\]

</td><td>

The Case Line Characteristic form displays details about the product offering included in a case line.The prefix for case line characteristic records is **CSLC**.

</td></tr></tbody>
</table>## Roles

The Case Lines and workflows application includes roles that provide access to case line item and case line characteristic records. It also updates some existing roles to provide this same access.

<table id="table_nfd_kkj_jcc"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Includes roles

</th></tr></thead><tbody><tr><td>

sn\_case\_line.characteristic\_creator

</td><td>

This user can create case line characteristic records if they have access to the parent case line item record.

</td><td>

sn\_case \_characteristic\_viewer

</td></tr><tr><td>

sn\_case\_line.characteristic\_writer

</td><td>

This user can update case line characteristic records if they have access to the parent case line item record.

</td><td>

sn\_case \_characteristic\_viewer

</td></tr><tr><td>

sn\_case\_line.characteristic\_delete

</td><td>

This user can delete case line characteristic records if they have access to the parent case line item record.

</td><td>

sn\_case \_characteristic\_viewer

</td></tr><tr><td>

sn\_case\_line.characteristic\_viewer

</td><td>

This user can view case line characteristic records if they have access to the parent case line item record.

</td><td>

 

</td></tr><tr><td>

sn\_case\_line.characteristic\_report\_viewer

</td><td>

This user can view reports for the case line characteristic table if they have access to the parent case line item record.

</td><td>

 

</td></tr><tr><td>

Case task agent\[sn\_customerservice.case\_task\_agent\]

</td><td>

This is an existing role.The case task agent has read, write, and create access for case line tasks:

-   If the case task agent is the assigned user on the case task \(assigned\_to\).
-   If the case task agent belongs to the same assignment group as the assigned user.

The case task agent has read access to the following:

-   The parent order case and the case line items.
-   The case line characteristic if they have read access to the associated case line item.
-   Account and contact records for the parent order case.

The case task agent can update the work notes, comments, attachments, and watch list of the parent order case and the case line items.

</td><td>

-   sn\_customerservice.csm\_workspace\_user
-   sn\_customerservice.customer\_data\_viewer
-   sn\_customerservice.case\_contributor\_editor
-   sn\_csm\_case\_types.service\_definition\_viewer

</td></tr><tr><td>

Customer service agent\[sn\_customerservice\_agent\]

</td><td>

This is an existing role.The customer service agent role has read, write, and update permissions for the following tables:

-   Case Line
-   Case Line Task
-   Case Line Characteristic

</td><td>

For more information, see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md#section_p5t_gcr_3mb).

</td></tr></tbody>
</table>