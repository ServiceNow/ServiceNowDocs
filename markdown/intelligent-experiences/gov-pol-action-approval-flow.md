---
title: Action approval flow in ServiceNow Arc
description: Tool gates, approval patterns, and auto approval decide whether each action Arc attempts runs, waits for a person's approval, or is blocked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-action-approval-flow.html
release: australia
topic_type: concept
last_updated: "2026-10-23"
reading_time_minutes: 7
keywords: [action approval, tool gates, approval patterns, auto approval, hard gate, soft gate, arc policies]
breadcrumb: [Working with Arc policy rules, Managing Arc policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Action approval flow in ServiceNow Arc

Tool gates, approval patterns, and auto approval decide whether each action Arc attempts runs, waits for a person's approval, or is blocked.

Three controls decide whether an action runs. Tool gates set how Arc handles each tool. Approval patterns identify the commands that need a person's decision. Auto approval lets an AI model reviewer approve some actions without prompting the user.

\[Omitted image "cowork-action-flow.png"\] Alt text: Flowchart showing how an action is evaluated through the active policy check, tool gate modes, approval patterns, auto approval, and environment controls.

Every action passes through these controls in the following order:

1.  Arc checks for an active policy. If no active policy is available, Arc refuses the action.
2.  Arc applies the tool gate for the tool. An allow gate runs the action without checking approval patterns, and a deny gate blocks it. A gate that requires approval sends the action to approval patterns, and so does a tool with no gate. An auto approval gate sends it to auto approval.
3.  When approval patterns apply, Arc compares the command against them. If no pattern matches, the action runs. A hard gate match prompts the user. A soft gate match runs the action when a saved approval exists and prompts the user otherwise. An allow carve-out match runs the action without a prompt.
4.  Under auto approval, Arc prompts the user if the action is under a hard gate. Otherwise, the model reviewer approves the action or escalates it to the user.
5.  When prompted, the user approves the action to run it or denies it to block it.
6.  When the action runs, network, file type, sandbox, and connector scope rules limit what it can reach.

## Tool gates

Each tool gate has one of the following modes:

|Mode|Behavior|
|----|--------|
|Allow|Runs the action without checking approval patterns or prompting.|
|Deny|Blocks the action, with no option to approve it.|
|Require approval|Checks the action against approval patterns, and prompts the user only when a pattern calls for it.|
|Auto approval|Sends the action to the model reviewer, except actions under a hard gate. This happens only when the auto approval capability is on and the user's chat is in auto mode. Otherwise, the gate works as if it requires approval.|

A tool with no tool gate is handled as if its gate requires approval. Because auto approval is set on each tool gate, you can reduce prompts on one frequently used tool while keeping stricter handling on others.

## Approval patterns

Approval patterns identify the commands that need a person's decision. They apply to tools whose gate requires approval or uses auto approval, and to tools with no gate. The default Arc policy includes predefined patterns, grouped by category.

Each pattern matches commands in one of the following ways:

|Match mode|Pattern|Matches when|
|----------|-------|------------|
|Exact|A literal string or regular expression|The command matches the pattern as written.|
|Relaxed|Several words|The words appear in the command in order, even with flags and values between them.|
|Keyword|A list of write verbs|The command contains one of the listed verbs.|

Exact matching is precise but can miss variations of a command. Relaxed matching catches variations but can match a word that appears where you didn't intend. Keyword matching catches any command that writes data, as long as its verb is on your list.

**Note:** A command that matches no approval pattern runs without a prompt. If you rely on keyword matching, a command that writes data with a verb that isn't on your list runs without approval.

Each pattern also has a gate that sets what happens when a command matches:

|Gate|Behavior|
|----|--------|
|Hard gate|Asks the user every time. The user can't save the decision.|
|Soft gate|Asks the user, who can save the decision for later actions of the same type.|
|Allow carve-out|Runs the command without a prompt, as an exception to a broader pattern.|

The default Arc policy applies hard gates to destructive operations, deletions, and changes to external systems, and soft gates to selected routine, low-impact patterns.

When more than one pattern matches a command, the pattern that matches more of the command wins, even if it comes from a lower-priority policy. For details, see [Policy stacking and precedence in ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-policy-stacking-precedence.md).

## Auto approval

Under auto approval, Arc still prompts the user for any action under a hard gate. An AI model reviewer evaluates every other action, including actions that match no pattern, against the user's request.

The model reviewer escalates actions that are destructive, irreversible, or visible outside Arc. Some of these actions escalate every time. Others escalate unless the user's request clearly identifies what to act on. For example, "close INCXXXXXXX" identifies a specific record, but "clean up the incidents" doesn't. An approved action proceeds. An escalated action appears to the user as a standard approval card.

Auto approval works only when the auto approval capability is turned on for the user's policy and the user's chat is in auto mode. Otherwise, a tool gate set to auto approval works as if it requires approval. If the model reviewer is unavailable, times out, or returns a decision that Arc can't read, Arc shows the approval card. See [Create a capability override for an Arc policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-arc-create-capability-override.md).

**Important:** The model reviewer is an AI model, and its decisions may be inaccurate or inappropriate. Because the reviewer evaluates context, its decisions can vary. To keep a human review step for sensitive actions, put those actions under hard gates.

## What users see

When an action needs approval, Arc holds it and shows the user an approval card. The card offers **Allow** for every matched action, and **Always Allow** only for soft gate patterns. Steps that the model reviewer approves show **Auto-mode allowed this**.

When a user selects **Always Allow**, Arc saves the decision and runs later actions of the same type without a prompt, such as the same command run on different files. An action of a different type prompts the user again. Users can view and revoke saved approvals in **Settings** &gt; **Approvals**. For more about the user's experience, see .

When an action reads or changes a path outside the user's workspace folders but inside the home folder, Arc asks for approval. The approval card offers **Always Allow** unless the policy would apply a hard gate to the same action on its own, in which case the user approves it each time. Because the decision comes from the policy, a change to your approval patterns changes this behavior too.

Saved approvals and the model reviewer are the two ways an action can run without a prompt:

|Method|Decision basis|Set by|Applies to|Best for|
|------|--------------|------|----------|--------|
|Saved approval|A user's saved decision for that type of action|The user, one approval at a time|Soft gate patterns only|Repeated actions of a known, stable type|
|Model review|An AI model's evaluation of the action in context|An administrator, by turning on the auto approval capability and setting a tool gate to auto approval, and the user, by switching the chat to auto mode|Actions not under a hard gate, including actions that match no pattern|Actions that a static pattern can't classify in advance|

Neither method approves a hard gate action or runs an action on a tool with a deny gate.

## Built-in protections

Some checks are built into Arc and run before any approval pattern. No tool gate mode, approval pattern, or auto mode turns them off.

-   **Sensitive files**

    Commands that touch credential and key files, such as SSH keys, cloud provider credentials, password manager data, or browser profiles, always need the user's approval.

-   **Locations that run code automatically**

    Commands that write to locations where the operating system runs code automatically, such as scheduled tasks, always need the user's approval. On macOS, this also covers writes to folders in the user's Library folder that no sandbox rule allows.

-   **Environment variable hijacking**

    Commands that set environment variables that change how programs load, such as `LD_PRELOAD`, always need the user's approval.

-   **Arc configuration files**

    The agent can't read or change the files that hold Arc configuration and credentials. These commands are blocked, with no option to approve them.


For a tool whose gate requires approval, or a tool with no gate, Arc also asks for approval when a shell command writes to a file through a redirect, pipes its output into a program that isn't a safe pipe target, or uses shell syntax that can't be safely analyzed. Under an allow gate or an auto approval gate, these checks are skipped.

