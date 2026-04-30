---
title: Assign a library import task for compliance approval
description: Assign a library import task to the compliance managers assignment group by using the library import task form in the GRC: Policy and Compliance integrator application.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Assign a library import task for compliance approval

Assign a library import task to the compliance managers assignment group by using the library import task form in the GRC: Policy and Compliance integrator application.

## Before you begin

For this procedure, you must log in with the sn\_compliance.admin role first and then submit the library import task to be approved.

Role required: sn\_compliance.admin

## Procedure

1.  Navigate to **All** &gt; **Policy and compliance integrator** &gt; **Content integrator** &gt; **Library import task**.

    The library import task is displayed in the New state as shown in the following example.

    ![Library import task.](../image/lib-import-task-new-related-list.png "Library import task in the New state")

2.  On the form, fill in the fields.

<table id="table_k1z_j22_vsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Number for the library import task. The number is LIT0001001 in the example. This field is auto-populated.

</td></tr><tr><td>

Provider

</td><td>

Name of the provider. This field is auto-populated.

</td></tr><tr><td>

Batch

</td><td>

Content integration batch number. The number is CIB0001001 in the example. This field is auto-populated.

</td></tr><tr><td>

State

</td><td>

State of the library import task. This field is auto-populated.

</td></tr><tr><td>

Assignment group

</td><td>

Assignment group that the library import task is assigned to. Select **Compliance managers** group.

</td></tr><tr><td>

Approver

</td><td>

Approver for the library import task.

</td></tr><tr><td>

Assigned to

</td><td>

Assignment group that the task is assigned to.

</td></tr><tr><td>

Approver group

</td><td>

Approver group for the library import task.

</td></tr><tr><td class="sub-head" colspan="2">

Related lists

</td></tr><tr><td>

Authority document staging

</td><td>

Authority document staging records that are related to the library import task.

</td></tr><tr><td>

Citation staging

</td><td>

Citation staging records that are related to the library import task.

</td></tr><tr><td>

Control objective staging

</td><td>

Control objective staging records that are related to the library import task.

</td></tr><tr><td>

Content onboarding tasks

</td><td>

Provider import tasks that are related to the library import task. This task is created when the provider that is mentioned in the content integration batch is not found in the provider \(sn\_grc\_provider\) table.

 If the provider import task is created, the state of the library import task is updated to **Provider onboarding**. When the provider import task is completed, the state of the library import task is updated to **New**.

</td></tr></tbody>
</table>3.  Click **Update**.


## What to do next

To learn how to approve the library import task that is assigned to the compliance managers assignment group, see [Approve the library import task](approve-lib-import-task.md).

