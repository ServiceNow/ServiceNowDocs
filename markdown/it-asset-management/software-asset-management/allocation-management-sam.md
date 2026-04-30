---
title: Allocation management on Software Asset Management
description: Software Asset Management \(SAM\) offers optimal license assignment confirming that licensing entities are allocated according to the available entitlements.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-02-05"
reading_time_minutes: 7
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Allocation management on Software Asset Management

Software Asset Management \(SAM\) offers optimal license assignment confirming that licensing entities are allocated according to the available entitlements.

For example, Software Asset Management determines the most cost-effective license assignment for a specific host or virtual machine based on the available Microsoft SQL Server Standard or Enterprise entitlements. Software Asset Management streamlines the licensing process and helps you optimize costs by selecting the most efficient licensing options. Allocation management saves your time, reduces the risk of compliance issues, and unnecessary expenses.

License allocations enable you to prioritize license assignments for specific hosts, virtual machines, users, devices, and more, according to the licensing strategy of your organization. You can override the default license assignment so that your unique needs are met.

There are several ways to manage allocations and here are a few scenarios to help you use allocation management effectively.

-   Using allocation to license entities with other licenses

    License a device or user with a different license than the one assigned by Software Asset Management for a flexible license management process.

-   Locking license assignment by creating allocations

    Lock a license assignment for the same license consumption to occur every time the reconciliation runs to maintain consistency and avoid unexpected changes.

-   Removing unnecessary allocations

    Remove unnecessary allocations when they’re no longer needed for an efficient license management process.

-   Copying allocations

    SAM Managers can copy allocations from one entitlement to another which helps to apply the same allocation strategy across multiple entitlements, saving time and maintaining consistency.

-   Overriding license assignment

    Override Software Asset Management license assignment and allocate the license to the Host or the Virtual Machine \(VM\) in a Hypervisor Cluster.


## Licensing entities with other licenses

Software Asset Management automatically licenses entities such as a virtual machine with Microsoft SQL Server Microsoft Standard license based on cost effectiveness. But the SAM Manager wants to change the license assignment to SQL Server Enterprise according to the licensing strategy of the organization.

SAM Manager analyzes the license consumption of a particular entity, Cluster A- VM 13, and verifies that it has been consumed by SQL Server Standard and the software installed on this virtual machine is also SQL server Standard.

![License consumption of Cluster-A-VM-13.](../image/licenses-required-vm-13.png)![The software installed on this virtual machine is SQL Server Standard.](../image/sql-server-standard-vm-13.png)

But according to the licensing strategy of the organization, SAM Manager wants to assign the SQL Server Enterprise license to this entity. In this scenario, the SAM Manager or SAM Admin can add an allocation to the SQL Server Enterprise entitlement, which would allocate SQL Server Enterprise licenses to the entity.

**Note:** You don't have to remember the quantity of licenses to allocate. Software Asset Management automatically determines the licenses required for the entity, so the SAM Manager or SAM Admin can allocate a license.

After reconciliation, Cluster A- VM 13 has consumed licenses from SQL Server Enterprise. Four rights have been consumed wherein only 1 was allocated. You can also verify that the **Allocated in use** field to confirm that the added allocations are consumed.![Four rights have been consumed wherein only 1 was allocated.](../image/licenses-reqd-vm-13.png)

For more information about the allocation fields, see [Software model results license metric results fields](../reference/license-metric-results-fields.md).

In the Cluster A- VM 13 Software installation list, the installed software is SQL Server Standard. However, the Software model result indicates that the entity is being consumed by the SQL Server Enterprise software model.![The entity is being consumed by SQL Server Enterprise software model.](../image/allocation-final-vm-13.png)

The use case of prioritizing certain entities to consume a specific license over others can be extended to many other scenarios. For example, software suites can be prioritized to consume licenses first, or licensing a particular device with a different license metric over others.

## Locking license assignments

Lets say, the SAM Manager is happy with the assignment of license consumption performed by the Software Asset Management application. You can view License Metric Results and Remediation Options for a software model result from a Product Result record. On the License Metric Results page, the **Not allocated in use** column shows the number of rights that are used to license installations, but not allocated. When this value is greater than zero, remediation options **Create Allocations** and **Remove Unallocated** are displayed on the Remediation Options page. For more information, see [View software model results](../task/t_ViewSWModelResults.md).

![Remediation options for a SQL server](../image/main-remediation-options.png)

The **Create Allocations** remediation option enables the SAM Manager to lock assignments for all entities \(device/user\) or individual entity, so that during future reconciliation runs, the license consumption occurs exactly as previously performed.

![Create Allocations Remediation Option](../image/remediation-options.png)

The allocation will be added to the entitlement immediately after performing the remediation action. For more information about remediation options, see [View software model results](../task/t_ViewSWModelResults.md).

## Overriding license assignment to a host or VM

Lets say, there’s a SQL Server Enterprise license, and Software Asset Management has optimized licensing by assigning it to the virtual layer. If your license strategy involves assigning licenses to the host layer, you can adjust this approach.

To override the license assignment:

1.  In the Software Asset Workspace, navigate to **License Operations** &gt; **Licensing**.
2.  Select **Software entitlements**.
3.  Select the software entitlements for SQL Server. For example, select the Microsoft SQL Server 2017 Enterprise software entitlement.![Licensing Software entitlements.](../image/select-software-entitlement.png)
4.  Select the **Device Allocations** tab and then select **New**.
5.  Add the Device Allocations details. When allocating license to the Host or VM, based on the value provided in the **Quantity** field, the Software Asset Management application determines the core count based on the following criteria:
    -   If an exact number of cores isn’t provided, the Software Asset Management application automatically uses the actual core count of a machine for licensing purposes.
    -   If fewer cores than the actual machine is provided, the Software Asset Management application counts the exact number of cores present on the machine for licensing purposes.
    -   If more cores than the actual machine is provided, the Software Asset Management application uses the number you entered. However, the surplus is marked as Allocated not in use for licensing.

Lets allocate one license to the Microsoft SQL Server 2017 Enterprise Software entitlement, and save the entitlement, then run software reconciliation. For more information, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).![Device allocation to the entitlement](../image/entitlement-device-allocation.png)

Cluster 103 has 3 hosts each with 16 cores. In the previous example, the license allocation was adjusted to 1 for one entitlement. The Software Asset Management application assigns the host the correct licenses based on the number of cores.![Licenses allocated to the hosts](../image/entitlement-allocated-to.png)

The Software Asset Management Manager can check the license usage by the cluster. To check the license usage, navigate to **License usage** &gt; **License Metrics Result** &gt; **Licenses Required By**. Select the **Is Virtual** column value as **false** to verify that it’s licensed at the Host layer.

![Is Virtual column in the Licenses Required By table.](../image/licenses-required-by.png)

You can customize the Licenses Required By page by adding columns such as **Allocated in use**, **Not allocated in use**, and **Allocation**. The Allocated in use column displays the count of rights that are allocated and are used to license installations. For more information about license usage by the cluster, see [View calculations for your licenses in workspace](../task/licenses-required-workspace.md).

![Licenses Required By table displaying the allocated licenses.](../image/customized-licenses-required-table-view.png)

When allocating software licenses, follow the licensing rules supported by the publisher.

**Important:**

-   Allocation isn’t required for the subscription products.
-   According to Microsoft licensing rules, host layer licensing isn’t supported for SQL Server Standard. When you allocate the license at host level, the allocated license number is shown in the **Allocated not in use** column.
-   Avoid allocating licenses to a cluster directly. Instead, allocate them to the hosts or VMs within the cluster. When you allocate a license to a cluster, the allocated license number is shown in the **Allocated not in use** column.
-   When the **Allocated not in use** column value is greater than zero, the **Remove Allocations** remediation option is automatically created for each unique license metric in the software model.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

