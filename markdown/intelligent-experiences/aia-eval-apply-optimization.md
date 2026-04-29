---
title: Apply optimizations to agentic AI assets and reevaluate
description: Review and accept system-generated recommendations to improve agent quality based on detected issues. Apply optimizations before triggering a re-evaluation to confirm that changes resolved the failures.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 3
breadcrumb: [Review results, Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Apply optimizations to agentic AI assets and reevaluate

Review and accept system-generated recommendations to improve agent quality based on detected issues. Apply optimizations before triggering a re-evaluation to confirm that changes resolved the failures.

## Before you begin

You must have a completed agentic evaluation with issues identified.

Role required: admin

## About this task

If issues are identified by the LLM judges, they can generate suggestions for possible fixes to address the issues. After reviewing the issue, you can select **Start optimization** to check the recommendations before applying them and starting a reevaluation.

If you are already in the flow for identifying issues, skip to step 6.

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

2.  Select the automated evaluation you want to review the results of.

    The evaluation details page opens, displaying the overall results and performance metrics.

3.  If any issues are identified, select **Review and optimize** to view details.

    The optimization guided setup opens for that agentic AI asset.

    Each issue is associated with a specific tool or agentic AI asset.

4.  Select an issue to review.

5.  [Go over the issue](aia-eval-review-issues.md), including [analyzing issue traces](aia-eval-analyze-traces.md).

6.  Select issues to optimize, then select **Start optimization**.

    You can choose to optimize for as many issues as you want. It is possible to generate specific changes to an agentic AI asset that address multiple issues at once.

7.  Select **Yes** to generate the optimization suggestions.

8.  Review the suggested optimizations.

    Optimizations occur at the prompt level for tool or agentic AI asset descriptions and lists of steps.

    If an optimization is to a description or list of steps, you can toggle to see the current instructions by itself next to the suggestion for the optimized version. You can also toggle to show the differences between the current and suggested version or to see just the optimized version by itself.

    If you want to make edits to the suggested texts, you can toggle **Edit mode** to enter your own text or change the contents of the generated text.

    To open the tool or agentic AI asset in AI Agent Studio, select the open link ![](../../../reuse/icons/product-icons/open-link-right-outline-24.svg) icon. The associated agentic AI asset opens in a new browser tab.

    You can see the issues that the optimization is trying to address by selecting **Contributing issues**. You can select an issue to review all of the details, including the root cause analysis.

9.  Select **Continue to re-evaluate** if you want to re-evaluate without applying the optimization or **Review and apply** if you want to make the suggested changes.

10. Review the details for reevaluation.

    The optimization summary includes the list of issues that are being trying to be addressed by the optimization.

    You can name your evaluation and select the version of the agentic AI asset. Because this is a reevaluation, the evaluation metrics and dataset are the same as the original run and can't be changed.

11. Select **Start re-evaluation** to begin the new agentic evaluation run.

    You can go back to a previous step in the issue-optimization flow by selecting **Back to evaluation setup**.


## Result

A new evaluation run begins with any changes you applied to the agentic AI asset.

## What to do next

You can [track and monitor your agentic evaluation](track-aia-eval-progress.md) while the reevaluation is in-progress. After the evaluation is complete, you can review and compare the results against the original evaluation and make further optimizations if necessary.

