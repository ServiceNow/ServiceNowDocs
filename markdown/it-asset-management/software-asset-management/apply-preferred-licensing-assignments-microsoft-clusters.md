---
title: Create preferred licensing assignments for Microsoft software products deployed on clusters
description: Create and define preferred licensing assignments for the Microsoft software products that are deployed on your hypervisor clusters. Use these assignments to specify whether you want to license each software product at either the physical host layer or virtual layer.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create preferred licensing assignments for Microsoft software products deployed on clusters

Create and define preferred licensing assignments for the Microsoft software products that are deployed on your hypervisor clusters. Use these assignments to specify whether you want to license each software product at either the physical host layer or virtual layer.

## Before you begin

Role required: sam\_admin

## About this task

**Note:** Preferred licensing assignments support only the per core and per core \(with CAL\) license metrics.

Preferred licensing assignments take precedence over the cost-based licensing optimizations that are recommended by default. By using a preferred licensing assignment, you can bypass these recommended licensing optimizations to better align with your organization's predetermined licensing strategy. For more information on cost-based licensing optimizations, see [Cost-based licensing optimization for Microsoft](../concept/cost-based-microsoft-cluster-licensing.md).

**Note:** You can alternatively license a Microsoft software product on a specific physical host, virtual machine \(VM\), user, or device by adding allocations directly to the corresponding software entitlement. ServiceNow recommends that you use either preferred licensing assignments only or allocations only on each hypervisor cluster. For more information on adding allocations to a software entitlement, see [Create entitlements in workspace](create-entitlements-workspace.md).

## Procedure

1.  On the page header of your ServiceNow instance, select **All**.

2.  In the menu navigation filter, enter `samp_device_license_assignment_list.do`.

    The Cluster License Assignments \[samp\_device\_license\_assignment\] table opens.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_zwr_v3q_jfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

License metric

</td><td>

License metric that you’re using to reconcile the Microsoft software product. Select either **Per core** or **Per core \(with CAL\)**.

</td></tr><tr><td>

Product version

</td><td>

Version of the Microsoft software product that you want to specify the licensing layer for.**Note:** If you don’t specify a product version, the Software Asset Management application automatically selects the most cost effective version for the licensing assignment.

</td></tr><tr><td>

Licensing layer

</td><td>

Layer that you want to license the Microsoft software product on. The options are **Physical** and **Virtual**.

</td></tr><tr><td>

Product

</td><td>

Microsoft software product that you want to specify the licensing layer for.

</td></tr><tr><td>

Cluster

</td><td>

Hypervisor cluster that you have deployed the Microsoft software product on.

</td></tr><tr><td>

Product edition

</td><td>

Edition of the Microsoft software product that you want to specify the licensing layer for.**Note:** If you don’t specify a product edition, the Software Asset Management application automatically selects the most cost effective edition for the licensing assignment.

</td></tr><tr><td>

Domain

</td><td>

Domain that the licensing assignment is available in.

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

The preferred licensing assignment is applied to the Microsoft software product.

**Parent Topic:**[Software Asset Management publisher pack for Microsoft](../concept/microsoft-publisher-pack.md)

