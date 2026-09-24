---
title: Create an IFL policy for SSO authentication
description: Create an identifier-first login \(IFL\) policy that routes matching users to a single sign-on \(SSO\) identity provider.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/create-ifl-policy-sso.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [create IFL policy, SSO login, identity provider, Multi-Provider SSO, Authentication Console]
breadcrumb: [Create an IFL policy, Manage IFL policies, Use the IFL policies, Authentication Console, Authentication, Access Management]
---

# Create an IFL policy for SSO authentication

Create an identifier-first login \(IFL\) policy that routes matching users to a single sign-on \(SSO\) identity provider.

## Before you begin

Role required: `user_authn_admin`

The SSO login authentication method is available only when the Multi-Provider SSO plugin is installed and at least one identity provider is configured. Until then, the SSO login option is unavailable and you can select only Use Password. To route users to password authentication instead, see [Create an IFL policy for password authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-password.md).

## About this task

An SSO-based IFL policy routes matching users to an organization identity provider, so they log in using their existing SSO credentials.

## Procedure

1.  Navigate to **All** &gt; **Authentication Console**.

2.  In the Authentication Console, open the **Policies** tab and select the option to create a policy.

3.  Under **Policy Details**, enter a **Name** \(required\) and, optionally, a **Description**.

4.  Under **Authentication Method**, select **SSO login**.

5.  In **Select an Identity Provider**, choose the identity provider to route matching users to.

6.  Under **Conditions**, specify the conditions that determine when the policy applies.

    1.  Select a **Field** and an **Operator**, and enter a value.

    2.  To combine conditions, use **or** and **and**, or select **Add condition set** to add another set of conditions.

7.  Under **Policy evaluation**, select **Active** to apply the policy during login, and enter a numeric **Policy order** value.

    Only active policies are evaluated. Policies are evaluated by order value, and lower values are executed first.

8.  Select **Create Policy**.


## Result

The policy appears on the Policies tab. When active, matching users are routed to the selected identity provider during the identifier-first login flow.

