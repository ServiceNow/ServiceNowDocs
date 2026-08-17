---
title: Disable evaluation for an AI system
description: Stop generating evaluation scores for one or more AI systems by disabling evaluation from the inventory, while preserving all historical score data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/disc-disable-evaluation.html
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI, use]
breadcrumb: [Evaluating AI systems, Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Disable evaluation for an AI system

Stop generating evaluation scores for one or more AI systems by disabling evaluation from the inventory, while preserving all historical score data.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_ai\_governance.ai\_steward

**Note:** Users with the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role can only disable evaluations for assets that they own.

## About this task

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory**.

2.  On the Overview tab, disable evaluation for one or more AI systems.

<table><thead><tr><th align="left" id="d134845e101">

Option

</th><th align="left" id="d134845e104">

Steps

</th></tr></thead><tbody><tr><td id="d134845e110">

**Disable evaluation for a single AI system**

</td><td>

1.  Select the AI system's display name to open its asset record.
2.  From the **Actions** list, select **Turn off evaluation**.
3.  In the confirmation dialog box, review the AI system that you selected.
4.  Select **Turn off evaluation** to confirm.


</td></tr><tr><td id="d134845e143">

**Disable evaluation for multiple AI systems**

</td><td>

1.  Select the check box for each AI system that you want to disable evaluation for.
2.  From the **Action** list, select **Disable evaluation**.
3.  In the confirmation dialog box, review each AI system that you selected and its current state, and optionally remove any AI system that you don't want to update.
4.  Select **Turn off evaluation** to confirm.


</td></tr></tbody>
</table>
## Result

Evaluation is turned off for each AI system that you updated.

-   New evaluation scores stop appearing within a few hours.
-   Historical scores are saved and remain visible on the **Monitor** tab of each asset record.
-   You can re-enable evaluation for these AI systems at any time, as long as they are managed.

## What to do next

To resume scoring, see [Enable evaluation for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-enable-evaluation.md).

