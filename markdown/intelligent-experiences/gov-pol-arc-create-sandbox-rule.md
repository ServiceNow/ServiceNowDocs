---
title: Create a sandbox rule for an Arc policy
description: Restrict the reach of ServiceNow Arc agent commands by limiting the paths, binaries, system calls, and environment variables the sandbox can use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-arc-create-sandbox-rule.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, sandbox rule, filesystem rule, binary rule, syscall rule, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create a sandbox rule for an Arc policy

Restrict the reach of ServiceNow Arc agent commands by limiting the paths, binaries, system calls, and environment variables the sandbox can use.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

Arc runs agent commands in an isolated sandbox on the user's device. Sandbox rules add restrictions to that sandbox. They can't remove its built-in protection of credential paths and system directories.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy you want to update.

3.  Select **More**.

4.  Select **Sandbox rules**.

5.  Select **Create sandbox rules**.

    If the policy already has sandbox rules, select **+ Add rule** instead.

6.  On the form, fill in the fields.

<table id="table_sandbox_rule_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Rule Name**

</td><td>

Name that describes what the rule does, for example, Allow curl binary or Read-only /etc.

</td></tr><tr><td>

**Rule Type**

</td><td>

What the rule controls.

 -   **__Filesystem__**

A file or directory path in the sandbox.

-   **__Binary__**

A program in the sandbox and the network access it gets.

-   **__Syscall__**

A system call that programs in the sandbox can make.

-   **__Environment Variable__**

An environment variable in the sandbox.

</td></tr><tr><td>

**Access Mode**

</td><td>

Access the sandbox gets to the path, binary, system call, or variable.

 -   **Read Only**
-   **Read / Write**
-   **Allow**
-   **Deny**
 Use **Read Only** or **Read / Write** for filesystem paths, and **Allow** or **Deny** to permit or block a binary or system call. To keep agent actions from changing a path, select **Deny**.

</td></tr><tr><td>

**Path / Binary / Syscall**

</td><td>

Target of the rule. Glob patterns are supported. For a filesystem rule, enter a path such as `/home/*`. For a binary rule, enter the program's path such as `/usr/bin/curl`. For a syscall rule, enter the system call name such as `ptrace`.

</td></tr><tr><td>

**Apply to UID**

</td><td>

User ID in the sandbox the rule applies to. Leave it empty to apply the rule to every user ID. 998 is the sandbox user. Rules don't apply to root \(0\), which runs the sandbox's startup scripts.

</td></tr><tr><td>

**Active**

</td><td>

Option to enforce the rule. Selected by default. An inactive rule is left out of the policy for every policy that links it.

</td></tr><tr><td>

**Description**

</td><td>

Compliance reason for the rule, kept for your audit trail.

</td></tr></tbody>
</table>7.  Select **Create**.


## Result

The rule appears on the policy's **Sandbox rules** tab, and the sandbox applies it for the users the policy covers at their next policy sync.

## Example: Let the agent read a shared folder but not change it

Your analysts keep approved templates in a reference folder in their home directory. Arc should be able to read the templates but never edit or delete them. Create a sandbox rule with the following values:

-   **Rule Name**: `Read-only reference templates`
-   **Rule Type**: **Filesystem**
-   **Access Mode**: **Read Only**
-   **Path / Binary / Syscall**: `/home/*/reference`
-   **Description**: `Protect approved templates from agent changes.`

The \* in the path matches any user's home directory, so one rule covers every analyst. Leave **Apply to UID** empty so the rule applies to every user ID in the sandbox except root.

## What to do next

For a worked example that protects the sandbox runtime directory with a filesystem deny rule, see .

