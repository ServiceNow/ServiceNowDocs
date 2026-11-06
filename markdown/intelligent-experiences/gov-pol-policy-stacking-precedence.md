---
title: Policy stacking and precedence in ServiceNow Arc
description: When more than one policy applies to a user, Arc merges them into one effective policy and resolves any conflicts by priority, specificity, and restrictiveness.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-policy-stacking-precedence.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 3
keywords: [policy stacking, precedence, priority, restrictiveness, user criteria, arc policies]
breadcrumb: [Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Policy stacking and precedence in ServiceNow Arc

When more than one policy applies to a user, Arc merges them into one effective policy and resolves any conflicts by priority, specificity, and restrictiveness.

## How policies merge

More than one active policy can apply to the same user, for example the default Arc policy and a policy for a support team. Each policy's user criteria decide which users it applies to. Arc merges every policy whose user criteria match the user into one effective policy, and the user's Arc application receives that policy at its next sync.

Rules from different policies add up. For example, a network rule in your policy that allows a new host joins the default allowlist instead of replacing it. Two rules conflict only when they govern the same thing, such as two tool gates for the same tool or two file type rules for the same extension.

## How conflicts are resolved

When two rules conflict, how Arc picks the winner depends on the rule type.

-   **Tool gates, sandbox rules, and capability overrides**

    The rule from the policy with the lowest priority number wins. The default Arc policy has priority 999, and new policies start at 100, so a new policy overrides the default policy unless you set its number above 999. If two capability overrides come from policies with the same priority, the more restrictive value applies.

-   **Approval patterns**

    Patterns from every policy that applies to the user are compared together. The pattern that matches more of the command wins first, whatever policy it comes from. For example, when a user runs `git push --force`, a pattern for `git push --force` takes precedence over a pattern for `git push`. Among patterns that match equally well, the pattern's own priority decides, then the policy's priority, then the more restrictive gate.

-   **File type rules**

    When rules from different policies cover the same extension, the rule from the policy with the lowest priority number wins.


## Restrictiveness by rule type

|Rule type|Most restrictive to least restrictive|
|---------|-------------------------------------|
|Tool gate|Block, then require approval or auto approval, then allow|
|Approval pattern|Hard gate, then soft gate, then allow carve-out|
|File type rule|Deny all access, then allow read and write, then allow read only|
|Network rule|Not on the allowlist, then on the allowlist|
|Sandbox filesystem rule|Deny, then read and write, then read only|
|Connector scope|Scope off, then scope on|

## Changing default behavior

To change how Arc behaves by default, create a policy that layers over the default Arc policy instead of changing the default itself. Layering has the following advantages:

-   **Intact defaults**

    The default Arc policy stays unchanged and keeps receiving product updates.

-   **Explainable policy**

    The override and the rule it overrides both exist as records, so you can explain the effective policy.

-   **Reversible changes**

    To undo the change, deactivate or delete your policy, and the previous behavior returns.


To layer a policy over the default:

1.  Create a policy and set its user criteria to the users or groups it applies to.
2.  Keep its priority number below 999. New policies start at 100, so the default value works unless you're layering over another policy of your own.
3.  Add only the rules you want to change. Anything you don't add keeps coming from the default Arc policy.

For the steps, see [Create an Arc policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-create-arc-policy.md).

## Example: Allow a site that the default Arc policy blocks

Your developers need Arc to reach your internal package registry at registry.example.com, which isn't on the default allowlist. To allow it, create a policy for the developer group and add an active network rule that allows registry.example.com. At the next sync, the developers' Arc application receives the default allowlist and your rule merged together, so the registry is reachable for developers only.

