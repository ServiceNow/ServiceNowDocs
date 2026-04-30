---
title: Configure Identity Provider attribute for Session Access
description: Use Identity Provider \(IDP\) attribute created from the Security Assertion Markup Language \(SAML\) response and OpenID Connect \(OIDC\) for removing or restricting user session access to the instance.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Tutorial: Use ZTA, Zero Trust Access, Access Management]
---

# Configure Identity Provider attribute for Session Access

Use Identity Provider \(IDP\) attribute created from the Security Assertion Markup Language \(SAML\) response and OpenID Connect \(OIDC\) for removing or restricting user session access to the instance.

## Before you begin

Role required: security\_admin

Enable the **Enable Session Access property**.

**Note:** To use the Session Access role configuration, you must elevate your role to `security_admin`.

Session Access can be controlled by the created policy and selected action when performing the configuration. Some of the scenarios are as follows:

-   If the Policy is true, and the roles action is set to **Remove Roles** along with the IDP attribute input and condition, then the selected roles and its associated child roles are removed for the user when trying to log in to the instance.
-   If the Policy is true, and the roles action is set to **Limit To Roles** along with the IDP attribute input and condition, then only the selected roles and its associated child roles are assigned to the user when trying to log in to the instance.

The following procedure shows steps to configure the IDP attribute from the SAML response a policy input to control session access.

## Procedure

1.  Navigate to **All** &gt; **Session Access** &gt; **Session Access Role Configurations**.

2.  On the Session Access Role Configurations page, select **New**.

3.  For removing any role for the user, on the form, fill the fields:

    -   Name
    -   Description
    -   Policy
    -   Action
    -   Role List
    -   Group List
    1.  Choose **Remove Roles** to remove roles for the user.

        For example: **itil**.

    2.  Choose **itil** role from the Role List.

    3.  Choose the **Policy**.

        To know more on how to create policy using different filter criteria using Adaptive Authentication policy creation, see [Filter criteria](../concept/adaptive-auth-filter-criteria.md).

    4.  Choose Action as Remove Roles.

        If the Policy is true, and the roles action is set to **Remove Roles**, then the selected roles is removed for the user when trying to log in to the instance.

    5.  In the Policy Input, create the Policy Input and Policy Condition.

        For example:

        -   **Policy Input**: Risk score attribute from Okta \(IDP\).
        -   **Policy Conditions**: Risk score from 60 through 80 as a condition.
        ![Identity Attribute Risk Score](../images/idp-attri.png)

        Based on this configuration, when the risk score attribute value from the Okta \(IDP\) beyond 80, the user isn’t authenticated with the roles \(**employee**\) and its child roles that were removed to the instance, the user is only authenticated with other roles assigned. If the risk score is from 60 through 80, the user is authenticated to the instance with all the roles.

        For more information on how to create Post Authentication Context's Policy with Policy inputs and Condition, see [Post-authentication context](../concept/post-auth-context.md).

        **Note:** If the **Enable Session Access** property is inactive, then the configuration for Session Access doesn’t restrict or remove the roles of the user.

    6.  Select **Submit**.


