---
title: Activate the policy-based login experience
description: Activate the policy-based login experience so that you can create and manage the identifier-first login policies that drive the policy-based login experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/activate-authentication-console.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [activate authentication console, Policy-Based Login Experience console, activate console, next-generation login experience]
breadcrumb: [Authentication Console, Authentication, Access Management]
---

# Activate the policy-based login experience

Activate the policy-based login experience so that you can create and manage the identifier-first login policies that drive the policy-based login experience.

## Before you begin

Role required: `user_authn_admin`

## About this task

You can activate the policy-based login experience by enabling the `glide.authenticate.policy_based_login_experience.enabled` system property and turning on **Enable policy-based login** in the Authentication Console. After the experience is active, you can create and manage identifier-first login policies in the Authentication Console. For an overview of the console, see [Authentication Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/authentication-console.md).

## Procedure

1.  In the navigation filter, enter `sys_properties.list` and open the system properties list.

2.  Open the `glide.authenticate.policy_based_login_experience.enabled` property.

3.  Set the **Value** to `true`.

4.  Select **Update**.

5.  Open the Authentication Console and select the **Settings** tab.

6.  Turn on **Enable policy-based login**.

    This setting determines the first authentication factor during user login.

7.  Create at least one active identifier-first login policy.

    See [Create an identifier-first login policy for password authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/create-ifl-policy-password.md) or [Create an identifier-first login policy for SSO authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/create-ifl-policy-sso.md).


## Result

The policy-based login experience is active. You can now create the identifier-first login policies that route users during the identifier-first login flow.

## What to do next

-   Create your first policy. See [Create an identifier-first login policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/create-ifl-policy.md).
-   Manage existing policies. See [Manage identifier-first login policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/manage-ifl-policies.md).

**Note:** The policy-based login experience takes effect only when the property is enabled, Enable policy-based login is turned on, and at least one active identifier-first login policy exists. Enabling the property alone doesn't change the login flow.

