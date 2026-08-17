---
title: Resolve an AI recommendation
description: Address an issue or opportunity by running an unsupervised agent, working through a guided conversation with a supervised agent, or resolving the issue yourself.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ac-resolve-ai-recommendation.html
release: zurich
topic_type: task
last_updated: "2026-04-23"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Resolve recommendations, Address action items, AI Control Tower, Enable AI experiences]
---

# Resolve an AI recommendation

Address an issue or opportunity by running an unsupervised agent, working through a guided conversation with a supervised agent, or resolving the issue yourself.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Activity Center** &gt; **Recommendations**.

2.  Identify the recommendation that you want to resolve.

    In the **Refine list** panel, you can narrow the list by applying filters for category, priority, confidence, outcome, completion status, or asset.

3.  Review the details of the recommendation by selecting **View details** from the action menu.

    The side panel shows the reasoning behind the recommendation, the asset or scope it applies to, and the history of any earlier runs.

4.  Resolve the recommendation using AI automation, AI review, or resolve the issue yourself.

<table><thead><tr><th align="left" id="d44738e111">

Option

</th><th align="left" id="d44738e114">

Description

</th></tr></thead><tbody><tr><td id="d44738e120">

**Automate using AI**

</td><td>

1.  Select **Automate using AI**.
2.  Confirm the action when prompted. AI Control Tower runs an unsupervised agent that executes the resolution workflow on your behalf.
3.  Monitor progress in the side panel. The **Focused** view shows the steps the agent is taking and the estimated time to complete. The recommendation status moves to **In progress** while the agent runs and to **Complete** when the work is done.


</td></tr><tr><td id="d44738e156">

**Review with AI**

</td><td>

1.  In the chat interface, work through the supervised agent's proposed actions one at a time. Accept, refine, or reject each action based on your judgment.
2.  Close the conversation when the agent reports that the recommendation is resolved. The recommendation status moves to **Complete**.


</td></tr><tr><td id="d44738e177">

**Open**

</td><td>

1.  Select **Open**. AI Control Tower redirects you to the record, page, or workflow where you can resolve the issue directly.
2.  In the record, page or workflow, take the action required to resolve the issue.
3.  Return to the Activity Center Recommendations view. After AI Control Tower detects that the underlying condition is resolved, the recommendation status moves to **Complete**. To mark the recommendation as resolved manually, select **Complete** from the action menu on the card.


</td></tr></tbody>
</table>
## Result

The recommendation status moves to **Complete** and the recommendation is removed from the default Recommendations list. To see completed recommendations, open the **Refine list** panel and select **Completed** in the **Completion status** filter.

