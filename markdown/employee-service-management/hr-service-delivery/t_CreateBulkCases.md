---
title: Create a bulk case request
description: Use bulk case request to create the same type of HR case, for multiple employees, without having to create the same case multiple times.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Creating bulk cases, HR Case Management, Explore and use HR Case and Knowledge Management, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Create a bulk case request

Use bulk case request to create the same type of HR case, for multiple employees, without having to create the same case multiple times.

## Before you begin

Role required: sn\_hr\_core.admin

**Note:** Previously, the HR case writer \(sn\_hr\_core.case\_writer\) role was required. Because bulk case creation involves a large number of cases, it was decided to change the required role to HR admin \(sn\_hr\_core.admin\).

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Bulk Case Requests**.

2.  Select **New**.

    On the form, fill in the fields.

<table id="simpletable_y2p_442_hpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name that describes the bulk case request.

</td></tr><tr><td>

HR service

</td><td>

The HR service associated with the bulk case request.**Note:** When you create a user segment group, the fields from the HR service you select can appear similar to creating a new HR case. For more information, see [Create a user segment group](bulk-case-segment.md).

</td></tr><tr><td>

Status

</td><td>

The status of the bulk case request.The default is **Draft** and changes to **Ready** after you create and save the **User segment groups** tab.

**Note:** At least one user must be included.

 The status changes to **In progress** after you select the **Create cases** button.

</td></tr><tr><td>

Create parent case

</td><td>

Indicates you want to create a parent case that is associated with the bulk cases. Check the **Create parent case** choice to create a parent case.

</td></tr><tr><td>

Opened by

</td><td>

The name of the user creating the bulk case request.

</td></tr><tr><td>

Selected user count

</td><td>

Shows the number of users selected for the bulk case request. **Note:** This field is empty until you create and save a user group segment.

</td></tr><tr><td>

Requested time

</td><td>

Shows the date and time your bulk case request was submitted to create cases.**Note:** This field is empty until you create a user group segment and select **Create cases**.

</td></tr></tbody>
</table>3.  Select **Save**.

    The **User segment groups** and **Cases created** tabs appear.

4.  Select **New** in the **User segment groups** tab.

    For more information, see [Create a user segment group](bulk-case-segment.md).


**Parent Topic:**[Creating bulk cases](../concept/bulk-case.md)

