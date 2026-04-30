---
title: History List
description: The history list displays each change as its own row in the change list.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Knowing about History sets, Auditing]
---

# History List

The history list displays each change as its own row in the change list.

![](../image/ViewHistoryList.png "View History List")

Click on a row item to view additional details about the change.

![](../image/ViewListChange.png "View List Change")

## Requirements

To view a history list, the following requirements must be met.

-   **Auditing**

    Auditing for the table must be enabled to view a history list.

-   **ACLs**

    By default, the List history option is only available to users with the admin user role. To enable this option to non-admins, create a custom ACL rule granting read access to the Record History \[sys\_history\_set\] table.

-   **Roles**

    At least one of the roles that the user has must be included in the **glide.history.role** property, which includes the itil role by default.


