---
title: Reference for agentic evaluations
description: Find technical reference material for roles, metrics, and output formats of agentic evaluations.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-18"
reading_time_minutes: 1
keywords: [reference]
breadcrumb: [Evaluate agentic AI assets, Now Assist AI agents, Enable AI experiences]
---

# Reference for agentic evaluations

Find technical reference material for roles, metrics, and output formats of agentic evaluations.

## Available metrics

<table><thead><tr><th>

Metric

</th><th>

What it measures

</th><th>

Ground truth required

</th></tr></thead><tbody><tr><td>

Task completeness

</td><td>

Whether the agentic AI asset fully addresses the user need.

</td><td>

Optional

</td></tr><tr><td>

Response accuracy

</td><td>

Whether the agentic AI asset's response is factually accurate

</td><td>

Recommended

</td></tr><tr><td>

Groundedness

</td><td>

Whether the agentic AI asset's response is grounded in the specific context of the task

</td><td>

No

</td></tr><tr><td>

Coherence

</td><td>

Whether the agentic AI asset's response is logically structured and clear

</td><td>

No

</td></tr><tr><td>

Tool use accuracy

</td><td>

Whether the agentic AI asset selected and used the correct tool to execute its tasks

</td><td>

Optional

</td></tr><tr><td>

Goal adherence

</td><td>

Whether the agentic AI asset stayed within its defined scope and instructions

</td><td>

No

</td></tr></tbody>
</table>## Issue types

Issues are broken down by behavior. Each metric has its own issues identified separately.

<table><thead><tr><th>

Category

</th><th>

Agentic AI asset behavior

</th></tr></thead><tbody><tr><td>

Incomplete response

</td><td>

Response failed to address the user's full request

</td></tr><tr><td>

Factual error

</td><td>

Response contained content that isn't factually correct

</td></tr><tr><td>

Hallucination

</td><td>

Response contained content not grounded in the specific context of the request

</td></tr><tr><td>

Incoherent output

</td><td>

Response was disorganized or difficult to understand

</td></tr><tr><td>

Incorrect tool use

</td><td>

Selected the wrong tool or passed incorrect parameters to a tool

</td></tr><tr><td>

Scope violation

</td><td>

Responded to a request outside its defined operating scope

</td></tr></tbody>
</table>## Data requirements

<table><thead><tr><th>

Requirement

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Minimum test cases

</td><td>

A minimum number of test cases is required per run. The specific metrics you are using for the run may have their own minimum test cases. Ensure that your dataset meets the requirements for all metrics.

</td></tr><tr><td>

Supported formats

</td><td>

CSV and structured JSON are supported.

</td></tr><tr><td>

Ground truth field

</td><td>

If you're using a ground truth, it must be provided as a separate field in the dataset. The ground truth field must be aligned to each test case individually.

</td></tr><tr><td>

Data representativeness

</td><td>

Datasets should reflect all of the tasks that the AI agent or agentic workflow will handle. Include edge cases and failure-prone scenarios to help ensure that you're testing against common real-world scenarios.

</td></tr></tbody>
</table>