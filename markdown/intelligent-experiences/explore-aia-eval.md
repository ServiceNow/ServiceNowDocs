---
title: Explore agentic evaluations
description: Automated evaluations test your agentic AI assets and help determine when they're ready for production. Learn more about how evaluations work, who they’re designed for, and the benefits they deliver.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-18"
reading_time_minutes: 3
keywords: [explore]
breadcrumb: [Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Explore agentic evaluations

Automated evaluations test your agentic AI assets and help determine when they're ready for production. Learn more about how evaluations work, who they’re designed for, and the benefits they deliver.

## Agentic evaluations overview

Automated agentic evaluations help give AI agent builders the confidence to deploy with objective, explainable evidence that their agents are ready for production. They remove the guesswork from quality assurance by running your agent against a defined dataset and applying LLM-powered judges to score quality, such as task completeness, response accuracy, and tool use. From there, the system generates recommended optimizations you can apply before triggering a re-evaluation to confirm improvements.

Building agentic AI assets like AI agents and agentic workflows is an iterative process. Agentic evaluations are designed to verify the quality of the AI asset with in a structured way to help speed up the process. Because you're testing against representative datasets, you can be more confident in the performance of your agentic AI asset to handle real-world situations.

Agentic evaluations can be run in non-production environments and don't require live deployment. They can be run during testing phases of agentic AI assets to help ensure that they can be deployed to a production environment while meeting your benchmarks and standards.

## Agentic evaluations users

|User|Description|
|----|-----------|
|Agent builder|Developer or configurator who builds agents in AI Agent Studio. Automated evaluations are designed so agent builders can run rigorous evaluations at scale.|
|Platform administrators|Platform administrators who govern which agents are approved for production can use automated evaluation results for evidence of quality before deployment.|
|AI leads and architects|AI leads and architects can use automated evaluation results for audit trails and quality metrics across multiple agents.|

## Automated evaluations workflow

1.  Configure an evaluation run with a name, selected agentic AI asset and its version, metrics, and dataset.
2.  Execute the run and track progress as the LLM judges agentic responses.
3.  Analyze the run results, including the judge scores and identified issues and traces.
4.  Optimize the agentic AI asset with targeted recommendations, then trigger reevaluations.
5.  Validate the quality of future runs or other changes to the agentic AI asset.

## Automated evaluations benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Evaluate specific versions of agentic AI assets for quality|[Execute an evaluation run](evaluating-aia.md)|Agent builders|
|Set your own standards for agentic AI responses and performance|[Custom metrics](../task/create-custom-metric.md)|Agent builders, Platform administrators, AI leads, and architects|
|Track evaluations as they progress|[In-progress results](../task/track-aia-eval-progress.md)|Agent builders|
|Identify issues and trace them back to the source|[Evaluation outputs](../task/review-aia-eval-outputs.md)|Agent builders, AI leads, AI architects|
|Optimize agentic AI assets based on evaluation results|[System-generated optimization recommendations](../task/aia-eval-apply-optimization.md)|Agent builders|

## What to explore next

To learn more about configuring and using agentic evaluations, see:

-   [Evaluating agentic AI assets](evaluating-aia.md)
-   [Reference for agentic evaluations](../reference/ref-aia-eval.md)

