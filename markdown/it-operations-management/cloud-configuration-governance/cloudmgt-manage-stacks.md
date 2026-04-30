---
title: Manage a stack
description: Use the Stack Details page to view details and status for a stack and to perform life-cycle operations on a stack.
locale: en-US
release: xanadu
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Cloud User Portal, Cloud Provisioning and Governance, ITOM Optimization, IT Operations Management]
---

# Manage a stack

Use the Stack Details page to view details and status for a stack and to perform life-cycle operations on a stack.

## Before you begin

Role required: sn\_cmp.cloud\_service\_user

## Procedure

1.  Use one of the following methods to open the **Stack Details** page:

    -   Click **Stacks** on the toolbar.
    -   Use the **Search** text box to search for the stack.
    -   On the home page, click a stack in the **Recent Stacks**, or the **Stack Health** section.
    -   On the home page, click **Manage Stacks**.
    By default, all stacks in all service categories are listed.

2.  In the **Stacks** list, select a stack category, and then click a stack **Name**.

    The **Stack Details** page displays the following information:

    ![Stack details](../image/stack-details.png)

    -   Breadcrumb navigation
    -   Name of the stack. Click **View Dependency** to view the dependency map for the stack, **Manage Stack** to view the resources, properties, and activities of the stack, and **Track Operations** to view the list of lifecycle operations performed on the stack and its resources.
    -   Status information
    -   List of all resources in the stack. Click a resource to view details in the **Properties** section. Color codes indicate status of the stack:
        -   Green: On/Active.
        -   Yellow: Turned off or Processing.
        -   Red: Terminated or Error.
    -   List of the stack properties. Some properties are set in the stack request form and others are set by policy
    -   Activities associated with the stack. Click a tab to view:
        -   Change requests that are associated with the stack. See [Track a change request](cloudmgt-track-change-request.md).
        -   Incidents that were raised for the stack. See [Submit an incident for a stack](cloudmgt-submit-incident.md) and [Track an incident](cloudmgt-track-incident.md).
        -   Cloud events that are associated with the stack. Cloud Events appears only when a resource is selected. See [View cloud events](cloudmgt-view-cloud-events.md).
        -   Catalog tasks associated with the stack. See [Resubmit a failed stack request](../../cloud-management-v2/task/resubmit-failed-request.md).
        -   Upcoming business hours schedule operations associated with the stack. You can skip an upcoming operation or cancel a schedule associated with the stack. See [Modify business schedule operations for a stack](cloudmgmt-modify-business-schedule.md).
    -   Operations you can perform on a stack. See [Perform a life-cycle operation on a stack or resource](cloudmgt-lifecycle-operation.md).
    -   Text box used to search the Cloud User Portal for stacks, resources based on types, stack requests, change requests, incidents, keys, and catalog items.
<table id="table-activities"><tbody><tr><td>

Name

</td><td>

Name that you specified when requesting the stack.

</td></tr><tr><td>

Stack Status

</td><td>

Current status of the stack:-   Active \(provisioned stacks\)
-   Terminated \(deprovisioned stacks\)
-   Unmanaged \(discovered stacks\)
-   Error \(errored stacks\)
-   Processing \(stacks being processed\)


</td></tr><tr><td>

Assigned To

</td><td>

Owner of the stack configuration. This drives the access controls and views in cloud portal.

</td></tr><tr><td>

Cloud Account

</td><td>

Cloud account that the stack is associated with.

</td></tr><tr><td>

Service Request Item

</td><td>

Record created in Request Item table when you ordered the catalog which resulted in this stack.

</td></tr><tr><td>

Blueprint

</td><td>

Blueprint with which the stack is associated.

</td></tr><tr><td>

Owned by

</td><td>

User name of the requester.

</td></tr><tr><td>

Owner Group

</td><td>

Name of the group the owner of the stack belongs to.

</td></tr><tr><td>

Schedule

</td><td>

The schedule is associated with the stack.

</td></tr><tr><td>

Output

</td><td>

Details specific to ARM/CFT stacks, such as the URL of an application, names, or locations of any resources created.

</td></tr><tr><td>

Updated

</td><td>

Date and time the stack details were last updated.

</td></tr><tr><td>

Created

</td><td>

Date and time the stack was requested.

</td></tr><tr><td>

End Date

</td><td>

Date and time the stack terminates \(unprovisioned\).

</td></tr></tbody>
</table>
