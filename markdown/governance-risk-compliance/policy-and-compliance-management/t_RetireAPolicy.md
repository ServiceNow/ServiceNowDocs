---
title: Retire a policy
description: Retiring a policy is part of the policy management process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/policy-and-compliance-management/t\_RetireAPolicy.html
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Manage, Classic UI, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Retire a policy

Retiring a policy is part of the policy management process.

## Before you begin

Role required: sn\_compliance\_admin or sn\_compliance\_manager

## About this task

A policy can be retired anytime after being approved and published to the KB. If the policy has reviewers, then one month before the policy retires, it is moved to the Review state. If there are no reviewers for the policy, then it is moved to the Draft state.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policies**.

2.  Open the Policy record.

3.  In the top-right corner, click **Retire**.

    This option is available only for policies in a published state.


## Result

When you retire a policy, the system evaluates each control objective linked to it. If a control objective isn’t linked to another Published policy or to an active citation, the system deactivates it and retires its associated controls. Otherwise, the control objective is left unchanged. Retiring a policy also cancels its policy acknowledgement campaign. For any common control retired as a result, the system deactivates its reliant entity associations.

**Parent Topic:**[Manage control objectives and policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/policy-and-compliance-management/r_PoliciesAndProcedures.md)

