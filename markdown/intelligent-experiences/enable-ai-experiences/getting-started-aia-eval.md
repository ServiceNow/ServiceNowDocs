---
title: Getting started with agentic evaluations
description: Learn what you need to run your first agentic evaluation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/enable-ai-experiences/getting-started-aia-eval.html
release: australia
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: task
last_updated: "2026-03-18"
reading_time_minutes: 1
keywords: [automated evaluations]
breadcrumb: [Evaluate, Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Getting started with agentic evaluations

Learn what you need to run your first agentic evaluation.

## Before you begin

Before you start your first execution run, ensure that you have the following:

-   An agentic AI asset that has been built and saved in AI Agent Studio
-   At least one version of the agentic AI asset
-   Available dataset with a minimum number of test cases. You can create new datasets using [Now Assist Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md).
-   You have the necessary permissions to run the agentic AI asset. You can verify whether you have the right permissions by checking the user access settings of the agentic AI asset in AI Agent Studio.

Role required: sn\_aia.admin

## Procedure

1.  Navigate to **All** &gt; **Now Assist Skill Kit** &gt; **Agentic Evaluations**.

2.  Select **Create new evaluation run**.

3.  Name the run and select the agentic AI asset and version.

    See [Version control for agentic AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/version-control.md) for more information about maintaining different versions of your agentic AI list of steps.

4.  Select the metrics to evaluate.

5.  Configure the data for the run.

    You can select a pre-existing dataset, create a new dataset using previous execution logs of the agentic AI asset, or generate new execution logs as part of executing the evaluation run.

6.  Review the configuration summary and submit.

7.  [Monitor progress and review logs when prompted.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/track-aia-eval-progress.md)

8.  [Review results, issues, and traces once the run completes.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/review-aia-eval-outputs.md)

9.  [Apply recommended optimizations and trigger a re-evaluation.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/aia-eval-apply-optimization.md)


