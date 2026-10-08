---
title: Action approval flow in ServiceNow Cowork
description: Tool gates, approval patterns, and auto approval determine whether each action in Cowork runs, requires approval, or is blocked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/action-approval-flow-cowork.html
release: australia
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 5
keywords: [Action approval]
breadcrumb: [Policy management and governance in ServiceNow Cowork, Explore Cowork, ServiceNow Cowork, Enable AI experiences]
---

# Action approval flow in ServiceNow Cowork

Tool gates, approval patterns, and auto approval determine whether each action in Cowork runs, requires approval, or is blocked.

Three controls determine whether an action runs. Tool gates set how Cowork handles each tool. Approval patterns identify commands that need approval. Auto approval lets an AI model reviewer approve some actions without prompting the user.

\[Omitted image "cowork-action-flow.png"\] Alt text: Flowchart showing how an action is evaluated through the active policy check, tool gate modes, approval patterns, auto approval, and environment controls.

Every action passes through these controls in the following order:

1.  Cowork checks for an active policy. If no active policy is available, Cowork refuses the action.

2.  Cowork applies the tool gate for the tool. **Allow** runs the action, **Deny** blocks it, the \(Human in the loop\) HITL sends it to approval patterns, and **Auto** sends it to auto approval.

3.  For HITL, Cowork compares the command against approval patterns. If no pattern matches, the action runs. If a hard gate pattern matches, Cowork prompts the user. If a soft gate pattern matches, the action runs when a saved approval exists. Otherwise, Cowork prompts the user.

4.  For **Auto**, Cowork prompts the user if the action is under a hard gate. Otherwise, the model reviewer approves the action or escalates it to the user.

5.  When prompted, the user approves the action to run it or denies the action to block it.

6.  When the action runs, sandbox, network, connector scope, and file type rules limit what the action can access.


## Gate strengths

Some actions require a human decision before they run. Approval patterns, described later in this topic, identify these actions and assign each one a gate strength:

|Gate|Behavior|Use|
|----|--------|---|
|Hard gate|Requires a human decision each time the action runs.|Destructive actions, such as actions that delete data or make changes to external systems|
|Soft gate|Requires a human decision, which the user can save for later occurrences of the action.|Routine actions with low impact that users repeat|

## Tool gates

You set a mode on each tool. The modes and the tools each mode suits are described in the following table.

|Mode|Behavior|Use|
|----|--------|---|
|Allow|Runs the action with no pattern matching and no prompt.|Tools with low impact, such as tools that only read data|
|Deny|Blocks the action with no option to approve it.|Tools that your organization doesn't permit|
|Human in the loop \(HITL\)|Checks the action against approval patterns.|Tools where specific commands require human review|
|Auto|Sends the action to auto approval.|Frequently used tools where repeated prompts slow users down|

Because **Auto** is a gate mode, you control it per tool. You can reduce prompts on one frequently used tool while keeping stricter handling on others.

## Approval patterns

Approval patterns identify the commands that need approval when a tool gate is set to **HITL**. The Default Policy includes predefined approval patterns organized by action category. Each pattern uses one of the match tiers in the following table.

|Tier|You configure|Matches when|
|----|-------------|------------|
|Pattern matching, exact|A literal string or regular expression|The command matches the pattern as written.|
|Pattern matching, relaxed fallback|A pattern of several words|The words appear in the command in order, even with flags and values between them.|
|Keyword matching|A list of write verbs|The command contains one of the listed verbs.|

**Note:** Under **HITL**, a command that matches no approval pattern runs without a prompt. If you rely on keyword matching, a command that writes data with a verb that isn't in your list runs without approval.

Use exact matching when you know the precise command to control. Exact matching can miss variations of that command. Use relaxed matching to catch variations, but relaxed matching can match a word that appears where you didn't intend. Use keyword matching to require approval for any command that writes data.

Cowork applies a fixed guard on credential paths that you can't turn off.

Each pattern has one of the following gate strengths:

-   **Hard gate**

    Requires a human decision each time the action runs.

-   **Soft gate**

    Requires a human decision, which the user can save for later occurrences of the action.


The Default Policy applies hard gates to destructive operations and actions that delete data or make changes to external systems, and soft gates to selected routine patterns with low impact.

Use a soft gate for routine actions that users repeat.

When a pattern requires approval, Cowork holds the action and displays an approval card to the user. The approval card offers **Allow** for every matched action and **Allow always** only for soft gate patterns.

When a user selects **Allow always**, Cowork saves the decision and runs later actions of the same type without a prompt, such as the same command run on different files. An action of a different type prompts the user again. Users can view and revoke saved approvals in **Settings** &gt; **Approvals**.

## Auto approval

When you set a tool gate to **Auto**, Cowork prompts the user for any action under a hard gate. An AI model reviewer evaluates every other action, including actions that match no pattern, against the user's request.

The model reviewer escalates actions that are destructive, irreversible, or visible outside Cowork. Some of these actions escalate every time. Others escalate unless the user's request clearly identifies what to act on. For example, "close INCXXXXXXX" identifies a specific record, but "clean up the incidents" doesn't. An approved action proceeds. An escalated action appears to the user as a standard approval card.

The model reviewer is an AI model, and its decisions may be inaccurate or inappropriate. Because the reviewer evaluates context, its decisions can vary. Hard gate actions go to the user for approval, not to the model reviewer. To keep a human review step for sensitive actions, place those actions under hard gates.

## Ways an action runs without a prompt

Under **HITL** or **Auto**, an action can run without a prompt in the ways described in the following table.

|Attribute|Saved approvals|Model review|
|---------|---------------|------------|
|Tool gate mode|HITL|Auto|
|Decision basis|A saved user decision for that type of action|An AI model's evaluation of the action in context|
|Set by|End user, one approval at a time|Administrator, by setting a tool gate to Auto|
|Scope|Soft gate patterns only|Actions not under a hard gate, including actions that match no pattern|
|Suited for|Repeated actions of a known, stable type|Actions that a static pattern can't classify in advance|

Neither method approves a hard gate action or runs an action on a tool set to **Deny**. Hard gate actions go to a human for approval.

Cowork also exempts read only commands from prompts, so routine work isn't interrupted.

**Parent Topic:**[Policy management and governance in ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/policy-management-cowork.md)

