---
title: Set agent limits and safeguards
description: Set limits on how long the agent runs and when it checks in with you, so it doesn't use more time or resources than a task needs and you stay in control of long runs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/set-agent-limits-safeguards.html
release: zurich
topic_type: task
last_updated: "2026-09-27"
reading_time_minutes: 1
keywords: [agent controls, max turns, check in turn, soft deletes, Read Aloud]
breadcrumb: [Use, ServiceNow Cowork, Enable AI experiences]
---

# Set agent limits and safeguards

Set limits on how long the agent runs and when it checks in with you, so it doesn't use more time or resources than a task needs and you stay in control of long runs.

## Before you begin

Role required: sn\_app\_cowork.user

## About this task

These limits work alongside the agent's own retry limit. When the agent makes several attempts at the same task without success, it stops and reports the problem instead of retrying indefinitely.

When a policy blocks an action, the agent reports the block and the reason and makes no further attempts. It doesn't try to work around the block.

## Procedure

1.  Navigate to **Settings** &gt; **General**.

2.  Scroll down to **Agent controls**.

3.  In **Max turns**, move the slider to the number of turns the agent can take before it stops with an error.

4.  In **Check-in at turn**, move the slider to the turn where the agent pauses and prompts you to confirm whether to continue.

    To turn off the pause, move the slider to 0. Set this value lower than **Max turns** so that the pause occurs before the hard stop.

5.  Select **Let the agent decide** to have the agent evaluate its own progress at the **Check-in at turn** instead of pausing.

    The agent still pauses when it cannot determine how to proceed.

6.  Select **Read Aloud** to listen to long responses through your browser's built-in text-to-speech feature.

    A speaker button appears on agent responses.

7.  Select **Soft Deletes** to keep deleted files and folders recoverable.

    The agent moves deleted items to a `dump/` directory with restore instructions instead of removing them permanently.

8.  In **Retention \(days\)**, specify how many days to keep deleted items.

    On startup, items older than the retention period are permanently removed.

9.  Select **Browse Deleted Files** to view or restore deleted items.

10. Select **Reset to defaults** to return all settings to their original values.


## Result

The agent uses your settings on its next run.

**Parent Topic:**[Using ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-using.md)

