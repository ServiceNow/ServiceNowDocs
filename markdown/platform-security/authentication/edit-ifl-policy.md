---
title: Edit an identifier-first login policy
description: Modify the conditions, authentication method, or evaluation order of an existing identifier-first login policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/authentication/edit-ifl-policy.html
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
keywords: [edit IFL policy, modify authentication policy]
breadcrumb: [Manage IFL policies, Use the IFL policies, Authentication Console, Authentication, Access Management]
---

# Edit an identifier-first login policy

Modify the conditions, authentication method, or evaluation order of an existing identifier-first login policy.

## Before you begin

Role required: `user_authn_admin`

## Procedure

1.  Navigate to **All** &gt; **Authentication Console**.

2.  Review the list of identifier-first login policies.

    The console lists each policy with its evaluation order and active status. The instance evaluates active policies in order and applies the first policy whose conditions match the user. For more information, see [Policy evaluation order](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/authentication/policy-evaluation-order.md).

3.  Select the policy you want to edit.

4.  Update the policy name, conditions, authentication method, or evaluation order as needed.

5.  Save your changes.


## Result

The updated policy takes effect in subsequent identifier-first login evaluations.

