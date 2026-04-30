---
title: Activate Session Validation Context
description: Use Session Validation Context to restrict access to ServiceNow when hijackers copy a user's session cookies from one device to another to impersonate the session or restricts the user's session access if they’re using an insecure network.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Session validation context, Authentication policy contexts, Adaptive authentication, Authentication, Access Management]
---

# Activate Session Validation Context

Use Session Validation Context to restrict access to ServiceNow® when hijackers copy a user's session cookies from one device to another to impersonate the session or restricts the user's session access if they’re using an insecure network.

## Before you begin

Role required: admin

To use the session validation, you must perform the following steps:

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **All Policies**.

2.  Select the **Session Validation Policy** in the Policies \(`sys_authentication_policy_list.do`\) page.

3.  Specify the **Policy Inputs** and **Policy Conditions**.

4.  Set the conditions to **true** or **false** for the filters that you’ve added.

5.  Select the **Active** check box to activate the policy after you set up the Session Validation Policy is set up with policy inputs and conditions.

6.  Select a **Force AuthnRequest** check box for the default identity provider in the sso\_properties table if the instance has SSO configured.

7.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Authentication Policies** &gt; **Properties**.

8.  Set the system property `session.validation.enabled` to **Yes**.

    ![Session Validation](../images/session-context.png)


## Result

The Session Validation feature is activated. You can configure the policy inputs and conditions for the policy to use the feature. To learn more, see [Tutorial: Configuring session validation](use-ip-session-context.md).

