---
title: Manage a user group segment
description: After creating a user group segment, you can review and edit it before you create cases.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Creating bulk cases, Use HR Case Management, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Manage a user group segment

After creating a user group segment, you can review and edit it before you create cases.

## Before you begin

Role required: sn\_hr\_core.admin

## Procedure

1.  Navigate to **All** &gt; **HR Case Management** &gt; **Bulk Case Requests**.

2.  Select any bulk case request that has a status of **Ready**.

    You can also edit a user group segment immediately after creating one.

3.  Select the user segment group you want to edit found under the **User segment groups** tab.

    The **User segment details** form appears.

4.  Scroll down to the **Selected users** tab.

5.  To remove a user from the user segment group, double-click in the **Status** column for the user you want to remove and change to **Excluded**.

    ![Status related to user in bulk case user segment](../image/bulk-case-user-seg-status.png)

    The meaning for each status:

    -   Included: User matches criteria defined in **User Segments**, create a case for the user.
    -   Excluded: User no longer matches the criteria defined in **User Segments**, do not create a case.
    -   Duplicate: The user has a duplicate record, do not create a case.
    The **Note** column provides information on the status. The definitions are:

    -   No hr\_service.hr\_criteria specified: HR criteria was not used in selecting the user for the user group segment.
    -   User satisfies hr\_service.hr\_criteria: HR criteria was used in selecting the user for the user group segment.
    -   User do not satisfy hr\_service.hr\_criteria: The user did not meet the HR criteria selected and is excluded from the user group segment.
    -   User from user-segment-group&lt;group-label&gt; with sys\_id&lt;unique-id&gt; is included: The user is marked as a duplicate.

        **Note:** The note clears after you change the status of a user.

6.  After changing a user's status, select **Save**.


**Parent Topic:**[Creating bulk cases](../concept/bulk-case.md)

