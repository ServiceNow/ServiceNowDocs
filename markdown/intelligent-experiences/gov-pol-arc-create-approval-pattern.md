---
title: Create an approval pattern for an Arc policy
description: Pause destructive or outbound commands for a person's decision, or let trusted routine commands run without a prompt, by matching them with an approval pattern.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-arc-create-approval-pattern.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, approval pattern, hard gate, soft gate, allow carve-out, match mode, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create an approval pattern for an Arc policy

Pause destructive or outbound commands for a person's decision, or let trusted routine commands run without a prompt, by matching them with an approval pattern.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

Approval patterns apply to calls from tools whose tool gate is set to **Require Approval** or **Auto Approval**, and from tools that have no tool gate. A tool gate set to **Allow** skips approval patterns, and a gate set to **Deny — hard block** blocks the tool before patterns are checked. When a command matches more than one pattern, the most specific match wins. A command that matches no pattern runs without a prompt. Arc always protects credential paths and other sensitive operations, whatever a pattern allows.

For how patterns work with tool gates and auto approval, see [Action approval flow in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-action-approval-flow.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy you want to update.

3.  Select the **Approval patterns** tab.

4.  Select **Create approval patterns**.

    If the policy already has approval patterns, select **+ Add rule** instead.

5.  On the form, fill in the fields.

<table id="table_approval_pattern_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Label**

</td><td>

Short name that identifies the pattern in lists, for example, Send Gmail or Block recursive delete.

</td></tr><tr><td>

**Description**

</td><td>

Purpose of the pattern, for other administrators who review it later.

</td></tr><tr><td>

**Category**

</td><td>

Area the commands belong to, which groups related patterns in the list.

 -   **Google Suite**
-   **Microsoft 365**
-   **ServiceNow**
-   **Filesystem**
-   **Communication**
-   **Browser**
-   **General**


</td></tr><tr><td>

**Domain**

</td><td>

Domain that owns the pattern. Keep the default unless your instance uses domain separation.

</td></tr><tr><td>

**Pattern**

</td><td>

What to match in the command. Its format depends on **Match Mode**.

 -   For **Exact** or **Relaxed**, enter the text or regular expression to match, for example, `rm -rf`.
-   For **Keyword**, enter single-word verbs separated by commas, for example, `send,create,delete,rm`.
 The maximum length is 4,000 characters.

</td></tr><tr><td>

**Match Mode**

</td><td>

How strictly the pattern has to match the command.

 -   **__Exact — fast string match__**

The pattern's words must appear next to each other, in order, with nothing between them. Use it for short, precise rules. This is the default.

-   **__Relaxed — token-in-order match__**

The pattern's words must appear in order, but flags and arguments can sit between them. Use it when you can't predict every flag order. For example, a relaxed pattern for `rm -rf` also matches `rm -v -rf`.

-   **__Keyword — comma-separated write verbs__**

Any listed verb matches as a whole word anywhere in the command. Use it as a broad safety net that catches every command of a kind, rather than for a single command. Keyword patterns require a specific **Tool Filter**.

</td></tr><tr><td>

**Tool Filter**

</td><td>

Tool the pattern applies to, for example, `bash`. Leave it empty or enter `*` to apply the pattern to every tool. Required when **Match Mode** is **Keyword**, and then it can't be empty or \*.

</td></tr><tr><td>

**Gate**

</td><td>

What happens when a command matches.

 -   **__Hard Gate__**

Asks the user every time, with no option to save the decision. Use it for destructive actions and changes to external systems. This is the default.

-   **__Soft Gate__**

Asks the user, and offers **Always Allow** so the user can save the decision for later commands of the same type. Use it for low-impact actions users repeat.

-   **__Allow — carve-out__**

Runs the command without a prompt. Use it to exempt a specific trusted command from a broader rule. Built-in safety checks still apply.

</td></tr><tr><td>

**Priority**

</td><td>

Tiebreaker among patterns that match a command equally well. A lower number wins. The default is 100.

 A more specific match always wins first, whatever its number. To loosen a broad rule without weakening a narrower one, add your exception as an equally specific pattern instead of lowering this number.

</td></tr><tr><td>

**Requires TOTP**

</td><td>

Option to require a code from the user's authenticator app, and their approval, for high-risk commands. Cleared by default. Users set up their authenticator in the Arc application. For details, see .

</td></tr><tr><td>

**Active**

</td><td>

Option to enforce the pattern. Selected by default. An inactive pattern is left out of the policy for every policy that links it.

</td></tr></tbody>
</table>6.  Select **Create**.


## Result

The pattern appears on the policy's **Approval patterns** tab, and Arc applies it for the users the policy covers at their next policy sync.

## Example: Require approval before infrastructure changes

Your platform engineers use Arc to work on Terraform code. Planning a change is safe, but applying one changes live infrastructure, so every apply needs the engineer's approval. Create an approval pattern with the following values:

-   **Label**: `Approve Terraform apply`
-   **Category**: **General**
-   **Pattern**: `terraform apply`
-   **Match Mode**: **Relaxed — token-in-order match**
-   **Tool Filter**: `bash`
-   **Gate**: **Hard Gate**

Relaxed matching catches the command even when an option sits between the words, such as `terraform -chdir=infra apply`, which an exact match would miss. The tool filter limits the pattern to shell commands. Because the gate is hard, the engineer approves every apply. The pattern doesn't affect `terraform plan`.

## What to do next

If the tool the pattern targets has a tool gate set to **Allow**, the pattern has no effect until you change the gate. For details, see [Create a tool gate for an Arc policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-tool-gate.md).

