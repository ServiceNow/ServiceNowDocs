---
title: Create licenses for distributed software using CSD 2.0
description: Licenses are associated with the software model and must be created if you want to track the license for software deployed by CSD 2.0.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client Software Distribution 2.0 application, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Create licenses for distributed software using CSD 2.0

Licenses are associated with the software model and must be created if you want to track the license for software deployed by CSD 2.0.

## Before you begin

Role required: sn\_csd.CSD Admin

You can create software licenses in CSD 2.0 for software items deployed from the service catalog by CSD 2.0. CSD 2.0 depends on the allocations available to determine if the license is available for the requested software. If **Allocations Available** is greater than `0`, CSD 2.0 assumes that the license is available for the software.

## Procedure

1.  Navigate to **Client Software Distribution 2.0** &gt; **Software Entitlements**.

2.  Click **New**.

3.  On the form, fill these values.

<table id="table_f41_jqh_fsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name to identify the license record.

</td></tr><tr><td>

Software Model

</td><td>

Software model from the CSD 2.0 table.

</td></tr><tr><td>

Rights

</td><td>

Total number rights.

</td></tr><tr><td>

Allocation Type

</td><td>

Type of license entitlement.**Note:**

-   For Microsoft Endpoint Configuration Manager:
    -   If **Install Collection** specified in **Software Configuration** \(that is linked with catalog item\) is of type **Device**, the license check is performed on software entitlements with **Allocation Type** as **Device**.​
    -   If **Install Collection** specified in **Software Configuration** \(that is linked with catalog item\) is of type **User**, the license check is performed on software entitlements with **Allocation Type** as **User**.
-   For :
    -   If **Group** specified in **Software Configuration** \(that is linked with catalog item\) is of type **Mobile** or **Computer**, the license check is performed on software entitlements with **Allocation Type** as **Device**.
    -   If **Group** specified in **Software Configuration** \(that is linked with catalog item\) is of type **User**, the license check is performed on software entitlements with **Allocation Type** as **User**.


</td></tr></tbody>
</table>4.  Click **Submit**.

    The license is created with the required rights.


**Parent Topic:**[Client Software Distribution 2.0 application](../concept/csd-app-2.md)

