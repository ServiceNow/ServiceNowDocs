---
title: Copy user or device allocations
description: Copy user or device allocations from one entitlement to the other.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Copy user or device allocations

Copy user or device allocations from one entitlement to the other.

## Before you begin

Copy allocations from a source entitlement to a target entitlement to renew expired entitlements or add a new maintenance. Additionally you can also copy allocations while creating entitlements that require the same allocations as in another entitlement.

The entitlement from which you want to copy the allocations is referred to as the source entitlement. The entitlement to which you want to copy the allocations is referred to as the target entitlement.

User allocations can be copied to only entitlements that support user allocations. Similarly, device allocations can be copied to entitlements that support device allocations. For details on license metrics, see [Software license metrics](../concept/c_SAMLicenseMetrics.md).

If the selected user or device is already allocated in the target entitlement, the quantity of that allocation is incremented.

Prior to copying allocations, ensure that the following prerequisites are met:

-   The target entitlement has enough allocations available. The **Copy allocations** button only appears when the allocations available on the entitlement is greater than zero. An error occurs if the number of allocations being copied exceeds the number of available allocations in the target entitlement
-   The target entitlement is in **Build**, **In use**, or **On order** state.
-   The target entitlement has enough available rights.

Role required: sam\_admin or sam\_user.

## Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations** &gt; **Software entitlements**.

2.  Open the target entitlement in which you want to copy the user or device allocations.

3.  Select the appropriate allocations related list \(User Allocations or Device Allocations\).

4.  Select **Copy allocations**.

    The details of the target entitlement such as allocations available, license type, active rights appear at the top of the page.

5.  Select the entitlement from which you want to copy the allocations from in the **Source entitlement** list.

    All the details of the source entitlement such as license metric, metric group appear on the Details page.

6.  Select the Source allocations related list and select the allocations.

7.  Select **Submit**.

    If the copy allocation process is successful, then **Submit** gets disabled. A message informs you that the copy of allocations is being processed. You can check the status by clicking the link in the message.

    The link takes you to the Software Asset Job Results \[samp\_job\_log\] table. Use the Name column to search for the job log record, titled **Copy Allocations to &lt; &gt;**, where the angle brackets refer to the display name of the target entitlement.


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

**Related topics**  


[Create device allocation](create-device-allocation.md)

