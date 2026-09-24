---
title: Activate or deactivate an IFL policy
description: Control whether an identifier-first login \(IFL\) policy is included in policy evaluation by activating or deactivating it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/activate-deactivate-ifl-policy.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [activate IFL policy, deactivate IFL policy]
breadcrumb: [Manage IFL policies, Use the IFL policies, Authentication Console, Authentication, Access Management]
---

# Activate or deactivate an IFL policy

Control whether an identifier-first login \(IFL\) policy is included in policy evaluation by activating or deactivating it.

## Before you begin

Role required: `user_authn_admin`

## About this task

Only active policies are evaluated during the identifier-first login flow. Deactivate a policy to remove it from evaluation without deleting it.

## Procedure

1.  Navigate to **All** &gt; **Authentication Console**.

2.  Review the list of IFL policies.

    The console lists each policy with its evaluation order and active status. The instance evaluates active policies in order and applies the first policy whose conditions match the user. For more information, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/policy-evaluation-order.md).

3.  Select the policy you want to activate or deactivate.

4.  Do one of the following:

    -   To include the policy in evaluation, set it to active.
    -   To remove the policy from evaluation, set it to inactive.
5.  Save your changes.


## Result

An active policy is included in policy evaluation. An inactive policy is retained but excluded from evaluation.

