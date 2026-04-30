---
title: Use Location Filter for Session Access
description: Use the location filter criteria created in Session Access to reduce roles based on the location of the user.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Tutorial: Use Location Filter criteria, Location Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Use Location Filter for Session Access

Use the location filter criteria created in Session Access to reduce roles based on the location of the user.

## Before you begin

Role required: admin

Plugin required: **Zero Trust - Location Based Access** \(`com.snc.zero_trust_location_access`\).

The following procedure describes on how to create a Location Filter with the countries that you want to remove or limit roles to the users based on the location.

## Procedure

1.  Navigate to **All** &gt; **Zero Trust Access** &gt; **Session Access Role Configurations**.

2.  To create a session access role configuration, select **New**.

3.  On the form, fill the fields:

<table id="table_vdl_r1g_twb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the configuration

</td></tr><tr><td>

Description

</td><td>

Short description of the configuration.

</td></tr><tr><td>

Policy

</td><td>

Choose the access policy. Use the look-up icon to view the list of policy.**Note:** You must add the location filter input and conditions by opening the policy record.

</td></tr><tr><td>

Action

</td><td>

**Remove Roles** or **Limit to Roles**.-   **Remove Roles**: When the configured user logged in, the list of roles provided in the Role or Group List are removed for the logged-in session.
-   **Limit To Roles**: When the configured user logged in only the selected roles is provided to the user and all the other roles are removed for the logged-in session.


</td></tr><tr><td>

Role List

</td><td>

Choose the role from the Role List.

</td></tr><tr><td>

Group List

</td><td>

Choose the role from the Group List.

</td></tr></tbody>
</table>4.  Select, **Submit**.

    The login for users based on the configured countries is as follows:

    -   If **Remove Roles**, the users from the configured countries in the location filter will be removed with the roles configured for the session.
    -   If **Limit To Roles**, the users from the configured countries in the location filter has only the roles that are configured for the session.
    To know more about how to remove or limit roles for a session, see [Tutorial: Use Zero Trust Access](use-zero-trust-access.md).


