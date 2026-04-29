---
title: Review issues discovered in agentic evaluations
description: Identify and prioritize specific quality failures detected during an evaluation run, organized by severity. Use issue severity and metric relevance to decide which failures to address before deployment.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 2
breadcrumb: [Review results, Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Review issues discovered in agentic evaluations

Identify and prioritize specific quality failures detected during an evaluation run, organized by severity. Use issue severity and metric relevance to decide which failures to address before deployment.

## Before you begin

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

2.  From the list, select the automated evaluation you want to review.

    The evaluation details page opens, displaying the overall results and performance metrics.

3.  If any issues are identified, select **Review and optimize** to view details.

    The optimization guided setup opens for that agentic AI asset.

    Each issue is associated with a specific tool or agentic AI asset.

4.  From the issues list, select an issue to review.

    Each issue has a description of what the issue is, a root cause analysis, traces associated with it, and a space for adding notes about the analysis.

<table><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Issue score and short description

</td><td>

Brief overview of the identified issue and its impact on the agentic AI asset

</td></tr><tr><td>

Description

</td><td>

More detailed information about the identified issue than the short description

</td></tr><tr><td>

Root cause analysis

</td><td>

Insights into the cause of the symptoms seen in the agentic AI asset. Identifies specific components of the issue and which metric discovered it.

</td></tr><tr><td>

Traces with this issue

</td><td>

Specific execution logs where the issue is seen. You can [analyze traces](aia-eval-analyze-traces.md) to understand how the issue manifests.

</td></tr><tr><td>

Analysis notes

</td><td>

Space for you to add details about the analysis and what you want to communicate to others about the issue. These notes aren't considered when applying optimizations. See [Apply optimizations](aia-eval-apply-optimization.md) for more information.

</td></tr></tbody>
</table>5.  [Analyze the traces of the issue](aia-eval-analyze-traces.md).

6.  After reviewing the identified issues, select **Start optimization** to see the LLM-recommended fixes.


## Result

Issues associated with the metrics for different components of the agentic AI asset are reviewed, analyzed, and documented.

## What to do next

Proceed to the next step to [apply optimizations](aia-eval-apply-optimization.md) to fix identified issues.

