---
title: Create an identifier-first login policy
description: Create an identifier-first login policy to route users to an authentication method based on conditions such as IP address, role, or group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/create-ifl-policy.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
keywords: [create IFL policy, new authentication policy]
breadcrumb: [Manage IFL policies, Use the IFL policies, Authentication Console, Authentication, Access Management]
---

# Create an identifier-first login policy

Create an identifier-first login policy to route users to an authentication method based on conditions such as IP address, role, or group.

## Before you begin

Role required: `user_authn_admin`

## About this task

Create an identifier-first login policy to define which authentication method applies to a set of users. The instance evaluates active policies in order and applies the first matching policy.

## Procedure

1.  Navigate to **All** &gt; **Authentication Console**.

2.  In the Authentication Console, open the **Policies** tab and select the option to create a policy.

3.  Under **Policy Details**, enter a **Name** \(required\) and, optionally, a **Description**.

4.  Under **Authentication Method**, select **SSO login** or **Use Password**.

    For SSO login, see [Create an identifier-first login policy for SSO authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/create-ifl-policy-sso.md). For Use Password, see [Create an identifier-first login policy for password authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/create-ifl-policy-password.md).

5.  Under **Conditions**, define the conditions that determine when the policy applies, using attributes such as IP address, role, or group.

    When a policy has multiple conditions, all conditions must be met for the policy to match.

6.  Under **Policy evaluation**, select **Active** to apply the policy during login, and enter a numeric **Policy order** value.

    To learn more, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/policy-evaluation-order.md).

7.  Select **Create Policy**.


## Result

The policy appears in the console and, when active, is included in policy evaluation during the identifier-first login flow.

