---
title: Remove a rule from an Arc policy
description: Stop applying a rule to the users an ServiceNow Arc policy covers by removing it from that policy, while other policies that use the rule keep it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-remove-arc-policy-rule.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, remove arc policy rule, delete rule, unlink rule, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Remove a rule from an Arc policy

Stop applying a rule to the users an ServiceNow Arc policy covers by removing it from that policy, while other policies that use the rule keep it.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

Removing a rule only unlinks it from this policy. The rule record stays, and other policies that link it aren't affected. A capability override is the exception, because it belongs to one policy, so removing it deletes it permanently.

After you remove a rule, the users this policy covers get that behavior from their other policies, such as the default Arc policy. You can't remove rules from the default policy.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy that contains the rule.

3.  Select the tab for the type of rule.

    To reach **Sandbox rules**, **Connector scopes**, or **Capability overrides**, select **More** first.

4.  Select the rule that you want to remove.

5.  Select **Delete**.

6.  In the **Remove this rule from the policy?** dialog box, select **Remove**.


## Result

The rule no longer appears on the policy's tab. The change reaches the users the policy covers at their next policy sync.

