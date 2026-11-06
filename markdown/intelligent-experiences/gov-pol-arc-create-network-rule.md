---
title: Create a network rule for an Arc policy
description: Open a destination that ServiceNow Arc needs to reach, or block one it shouldn't, by adding a network rule for the users a policy covers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-arc-create-network-rule.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, network rule, network allowlist, audit enforcement, sandbox network, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create a network rule for an Arc policy

Open a destination that ServiceNow Arc needs to reach, or block one it shouldn't, by adding a network rule for the users a policy covers.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

The agent's sandbox can reach only the hosts and ports on its network allowlist. The default Arc policy includes a list of trusted domains, and your policy's rules are merged with that list for the users the policy covers.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy you want to update.

3.  Select the **Network rules** tab.

4.  Select **Create network rules**.

    If the policy already has network rules, select **+ Add rule** instead.

5.  On the form, fill in the fields.

<table id="table_network_rule_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Rule Name**

</td><td>

Name that describes what the rule does, for example, Allow GitHub API.

</td></tr><tr><td>

**Host / Domain**

</td><td>

Destination the rule applies to. Enter a host name such as `registry.example.com`, a wildcard such as `*.github.com` to cover every subdomain, or an IP range in CIDR notation such as `10.0.0.0/8`.

</td></tr><tr><td>

**Protocol**

</td><td>

Protocol the rule applies to. The default is **HTTPS**.

 -   **HTTPS**
-   **HTTP**
-   **gRPC**
-   **SMTP**
-   **TCP**
-   **Any**


</td></tr><tr><td>

**Access**

</td><td>

Whether the sandbox can reach the destination.

 -   **__Allow__**

Adds the destination to the allowlist. This is the default.

-   **__Deny__**

Blocks the destination. Use it to close one host inside a domain that another rule allows, for example, to block a single subdomain while `*.example.com` stays open.

</td></tr><tr><td>

**Allow Encoded Slash \(%2F\)**

</td><td>

Option to keep encoded slashes \(%2F\) in URL paths instead of rejecting the request. Cleared by default. Select it for services that need encoded slashes, such as GitLab project paths that include a namespace.

</td></tr><tr><td>

**Active**

</td><td>

Option to enforce the rule. Selected by default. An inactive rule is left out of the policy for every policy that links it.

</td></tr><tr><td>

**Enforcement**

</td><td>

How strictly Arc applies the rule.

 -   **__Enforce__**

Applies the rule. This is the default.

-   **__Audit — allow and log violation__**

Lets the traffic through and logs it as a violation. Use it to see what a rule would affect before you enforce it.

-   **__Disabled__**

Keeps the rule but doesn't apply it.

</td></tr><tr><td>

**Port**

</td><td>

Port the rule applies to, for example, 443, 80, 22, or 25. Leave it empty to apply the rule to any port.

</td></tr><tr><td>

**Justification**

</td><td>

Business or compliance reason for the rule, kept for your audit trail.

</td></tr></tbody>
</table>6.  Select **Create**.


## Result

The rule appears on the policy's **Network rules** tab, and the sandbox applies it for the users the policy covers at their next policy sync.

## Example: Let developers reach an internal package registry

Your developers need Arc to install packages from registry.example.com, which isn't on the default allowlist. On a policy whose user criteria cover the developer group, create a network rule with the following values:

-   **Rule Name**: `Allow internal package registry`
-   **Host / Domain**: `registry.example.com`
-   **Protocol**: **HTTPS**
-   **Access**: **Allow**
-   **Port**: `443`
-   **Justification**: `Developers install approved packages from the internal registry.`

Leave the other fields at their defaults. At their next policy sync, developers can reach the registry. Everyone else keeps the default allowlist, so the registry stays unreachable for them.

## What to do next

Confirm the rule works as intended on a test user's device before you widen the policy.

