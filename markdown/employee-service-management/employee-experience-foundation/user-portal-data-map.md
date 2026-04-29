---
title: User portal data map
description: User Portal Data Map table table is accessible only to the maint user and is auto-deleted in 30 days with an auto-flush job.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Mega menu async load system properties, Mega menu configuration, Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# User portal data map

**User Portal Data Map table** table is accessible only to the maint user and is auto-deleted in 30 days with an auto-flush job.

## Before you begin

Role required: admin or maint user.

## About this task

**User Portal Data Map table** stores the session data when the user logs in. When you mark

-   **sn\_ex\_sp.megamenu \_async\_load**=true and **sn\_ex\_sp.megamenu\_async\_load\_skeleton\_view**=true, the user portal data map \(sn\_ex\_sp\_user\_portal\_data\_map\) fetches, stores, refreshes, and displays the latest mega menu session data without page refresh. Skeleton loaders appear, a job fetching the latest data runs in the background, then this data is displayed for subsequent sessions until the data is fetched afresh.
-   **sn\_ex\_sp.megamenu \_async\_load**=true and **sn\_ex\_sp.megamenu\_async\_load\_skeleton\_view**=false, the user portal data map \(sn\_ex\_sp\_user\_portal\_data\_map\) saves the megamenu session data from the most recent session. Table data updates with each login. This data appears for subsequent sessions without skeleton loaders.

    **Note:** Ensure you re-login for the changes to display.


## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables** &gt; **User Portal Data Map**.

2.  On the sn\_ex\_sp\_user\_portal\_data\_map, go to the **Application Access** tab.

3.  See the following options with the **All application scopes**.

    -   Can read
    -   Can create
    -   Can update
    Do not select **Can delete**

    **Note:** Data in the **User Portal Data Map table** table is accessible only to the maint user and is auto-deleted in 30 days with an auto-flush job.


## What to do next

In the navigation filter, enter `sn_ex_sp_user_portal_data_map.list` to see the data.

![Illustrative image for the user portal data map session data](../images/mm-user-portal-data-map.png "User portal data map session data")

**Related topics**  


[Configure Mega menu async load system properties](config-mega-menu-async-load.md)

