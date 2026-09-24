---
title: Create an IFL policy
description: Create an identifier-first login \(IFL\) policy to route users to an authentication method based on conditions such as role, group, or department.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/create-ifl-policy.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [create IFL policy, new authentication policy]
breadcrumb: [Manage IFL policies, Use the IFL policies, Authentication Console, Authentication, Access Management]
---

# Create an IFL policy

Create an identifier-first login \(IFL\) policy to route users to an authentication method based on conditions such as role, group, or department.

## Before you begin

Role required: `user_authn_admin`

## About this task

Create an IFL policy to define which authentication method applies to a set of users. The instance evaluates active policies in order and applies the first matching policy.

## Procedure

1.  Navigate to **All** &gt; **Authentication Console**.

2.  Select **New**.

3.  Enter a name for the policy.

4.  Define the conditions that determine when the policy applies, using attributes such as IP address, role, or group.

    When a policy has multiple conditions, all conditions must be met for the policy to match.

5.  Select the authentication method to apply when the policy matches, such as an [SSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-sso.md) or [Password](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/create-ifl-policy-password.md).

6.  Set the evaluation order for the policy.

    To learn more, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/policy-evaluation-order.md).

7.  Activate the policy, and then save your changes.


## Result

The policy appears in the console and, when active, is included in policy evaluation during the identifier-first login flow.

