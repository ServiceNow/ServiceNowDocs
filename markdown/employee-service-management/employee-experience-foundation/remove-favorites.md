---
title: Remove favorites
description: Enable the RCAs to manage the favorites options from the Employee Center.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Cross-channel favorites, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Remove favorites

Enable the RCAs to manage the favorites options from the Employee Center.

## Before you begin

Set the Application Restricted Caller Access on the **Table: Portal Favorite**.

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **Favorite**.

2.  On the sp\_favorite, go to the **Application Access** tab.

3.  Ensure you select all the following options with the **All application scopes**.

    -   Can read
    -   Can create
    -   Can update
    -   Can delete

        **Note:** When you do not select the Delete operation with **sp\_favorite**, you are unable to remove the favorite from your favorites. The following message appears.

        ```
        Delete operation against 'sp_favorite' from scope 'sn_ex_sp' has been refused due to the table's cross-scope access policy
        Unable to remove this item from your favorites.
        ```


## Result

The **Favorite** functionality is enabled and you can perform the specified CRUD operations.

