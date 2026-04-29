---
title: Using Operational Technology Change Management to optimize your production process
description: The Operational Technology Change Management application enables your team members to work collaboratively on changes to operational technology \(OT\) devices or industrial equipment configurations. These changes include any optimizations, alterations in the production process, or vulnerability fixes.
locale: en-US
release: australia
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Operational Technology Change Management, Operational Technology]
---

# Using Operational Technology Change Management to optimize your production process

The Operational Technology Change Management application enables your team members to work collaboratively on changes to operational technology \(OT\) devices or industrial equipment configurations. These changes include any optimizations, alterations in the production process, or vulnerability fixes.

## Operational Technology Change Management overview

By using the Operational Technology Change Management application, you can manage your OT change requests separately from your Information Technology \(IT\) change requests. You can separate OT change requests from IT change requests by the network type and you can manage OT change requests per site.

The following examples show how to apply Operational Technology Change Management to your organization:

-   An OT remediation owner, who's responsible for fixing vulnerabilities on OT devices, wants to initiate a change to fix a group of vulnerabilities.
-   An OT technician, who's responsible for OT configurations and plant engineering activities, wants to execute a change to fix a malfunctioned robotic arm on the industrial floor.
-   A plant head, who's responsible for overall production activity, wants to review and approve a change requested by the engineering team.

## OT change requests

OT change requests occur when there’s a disruption in service from an OT device on an OT network. In some cases, the OT device may not be known when the change request is created. When you create an OT change request from the Industrial Workspace, the change request is automatically assigned a Network Type of **OT**. This attribute is used to distinguish an OT change request from an IT change request. This field isn’t displayed by default. For more information about OT devices, see [OT device related items and related lists](../../mftg-manufacturing-oper-tech-mgr/reference/ot-assets-related-links-and-lists.md).

For more information about how to create an OT change request, see [Create a change request](../task/create-ot-change-request.md).

## Separating an IT and OT change

When the Operational Technology Change Management application is installed on your instance, you can choose a Network Type of **IT**, **OT**, or **None**. New change requests are assigned a Network Type of **None** by default.

## Operational Technology Change Management model state transitions

The following tables list the Operational Technology Change Management model state transitions for both the Basic OT Change Model and the Advanced OT Change Model. For more information about the OT Change Models, see [Select a change model to fulfill change requests](../task/select-change-model.md).

<table id="table_ifw_jdj_yxb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

An OT change request is initiated.

</td></tr><tr><td>

Plan

</td><td>

The OT change request is analyzed with the following criteria:-   Justification
-   Implementation plan
-   Risk and impact analysis
-   Backout plan
-   Test plan
-   Schedule the change

</td></tr><tr><td>

Implementation

</td><td>

The change is performed on the targeted OT device.

</td></tr><tr><td>

Closed

</td><td>

The change record is closed after the change is completed.

</td></tr><tr><td>

Canceled

</td><td>

The change record is canceled and the change isn’t applied to the OT device.

</td></tr></tbody>
</table><table id="table_bt4_kdj_yxb"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New

</td><td>

An OT change request is initiated.

</td></tr><tr><td>

Plan

</td><td>

The OT change request is analyzed with the following criteria:-   Justification
-   Implementation plan
-   Risk and impact analysis
-   Backout plan
-   Test plan
-   Schedule the change

</td></tr><tr><td>

Approve

</td><td>

The reviewers approve or deny the OT change request.

</td></tr><tr><td>

Implementation

</td><td>

The change is performed on the targeted OT device.

</td></tr><tr><td>

Post-Implementation Review

</td><td>

Add additional OT change tasks if needed and perform the following checks:-   Electrical check
-   Network check
-   Quality check
-   Safety check

</td></tr><tr><td>

Closed

</td><td>

The change record is closed after the change is completed.

</td></tr><tr><td>

Canceled

</td><td>

The change record is canceled and the change isn’t applied to the OT device.

</td></tr></tbody>
</table>**Parent Topic:**[Exploring Operational Technology Change Management](exploring-operational-technology-change-mgt.md)

