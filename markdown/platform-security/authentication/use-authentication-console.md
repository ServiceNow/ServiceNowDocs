---
title: Use the IFL policies
description: Use the identifier-first login \(IFL\) policies to view, build, order, and maintain authentication mechanism that route users during the next-generation login experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/use-authentication-console.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [use authentication console, Policy-Based Login Experience console, manage IFL policies, policy order, next-generation login experience]
breadcrumb: [Authentication Console, Authentication, Access Management]
---

# Use the IFL policies

Use the identifier-first login \(IFL\) policies to view, build, order, and maintain authentication mechanism that route users during the next-generation login experience.

## Before you begin

Role required: `user_authn_admin`

The policy-based login experience must be active. To learn more, [Activate the policy-based login experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/activate-authentication-console.md).

## About this task

The policy-based login experience is a no-code interface for managing the next-generation login experience. From the console, you can view your existing IFL policies, see their evaluation order and status, and perform all policy management actions. For an overview of the console, see [Authentication Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/authentication-console.md).

## Procedure

1.  Navigate to **All** &gt; **Authentication Console**.

2.  Review the list of IFL policies.

    The console lists each policy with its evaluation order and active status. The instance evaluates active policies in order and applies the first policy whose conditions match the user. For more information, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/policy-evaluation-order.md).

3.  From the console, perform the policy management action you need:

    -   To add a policy, create one. See [Create an IFL policy for password authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-password.md) or [Create an IFL policy for SSO authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-sso.md).
    -   To change a policy's conditions, authentication method, or order, edit it. See [Edit an IFL policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/edit-ifl-policy.md).
    -   To include a policy in evaluation or remove it from evaluation without deleting it, activate or deactivate it. See [Activate or deactivate an IFL policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/activate-deactivate-ifl-policy.md).
    -   To permanently remove a policy, delete it. See [Delete an IFL policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/delete-ifl-policy.md).

## Result

Your policy changes apply to subsequent identifier-first login evaluations. Active policies are evaluated in order; if no policy matches, the instance uses the default routing.

## What to do next

For field descriptions used when building a policy, see IFL policy field reference.

