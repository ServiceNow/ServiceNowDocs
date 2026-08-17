---
title: Enable evaluation for an AI system
description: Start generating quality and safety scores for one or more AI systems by enabling evaluation from the inventory.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/disc-enable-evaluation.html
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI, use]
breadcrumb: [Evaluating AI systems, Managing your AI asset inventory, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Enable evaluation for an AI system

Start generating quality and safety scores for one or more AI systems by enabling evaluation from the inventory.

## Before you begin

Before enabling evaluation for an AI system at the asset level, activate evaluation scoring for AI systems.

-   For ServiceNow AI systems, see [Activate evaluation scoring for ServiceNow AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-monitor-servicenow-ai-system.md).
-   For external AI systems, see [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-monitor-external-ai-system.md).

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory**.

2.  On the Overview tab, enable evaluation for one or more AI systems.

<table><thead><tr><th align="left" id="d121540e132">

Option

</th><th align="left" id="d121540e135">

Steps

</th></tr></thead><tbody><tr><td id="d121540e141">

**Enable evaluation for a single AI system**

</td><td>

1.  Select the AI system's display name to open its asset record.
2.  From the **Actions** list, select **Turn on evaluation**.
3.  In the confirmation dialog box, review the AI system that you selected.
4.  Select **Turn on evaluation** to confirm.


</td></tr><tr><td id="d121540e174">

**Enable evaluation for multiple AI systems**

</td><td>

1.  Select the check box for each AI system that you want to enable evaluation for.
2.  From the **Action** list, select **Turn on evaluation**.
3.  In the confirmation dialog box, review each AI system that you selected and its current state, and optionally remove any AI system that you don't want to update.
4.  Select **Turn on evaluation** to confirm.


</td></tr></tbody>
</table>
## Result

Evaluation is enabled for each AI system that you selected.

-   New evaluation scores appear on the **Monitor** tab of each asset record within minutes.
-   Historical scores for ServiceNow and external systems are saved.
-   You can turn off evaluation for these assets at any time. See [Disable evaluation for an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-disable-evaluation.md).

