---
title: Out Of Box Policies
description: The Cloud Services Catalog Out of the Box Policies comprise Approval, Naming, Lease and Quota Provisioning Policies.
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Out Of Box Policies

The Cloud Services Catalog Out of the Box Policies comprise Approval, Naming, Lease and Quota Provisioning Policies.

<table id="simpletable_mj5_24y_nxb"><thead><tr><th>

Provisioning Policies

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Approval

</td><td>

ServiceNow Approval action called via Policy Trigger, on specific occasions. Example: When a requester orders VM of type other than t2.micro and t2.nano, or when more than two extra disks are requested for certain catalog items.

</td></tr><tr><td>

Naming Policy

</td><td>

A good approach for resources deployed as part of a single request is to tag the resources with a common name, such as the stack's name. If the stack name follows standard convention, for easy ownership identification, and for age, that is useful. The naming policy that is shipped out of the box is enabled for all cloud catalog items. When the policy is active, a stack name is suggested in a particular naming format for Stack Name field in the form. The naming format uses a combination of initial letters of the requesters name, followed by the current date and time in mm dd hh mm format. Example: if the requester name is John Smith, and the date/time is 10:30 am on 15-May, the stack name is generated as 'js05151030'.

</td></tr><tr><td>

Lease Policy

</td><td>

Lease Policy is used to trigger de-provisioning of unused/unwanted stacks to save costs on cloud. The lease policy will de-provision active stacks after the lease period expires. A week prior to this, reminders are sent to stack owners mentioning the stack is expiring.

</td></tr><tr><td>

Quota Policy

</td><td>

Quota Policy is used to decide if a request which is run once quota is exceeded, should go to approval or to be aborted. See [Resource order controls for template-based cloud catalog items](../../cloud-management-v2/concept/resource-order-control-template-based-catalog.md)

</td></tr></tbody>
</table>**Parent Topic:**[Out Of Box Catalogs using Cloud Services Catalog](../concept/out-of-the-box-catalog-items.md)

