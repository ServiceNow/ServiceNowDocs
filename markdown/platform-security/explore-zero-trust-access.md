---
title: Explore Zero Trust Access
description: Zero Trust Access \(ZTA\) is a security model that assumes that no user or device is trusted by default.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Zero Trust Access, Access Management]
---

# Explore Zero Trust Access

Zero Trust Access \(ZTA\) is a security model that assumes that no user or device is trusted by default.

ZTA ensures that all access to applications and data is granted on a least privilege basis, only after the user's identity verification and risk assessment.

## Zero Trust - Policy Based Session Access

ServiceNow Zero Trust - Policy Based Session Access \(Session Access\) enables organizations to dynamically reduce user privilege in a web session based on a variety of factors, including IP address, location, authentication method, user’s role, group, user having MFA and attributes shared by the Identity Provider \(IDP\). This can help protect organizations from unauthorized access and data breaches, even when high-privileged users access applications from untrusted devices or locations.

Zero Trust - Policy Based Session Access

It enables the security admins to reduce or limit user access in a session based on IP address, location, Identity Provider attributes, and user attributes using adaptive authentication policies.

![Zero Trust Access and Adaptive Authentication](../images/session-access-aa.png)

**Note:**

-   Session Access configurations can only be performed with `security_admin` role. You must elevate your role to `security_admin`.
-   Session Access doesn’t support integrations.
-   Session Access has no impact if the reduced or limited role isn’t assigned to a user. In this case, there are no changes to the logged in session. The user continues to access the instance with the assigned privileges.
-   Session Access has no impact while the user is already logged in to the instance and simultaneously the admin configures the policy. The user has to log out from the session for the policy to be effective.
-   Session Access has no impact when the user is in a trusted network and later switches to a VPN \(change in location or network\) within a session.
-   Session Access is enforced at the time of login. Any change in risk parameters during the session won’t result in reduced access. For example, a user switching from the corporate network to an untrusted network after establishing the session won’t result in reduced access unless the user logs out and logs in again.
-   Session Access \(Zero trust access - ZTA\) feature, roles like `snc_internal` and `snc_external` cannot be removed.
-   Session Access \(Zero trust access - ZTA\) feature does not remove a role from the `sys_user_has_role` or the user group membership table. Based on the ZTA policy, it establishes the user session with reduced or limited roles.
-   The scripts running in the system context will not honor the ZTA session roles.

## Use case

Following are some of the use cases of Zero Trust Access:

-   Reduce privileges based on the risk associated with the session. For example, a fulfiller role user logging from outside the trusted network can be configured to have only the requester role for the session.
-   Reduce access based on IDP response for a user session, if the user is using an untrusted device. For more information, see [Configure Identity Provider attribute for Session Access](../task/configure-idp-session-access.md).

This role relegation ensures that the user doesn’t have any other existing privileges in a session. When the user is logging in from a trusted network, all the existing privileges are assigned for a session.

Multiple IP conditions and multiple role or group assignments can be defined as part of the policy.

## Zero Trust Access - Mobile

You can use the Zero Trust Access - Session Access policy within the Adaptive Authentication policy to reduce the roles or privileges of the particular session in mobile.

Zero Trust Access - Session Access mobile can be enabled by enabling the **glide.authenticate.session\_access.mobile.enabled** from the system properties table.

To use Zero Trust Access - Session Access mobile with the IDP attributes you can configure the **glide.authenticate.session\_access.mobile.refresh\_token\_interval** field. This enables the administrators to effectively control the session access based on refresh token.

For more information, see Configure Zero Trust Access for mobile.

