---
title: Edit an IFL policy
description: Modify the conditions, authentication method, or evaluation order of an existing identifier-first login \(IFL\) policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/edit-ifl-policy.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [edit IFL policy, modify authentication policy]
breadcrumb: [Manage IFL policies, Use the IFL policies, Authentication Console, Authentication, Access Management]
---

# Edit an IFL policy

Modify the conditions, authentication method, or evaluation order of an existing identifier-first login \(IFL\) policy.

## Before you begin

Role required: `user_authn_admin`

## Procedure

1.  Navigate to **All** &gt; **Authentication Console**.

2.  Review the list of IFL policies.

    The console lists each policy with its evaluation order and active status. The instance evaluates active policies in order and applies the first policy whose conditions match the user. For more information, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/policy-evaluation-order.md).

3.  Select the policy you want to edit.

4.  Update the policy name, conditions, authentication method, or evaluation order as needed.

5.  Save your changes.


## Result

The updated policy takes effect in subsequent identifier-first login evaluations.

