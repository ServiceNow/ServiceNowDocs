---
title: Delete an IFL policy
description: Permanently remove an identifier-first login \(IFL\) policy from the Policy-Based Login Experience console.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/delete-ifl-policy.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [delete IFL policy, remove authentication policy]
breadcrumb: [Manage IFL policies, Use the IFL policies, Authentication Console, Authentication, Access Management]
---

# Delete an IFL policy

Permanently remove an identifier-first login \(IFL\) policy from the Policy-Based Login Experience console.

## Before you begin

Role required: `user_authn_admin`

## About this task

Deleting a policy permanently removes it. If you want to keep the policy but exclude it from evaluation, deactivate it instead. See [Activate or deactivate an IFL policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/activate-deactivate-ifl-policy.md).

## Procedure

1.  Navigate to **All** &gt; **Authentication Console**.

2.  Review the list of IFL policies.

    The console lists each policy with its evaluation order and active status. The instance evaluates active policies in order and applies the first policy whose conditions match the user. For more information, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/policy-evaluation-order.md).

3.  Select the policy you want to delete.

4.  Select **Delete**.

5.  Confirm the deletion.


## Result

The policy is removed and is no longer evaluated during the identifier-first login flow.

