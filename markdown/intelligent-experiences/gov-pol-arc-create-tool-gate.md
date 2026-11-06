---
title: Create a tool gate for an Arc policy
description: Decide how ServiceNow Arc handles a tool, such as the shell or an MCP server tool, by letting it run, blocking it, or sending its calls for review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-arc-create-tool-gate.html
release: australia
topic_type: task
last_updated: "2026-10-22"
reading_time_minutes: 5
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, tool gate, gate mode, safe pipe targets, transparent prefixes, auto approval, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Create a tool gate for an Arc policy

Decide how ServiceNow Arc handles a tool, such as the shell or an MCP server tool, by letting it run, blocking it, or sending its calls for review.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward and sn\_app\_arc.admin

## About this task

A tool gate is the first check Arc applies when the agent calls a tool. The gate's mode decides whether the call runs, is blocked, or goes on to approval patterns or an AI classifier for review. Built-in safety checks, such as protection of credential paths, still apply whatever mode you choose.

The **Safe Pipe Targets** and **Transparent Prefixes** fields matter only for a gate on the bash tool, where they decide when piped commands and command chains need approval. Neither field has any effect when the gate is set to **Allow**, and **Safe Pipe Targets** also has no effect when it's set to **Auto Approval**.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies** &gt; **Arc policies**.

2.  Select the policy you want to update.

3.  Select the **Tool gates** tab.

4.  Select **Create tool gates**.

    If the policy already has tool gates, select **+ Add rule** instead.

5.  On the form, fill in the fields.

<table id="table_tool_gate_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Tool Name**

</td><td>

Tool the gate controls. Enter the tool's ID exactly as Arc names it, for example, `bash` or `remove_path` for a built-in tool, or `github/create_pr` for a tool from an MCP server.

 To control every tool on one MCP server with a single gate, enter the server name followed by /\*, for example, `github/*`. A gate for a specific tool takes precedence over a wildcard gate.

 The default Arc policy gates the `bash`, `send_message`, and `remove_path` tools. A gate in your policy for the same tool name replaces the default gate for the users your policy covers.

</td></tr><tr><td>

**Tool Type**

</td><td>

Kind of tool the gate applies to.

 -   **Built-in**
-   **MCP**
-   **Skill**
-   **Workflow**
-   **Plugin / External**


</td></tr><tr><td>

**Gate Mode**

</td><td>

How Arc handles calls to the tool.

 -   **__Allow__**

Runs every call without checking approval patterns. Use it for low-impact tools, such as tools that only read data. This is the default.

-   **__Deny — hard block__**

Blocks every call to the tool, with no option for the user to approve it. Use it for tools your organization doesn't permit.

-   **__Require Approval — HITL every call__**

Checks each call against the policy's approval patterns. A call that matches a pattern waits for the user's decision. A call that matches no pattern runs without a prompt, so pair this mode with approval patterns that cover the commands you want reviewed.

-   **__Auto Approval — classifier check when the user is in auto mode \(needs the Auto Mode capability\)__**

When the user switches a chat to auto mode, an AI safety classifier reviews each call instead of asking the user. Anything the classifier blocks or can't assess still goes to the user, and actions under a hard gate approval pattern always ask the user.

Auto mode is available only when the **auto\_approval** capability is turned on for the user's policy. While it's off, or when the chat isn't in auto mode, this gate behaves like **Require Approval**. To turn it on, see [Create a capability override for an Arc policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-capability-override.md).

The classifier is an AI model, and its decisions may be inaccurate. To keep a person in the loop for sensitive actions, cover them with hard gate approval patterns.

</td></tr><tr><td>

**Active**

</td><td>

Option to enforce the gate. Selected by default. An inactive gate is left out of the policy for every policy that links it. Calls to the tool are then handled by any other gate that matches the tool, such as a wildcard gate or a gate in another policy that applies to the user. If no gate matches, calls are checked against approval patterns.

</td></tr><tr><td>

**Description**

</td><td>

Reason for the gate, kept for your audit trail, for example, the compliance requirement it meets.

</td></tr><tr><td>

**Safe Pipe Targets \(read-only filters\)**

</td><td>

Commands that are safe to receive another command's output, for a gate on the bash tool. List commands that only read their input and never run code or write files, separated by commas, for example, `head,tail,grep,wc,sort,uniq,cut,cat,jq,column`.

 When a command pipes its output to other commands, such as `cat app.log | grep error`, Arc treats it as read-only only if every command after a pipe is on this list. Any other target, such as a shell, an interpreter like `python3`, `xargs`, or `tee`, sends the command for approval.

 If you leave this field empty, every piped command needs approval. Arc has no fallback list.

 The bash gate in the default Arc policy ships with a list of common read-only commands. A bash gate in your policy replaces the default gate, so start from that list rather than an empty field. The list follows this table.

</td></tr><tr><td>

**Transparent Prefixes \(safe shell builtins\)**

</td><td>

Shell builtins that only change the shell's own state, for a gate on the bash tool. List them separated by commas, for example, `cd,pushd,popd,export,set,unset,umask`.

 When a command chain starts with one of these, such as `cd /skills/report && python3 run.py`, Arc skips the prefix and checks the rest of the chain against approval patterns. It also uses the rest of the chain when it saves an **Always Allow** decision, so moving to another folder first doesn't change what the user approved.

 If you leave this field empty, Arc checks every part of the chain on its own. Don't add `source` or `.`, because sourcing a file runs its contents as shell code.

</td></tr></tbody>
</table>    Safe pipe targets in the bash gate of the default Arc policy:

    ```
    head,tail,cat,tac,rev,nl,grep,egrep,fgrep,rg,ag,wc,sort,uniq,cut,tr,fold,fmt,column,comm,paste,join,look,expand,unexpand,pr,less,more,jq,yq,cksum,md5sum,sha1sum,sha256sum,sha512sum,xxd,od,hexdump,strings,base64
    ```

6.  Select **Create**.


## Result

The tool gate appears on the policy's **Tool gates** tab, and Arc applies it for the users the policy covers at their next policy sync.

## Example: Keep the agent from opening pull requests

Your users connect Arc to GitHub to read code and review issues, but your security team doesn't permit an agent to open pull requests. Create a tool gate with the following values:

-   **Tool Name**: `github/create_pr`
-   **Tool Type**: **MCP**
-   **Gate Mode**: **Deny — hard block**
-   **Description**: `Agents can't open pull requests, per the source control policy.`

A tool from an MCP server is named with the server, a slash, and the tool, so this gate affects only the pull request tool. Users can still read code and issues through the GitHub connector, but any attempt to open a pull request is blocked.

## What to do next

If you set the gate to **Require Approval**, add approval patterns for the commands you want reviewed. For details, see [Create an approval pattern for an Arc policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-approval-pattern.md).

