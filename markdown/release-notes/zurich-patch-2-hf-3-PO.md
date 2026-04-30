---
title: Zurich Patch 2 Hotfix 3
description: The Zurich Patch 2 Hotfix 3 release contains fixes to these problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-20"
reading_time_minutes: 2
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 2 Hotfix 3

The Zurich Patch 2 Hotfix 3 release contains fixes to these problems.

-   **Build information:**

    Build date: 11-18-2025\_1831

    Build tag: glide-zurich-07-01-2025\_\_patch2-hotfix3-11-14-2025


**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

## Fixed problem

<table id="all-other-fixes"><thead><tr><th>

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

AI Agents \(Glide Family\)

 PRB1963825

</td><td>

Update AI Agents \(AIA\) true-up version to 4.0.38

</td><td>

Updating the AIA true-up version to fix a potential infinite loop in an upgrade scenario.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1947698

</td><td>

Only one agentic workflow executes successfully when the same trigger fires simultaneously

</td><td>

When a workflow trigger fires simultaneously multiple times, only one of the resulting agentic workflows executes successfully. The other workflows terminate immediately with an error indicating that no session ID could be found. Each trigger correctly creates a new execution plan and a new conversation record, but only one conversation proceeds, while the others fail at the start.

</td><td>

1.  Create the agentic workflow named 'Test multiple case executions'.
2.  Select three or more case records and update them simultaneously so that the trigger fires for all at once.
3.  Notice that the three execution plans \(sn\_aia\_execution\_plan\) and three conversation records are created. Only one conversation and execution plan executes successfully. The other conversations don't continue after the first task with the error 'No session ID found'.

 Expected behavior: Each triggered workflow should independently create or resolve its own valid session so that all conversations execute successfully, even under concurrent trigger conditions.

 Actual behavior: Only one conversation executes successfully. The other conversations either terminate immediately or don't continue after the first task with 'No session ID found' error.

</td></tr><tr><td>

Virtual Agent

 PRB1962510

</td><td>

Empty sys\_cs\_message is created when Agentic Mode is on

</td><td>

 

</td><td>

1.  Set up NAVA.
2.  Make sure Agentic Mode is turned on.
3.  Search 'What is spam?'.
4.  Navigate to sys\_cs\_message.
5.  Check for an empty message.

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1956730

</td><td>

Live agent only mode doesn't work for third-party channels

</td><td>

The user messages aren't be received by the agent. This message appears in the log: 'Couldn't find rich control, dropping current message'.

</td><td>

1.  Set up VA and a third-party channel \(for example, Teams\).
2.  Set up VA to live-agent only mode \(for example, by having a custom greeting topic that directs to LA\).
3.  Start the conversation.
4.  Accept as agent.
5.  Attempt to send messages as a user.

 Observe that the user messages aren't received by the agent with this message in the log: 'Couldn't find rich control, dropping current message'.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 2 Hotfix 2](https://downloads.docs.servicenow.com/enus/zurich/rn/hotfix/zurich-patch-2-hf-2.pdf)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)

