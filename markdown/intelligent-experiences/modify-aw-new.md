---
title: Modify an agentic workflow
description: Modify an agentic workflow in AI Agent Studio to refine its performance, align with business goals, or enable it to perform new tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/modify-aw-new.html
release: australia
topic_type: task
last_updated: "2026-06-06"
reading_time_minutes: 2
breadcrumb: [Create an agentic workflow, AI Agent Studio, Enable AI experiences]
---

# Modify an agentic workflow

Modify an agentic workflow in AI Agent Studio to refine its performance, align with business goals, or enable it to perform new tasks.

## Before you begin

Role required: sn\_aia.admin

## About this task

You can make tweaks to your agentic workflow based on previous performance, refine it to better align with evolving business goals, or make major changes to enable it to perform entirely new tasks. This includes updating the workflow definition and instructions, adjusting security controls, adding or removing triggers, modifying AI agents to provide more or better capabilities, and changing where and how the agentic workflow is invoked.

The instructions field supports multiple versions within the same agentic workflow, allowing you to test different instructions and evaluate performance without losing previous versions. For more information, see [Version control for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/version-control.md).

## Procedure

1.  Navigate to the **All** &gt; **AI Agent Studio** &gt; **Agentic solutions**.

2.  Select the agentic workflow that you want to modify.

3.  In the node view, select the first node of the agentic workflow.

    The first node contains the main configuration settings for the agentic workflow. The other nodes represent the individual agents that comprise the underlying architecture.

4.  [Review or create content in the **Expected behavior** section](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-aw-new.md).

5.  [Add or modify AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-aia-aw-new.md) that work together within the agentic workflow.

6.  [Define the agentic workflow access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/define-sec-aw-new.md).

7.  [Add a trigger to automatically invoke your agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aw-new.md) if a specified event occurs.

8.  [Determine how and where users can engage with your agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/channels-access-aw-new.md).

9.  Select **Save** or **Run test** to save your changes.


## Result

Your agentic workflow is modified and ready to use.

## What to do next

You can [test your agentic workflow manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md) or [evaluate the agentic workflow using automated tests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/launch-aia-eval.md).

