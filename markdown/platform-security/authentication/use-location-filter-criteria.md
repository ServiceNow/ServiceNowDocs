---
title: Tutorial: Use Location Filter criteria
description: Describes steps to use location filter criteria in the authentication policy and restrict access to the users based on the location.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Location Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Tutorial: Use Location Filter criteria

Describes steps to use location filter criteria in the authentication policy and restrict access to the users based on the location.

## Before you begin

Role required: admin

Plugin required: **Zero Trust - Location Based Access** \(`com.snc.zero_trust_location_access`\).

Property: Enable the Adaptive authentication property.

**Note:** Administrators can only create the policy based on location filters if the location is available for the current user session.

The following procedure describes how to create and use the location filter criteria in an authentication policy.

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Filter Criteria** &gt; **Location Filter**.

2.  Select **New**.

3.  On the form, fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the criteria.|
    |Description|Short description of the criteria.|
    |Application|Scope of the application.|

4.  In the **Locations** sections, under the Locations for criteria tab, double-click to **Insert a new row**.

5.  Specify the locations.

    For example, use some of the APAC regions to control the logins of the users coming from APAC.

    ![Filter Criteria](../images/apac-filter-criteria.png)

    Based on the criteria set in the example, you can control logins from `Indonesia`, `China`, and `Malaysia` for your instance.

6.  Select **Submit**.

7.  Use the filter criteria created in any of the authentication context \(Pre, Post, MFA\) and Session Access.

    To know more about the configuration based on authentication context and session access, see:

    -   [Location Filter in Pre Authentication Context](use-lf-pre-auth.md)
    -   [Location Filter in Post Authentication Context](use-lf-post-auth.md)
    -   [Location Filter in MFA Context](use-lf-in-mfa.md)
    -   [Location Filter for Session Access](lf-for-session-access.md)
    You can use the Property ID - Error message to be displayed to the user when login fails due to authentication policy failure \(`glide.auth.policy.ui.error.message`\) to customize the error message.


