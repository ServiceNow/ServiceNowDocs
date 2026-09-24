---
title: Activate the policy-based login experience
description: Activate the policy-based login experience so that you can create and manage the identifier-first login \(IFL\) policies that drive the next-generation login experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/activate-authentication-console.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [activate authentication console, Policy-Based Login Experience console, activate console, next-generation login experience]
breadcrumb: [Authentication Console, Authentication, Access Management]
---

# Activate the policy-based login experience

Activate the policy-based login experience so that you can create and manage the identifier-first login \(IFL\) policies that drive the next-generation login experience.

## Before you begin

Role required: `user_authn_admin`

## About this task

You can activate the policy-based login experience it by enabling the `glide.authenticate.policy_based_login_experience.enabled` system property. After the property is active, you use create and manage IFL policies in the Authentication Console. For an overview of the console, see [Authentication Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/authentication-console.md).

## Procedure

1.  In the navigation filter, enter `sys_properties.list` and open the system properties list.

2.  Open the `glide.authenticate.policy_based_login_experience.enabled` property.

3.  Set the **Value** to `true`.

4.  Select **Update**.

5.  Open the Authentication Console and select the **Settings** tab.

6.  Turn on **Enable policy-based login**.

    This setting determines the first authentication factor during user login.

7.  Create at least one active IFL policy.

    See [Create an IFL policy for password authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-password.md) or [Create an IFL policy for SSO authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-sso.md).


## Result

The policy-based login experience is active. You can now create the IFL policies that route users during the identifier-first login flow.

## What to do next

-   Create your first policy. See Create an IFL policy.
-   Manage existing policies. See Manage IFL policies.

**Note:** The next-generation login experience takes effect only when this property is enabled and at least one active IFL policy exists. Enabling the property alone does not change the login flow.

