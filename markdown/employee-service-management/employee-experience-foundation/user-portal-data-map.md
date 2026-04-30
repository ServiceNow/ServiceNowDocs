---
title: User portal data map
description: Stores the stale data for the first session when the user logs in. The data is displayed until new data is fetched and updated in the UI.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Mega menu async load system properties, Mega menu configuration, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# User portal data map

Stores the stale data for the first session when the user logs in. The data is displayed until new data is fetched and updated in the UI.

## Before you begin

Role required: admin or maint user.

## About this task

When you mark

-   **sn\_ex\_sp.megamenu \_async\_load**=true and **sn\_ex\_sp.megamenu\_async\_load\_skeleton\_view**=true, the user portal data map \(sn\_ex\_sp\_user\_portal\_data\_map\) fetches, stores, refreshes, and displays the latest mega menu session data without page refresh. Skeleton loaders appear, a job fetching the latest data runs in the background, then this data is displayed for subsequent sessions until the data is fetched afresh.
-   **sn\_ex\_sp.megamenu \_async\_load**=true and **sn\_ex\_sp.megamenu\_async\_load\_skeleton\_view**=false, the user portal data map \(sn\_ex\_sp\_user\_portal\_data\_map\) stores the mega menu session data for the first session. This data appears for subsequent sessions without skeleton loaders.

    **Note:** Ensure you re-login for the changes to display.


Data in this table is accessible only to the maint user and is auto-deleted in 30 days with an auto-flush job.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **User Portal Data Map**.

2.  On the sn\_ex\_sp\_user\_portal\_data\_map, go to the **Application Access** tab.

3.  Ensure you select all the following options with the **All application scopes**.

    -   Can read
    -   Can create
    -   Can update
    Do not select **Can delete**

    **Note:** When you do not select the Delete operation, you can't delete it.


## What to do next

In the navigation filter, enter `sn_ex_sp_user_portal_data_map.list` to see the data.

![image.mm-user-portal-data-map]

**Related topics**  


[Configure Mega menu async load system properties](config-mega-menu-async-load.md)

