---
title: Create a case or account escalation template
description: Create a template for each type of case or account escalation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure escalation management, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a case or account escalation template

Create a template for each type of case or account escalation.

## Before you begin

Role required: sn\_crm\_foundation\_admin or sn\_crm\_escalation\_admin oradmin

## About this task

An escalation template determines how an escalation request is processed and includes the type of escalation \(case or account\); an approval list or workflow \(if approval is required\), and an escalation watch list.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Escalation Templates**.

2.  Click **New**.

3.  Fill in the fields on the Escalation Template form, as needed.

<table id="table_jks_bws_mf"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the escalation template.

</td></tr><tr><td>

Skip Escalation Approval

</td><td>

Enable this check box to skip the need for approval. If skipped, escalations are automatically approved.

</td></tr><tr><td>

Use Default Approval

</td><td>

Enable this check box to use the default approval flow \(**Escalation - Approval**\) provided with the escalation feature. If using the default approval flow, select an **Approval Group**.

</td></tr><tr><td>

Escalation Approval Flow

</td><td>

Staring with the Zurich release, the **Escalation Approval Flow** field is added to the Escalation Template \(sn\_customerservice\_escalation\_template\) table. Existing customers with customizations can still view the legacy **Escalation Approval Workflow** field. You can continue using your current escalation workflows or migrate to the new flows, depending on your customizations. **Note:** As per of this update:

-   The legacy Escalation-Approval workflow has been migrated to the low-code flow designer.
-   The Escalation Master–Approval workflow has been converted into a business rule.
Existing customers who haven’t customized these workflows should migrate to the new equivalent base system flows. Customers with customized versions might continue using them, but are encouraged to transition to the updated flows. Custom workflows remain supported, and customers can continue to create them as needed. However, any new business requirements must be implemented using the new or updated flow-based framework, rather than legacy workflows.

</td></tr><tr><td>

Add Case Assignment Group Manager to Approvers

</td><td>

For case escalation, enable this check box to add the manager of the case assignment group to the list of approvers.

</td></tr><tr><td>

Approval Group

</td><td>

If the **Use Default Approval** check box is enabled:-   For the **Case Escalation** type, you can select an additional approval group.
-   For the **Account Escalation** type, you must select an approval group.
 **Note:** If there are no approvers, escalation requests are automatically approved.

</td></tr><tr><td>

Escalation Approval Workflow

</td><td>

The workflow used to approve escalation requests. Use the default **Escalation-Approval** flow or select a different flow.

</td></tr><tr><td>

Type

</td><td>

The type of escalation:-   Case Escalation
-   Account Escalation


</td></tr><tr><td>

Escalation Watch List

</td><td>

Add users to the escalation template watch list. These users receive notifications for all escalations that use this escalation template. For an account escalation, the account team is automatically added to the watch list.

**Note:** Users can also be added to the watch list on the escalation record.

</td></tr></tbody>
</table>4.  Click **Submit**.


