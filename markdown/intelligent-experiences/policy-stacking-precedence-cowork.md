---
title: Policy stacking and precedence in ServiceNow Cowork
description: When more than one policy applies to a user, ServiceNow Cowork merges them and resolves conflicts by priority in a fixed order, specificity, and restrictiveness.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/policy-stacking-precedence-cowork.html
release: australia
topic_type: concept
last_updated: "2026-09-29"
reading_time_minutes: 2
keywords: [policy stacking, precedence, priority, restrictiveness, user criteria]
breadcrumb: [Policy management and governance in ServiceNow Cowork, Explore Cowork, ServiceNow Cowork, Enable AI experiences]
---

# Policy stacking and precedence in ServiceNow Cowork

When more than one policy applies to a user, ServiceNow Cowork merges them and resolves conflicts by priority in a fixed order, specificity, and restrictiveness.

More than one policy can apply to the same user, for example the **Default Policy** and a policy for a support team. The **User Criteria** field on each policy record decides which users the policy applies to. The instance merges every policy whose user criteria match the user, then resolves conflicts in the following order:

1.  Priority: Each policy has a priority number, and a lower number means a higher priority. The rule from the policy with the lowest priority number wins. For example, if the Default Policy has priority 999 and a support team policy has priority 100, the support team policy's rules override the Default Policy for users in that team.
2.  Specificity: If two conflicting approval patterns come from policies with the same priority, the pattern that matches more of the command wins. For example, when a user runs git push --force, a pattern for git push --force takes precedence over a pattern for git push.
3.  Restrictiveness: If rules still tie, the more restrictive rule applies, so an ambiguous configuration always resolves toward the safer outcome.

## Restrictiveness by component

|Component|Most restrictive to least restrictive|
|---------|-------------------------------------|
|Tool gate|**Deny**, then **HITL** or **Auto**, then **Allow**|
|Approval pattern|Hard gate, then soft gate|
|File type rule|Deny, then allow write, then allow read|
|Network rule|Not allowlisted, then allowlisted|
|Sandbox filesystem|Deny, then read and write, then read|
|Connector scope|Scope off, then scope on|

## Change default behavior

To change a default, create a policy instead of editing the **Default Policy**:

1.  Create a policy and set its user criteria to the users or groups it applies to.
2.  Set a priority number lower than the policy you want to override. The **Default Policy** has priority 999. New policies have priority 1,000 by default, so change the priority, or the new policy doesn't override the **Default Policy**.
3.  Add only the rules you want to change. Anything you don't add keeps coming from the **Default Policy**.

To undo the change, delete your policy. The previous behavior returns.

This approach has the following advantages:

-   **Intact defaults**

    The **Default Policy** stays unchanged and keeps receiving product updates.

-   **Explainable policy**

    The override and the rule it overrides both exist as records, so you can explain the effective policy.

-   **Reversible changes**

    Reverting means deleting one record.


## Example: Allow a site that the Default Policy blocks

Your developers need Cowork to reach your internal package registry at registry.example.com, which isn't on the Default Policy network allowlist. To allow it, create a policy for the developer group, add a network rule for registry.example.com, and make sure the rule is active. At the next sync, the client receives the Default Policy allowlist and your rule merged together, so the registry is reachable for developers only.

**Parent Topic:**[Policy management and governance in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/policy-management-cowork.md)

