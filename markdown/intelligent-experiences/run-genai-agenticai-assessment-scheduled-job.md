---
title: Run the GenAI/AgenticAI Assessment scheduled job
description: Before you can view the agentic AI or Now Assist assessment results, you must first run the GenAI/AgenticAI Assessment scheduled job.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-09-29"
reading_time_minutes: 1
keywords: [Now Assist Readiness Evaluation, Now Assist Readiness Evaluation app, Now Assist Readiness, Now Assist assessment, GenAI assessment, AI assessment, Agentic AI assessment]
breadcrumb: [Configure, Now Assist Readiness Evaluation, Enable AI experiences]
---

# Run the GenAI/AgenticAI Assessment scheduled job

Before you can view the agentic AI or Now Assist assessment results, you must first run the GenAI/AgenticAI Assessment scheduled job.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Set the Scheduled Jobs filter to `Application is Now Assist Readiness Evaluation`, and then select **Run**.

    **Tip:** If the Application column isn’t displayed in your ServiceNow instance, personalize the column settings using the Update Personalized List icon ![](../../../reuse/icons/product-icons/gear-changes-outline-24.svg) from the list header.

3.  Select **GenAI/Agentic AI Assessment** from the Name column.

4.  Select **Execute Now**.

    This action begins the scheduled job for the agentic and generative AI assessments found in **Workspaces** &gt; **Now Assist Readiness Evaluation**.


## What to do next

If you must rerun all the scheduled jobs, or specifically, the agentic AI scheduled jobs for ITSM and CSM, repeat these steps.

**Note:** You must complete the additional steps in the Now Assist Readiness Evaluation guided setup if you want to work with the Now Assist for HRSD product. If you don’t complete the additional guided setup steps for the Now Assist for HRSD product, the assessment continuously fails. For more information about completing the Now Assist Readiness Evaluation guided setup, see [Configure the Now Assist Readiness Evaluation guided setup](configure-nare-guided-setup.md).

