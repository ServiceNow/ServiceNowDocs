---
title: Test a ServiceNow Cowork policy change
description: Verify that a policy change works as intended before you apply it to all users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/test-cowork-policy-change.html
release: zurich
topic_type: task
last_updated: "2026-09-29"
reading_time_minutes: 1
keywords: [test policy, policy sync]
breadcrumb: [Reference, ServiceNow Cowork, Enable AI experiences]
---

# Test a ServiceNow Cowork policy change

Verify that a policy change works as intended before you apply it to all users.

## Before you begin

Create the policy with user criteria that cover only a test user.

Role required: sn\_app\_cowork.admin

## About this task

The instance merges policies and sends only the result, so a mistake in a broadly scoped policy affects every user it covers at their next sync. Test with a scoped policy first.

## Procedure

1.  Save the policy on the instance.

2.  Sync the policy to the client.

    Wait for the change to arrive, which happens in near real time, or ask Cowork application on the client to restart the sandbox.

3.  On the client, confirm the last policy sync time in **Settings** &gt; **Agent Sandbox**.

4.  Run the action you intended to control, and confirm that the policy handles it as expected.

5.  Run an action that the change shouldn't affect, and confirm that it still works.

    Testing both confirms that the rule is doing what you intend, not blocking actions for an unrelated reason.

6.  Update the policy's user criteria to cover the users or groups it's meant for.


## Result

The policy change applies to its intended users at their next sync.

**Parent Topic:**[ServiceNow Cowork reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-reference.md)

