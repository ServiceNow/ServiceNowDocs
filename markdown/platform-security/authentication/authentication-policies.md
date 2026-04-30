---
title: Authentication policies
description: Authentication policies evaluate authentication requests based on the specified policy conditions and either allow or deny access depending on the output of policy conditions evaluation. For example, access is allowed only if all the policy conditions specified in Allow Access Policy evaluate to true.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Adaptive authentication, Authentication, Access Management]
---

# Authentication policies

Authentication policies evaluate authentication requests based on the specified policy conditions and either allow or deny access depending on the output of policy conditions evaluation. For example, access is allowed only if all the policy conditions specified in **Allow Access Policy** evaluate to true.

Use the built-in authentication policies or create an authentication policy according to your security requirements. You can find the policies on your instance by navigating to **Adaptive Authentication** &gt; **Authentication Policies** &gt; **All Policies**.

**Note:** At any point of time, either Allow Access Policy or Deny Access Policy can be executed but not both.

|Policy|Description|
|------|-----------|
|Allow access policy|Denies all the authentication requests by default. Allows only the authentication requests that match the specified policy conditions.|
|Allow access pre-auth policy|Allow access pre-auth policy.|
|Allow non local login users|Choose this policy to allow non-local login users. Used in the context of SSO recovery flows.|
|Deny access policy|Allows the authentication requests by default. Denies only the authentication requests that match the specified policy conditions.|
|Global blocking policy|Denies the access requests of users and APIs before authentication. This policy can be used as an alternative to the [IP Address Access Control](../../../administer/login/task/t_AccessControl.md).|
|Session Validation Policy|The authentication policy evaluates Filter Criteria \(For example, IP address\) to determine whether a session should remain active for incoming requests. You must set the filter criteria on this policy.|
|Local login deny policy|Choose this policy to block all local logins. Used in the context of SSO recovery flows.|
|Step-down MFA policy|Choose **Step-Down MFA Policy** as the default policy in situations where users do not require MFA authentication. When the policy conditions defined in the Step-Up MFA Policy evaluate to true, users are not required to login using MFA.|
|Step-up MFA policy|Choose **Step-Up MFA Policy** as the default policy to require MFA authentication when the policy conditions defined in the Step-Up MFA Policy evaluate to true.|

