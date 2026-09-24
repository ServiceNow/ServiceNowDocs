---
title: Create an IFL policy for password authentication
description: Create an identifier-first login \(IFL\) policy that routes matching users to password-based authentication \(a username and password managed within the platform\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/create-ifl-policy-password.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [create IFL policy, password authentication, Use Password, Authentication Console]
breadcrumb: [Create an IFL policy, Manage IFL policies, Use the IFL policies, Authentication Console, Authentication, Access Management]
---

# Create an IFL policy for password authentication

Create an identifier-first login \(IFL\) policy that routes matching users to password-based authentication \(a username and password managed within the platform\).

## Before you begin

Role required: `user_authn_admin`

## About this task

A password-based IFL policy routes matching users to log in with a username and password managed within the platform. Use this policy type for users who don't authenticate through single sign-on \(SSO\). For a policy that routes users to an identity provider, see [Create an IFL policy for SSO authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-sso.md).

## Procedure

1.  Navigate to **All** &gt; **Authentication Console**.

2.  In the Authentication Console, open the **Policies** tab and select the option to create a policy.

3.  Under **Policy Details**, enter a **Name** \(required\) and, optionally, a **Description**.

4.  Under **Authentication Method**, select **Use Password**.

    Use Password routes the user to log in with a username and password managed within the platform for basic authentication.

5.  Under **Conditions**, specify the conditions that determine when the policy applies.

    1.  Select a **Field** and an **Operator**, and enter a value.

    2.  To combine conditions, use **or** and **and**, or select **Add condition set** to add another set of conditions.

6.  Under **Policy evaluation**, select **Active** to apply the policy during login, and enter a numeric **Policy order** value.

    Only active policies are evaluated. Policies are evaluated by order value, and lower values are executed first.

7.  Select **Create Policy**.


## Result

The policy appears on the Policies tab. When active, matching users are routed to password-based authentication during the identifier-first login flow.

