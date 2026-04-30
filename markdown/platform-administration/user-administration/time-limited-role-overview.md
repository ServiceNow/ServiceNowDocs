---
title: Time-limited role
description: Time-limited roles give users the defined role during the defined time period.
locale: en-US
release: zurich
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-02-26"
reading_time_minutes: 1
breadcrumb: [Managing roles, User admin, Configure core features, Administer]
---

# Time-limited role

Time-limited roles give users the defined role during the defined time period.

Assigning the time-limited roles ensures users have elevated access only when needed, without requiring manual revocation. When you assign a time-limited role to a user, you specify a start and end date. The system automatically activates the role at the start date and removes it when the end date passes, eliminating the need for manual access cleanup.

## Supported roles and limits

Time-limited roles enhance security by automatically reducing privileges when no longer needed, support compliance through time-bound access policies, and improve efficiency by eliminating manual tracking and revocation. The following table provides information about the available time-limited roles and limits:

<table id="table_db5_z3t_k3c"><thead><tr><th>

Supported Roles

</th><th>

Assignment Rules

</th></tr></thead><tbody><tr><td>

-   `admin`
-   `snc_read_only`
-   `impersonator`
-   `snc_required_script_writer_permission`

</td><td>

-   Maximum of four concurrent time-limited roles per user can be assigned
-   Time-limited role can be maximum of 5 days per user.
-   Time-limited assignments can handle more than one role assignment to a user, even if the total duration across assignments is less than five days.

</td></tr></tbody>
</table>-   **[Grant a time-limited user role](time-limited-roles.md#)**  
Learn how to assign a role to a user temporarily. Use this feature if you have a user who needs to perform a one-time action that is normally outside their roles.

**Parent Topic:**[Managing roles](ua-creating-roles.md)

