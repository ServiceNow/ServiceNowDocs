---
title: Run individual assessment scheduled jobs
description: Use individual scheduled jobs to assess readiness for Now Assist and agentic AI implementations across your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-readiness-evaluation/run-genai-idividual-assessment-scheduled-job.html
release: australia
product: Now Assist Readiness Evaluation
classification: now-assist-readiness-evaluation
topic_type: task
last_updated: "2026-07-09"
reading_time_minutes: 1
keywords: [Now Assist, agentic AI, readiness evaluation, assessment, scheduled jobs]
breadcrumb: [Configure, Now Assist Readiness Evaluation, Enable AI experiences]
---

# Run individual assessment scheduled jobs

Use individual scheduled jobs to assess readiness for Now Assist and agentic AI implementations across your instance.

## Before you begin

Role required: admin

## About this task

The Now Assist application provides scheduled jobs that assess your instance readiness for Now Assist and agentic AI. The following individual scheduled jobs are available:

-   Now Assist Assessment - Virtual Agent
-   Now Assist Assessment - ITSM
-   Now Assist Assessment - HRSD
-   Now Assist Assessment - CSM
-   Now Assist Assessment - AI Search
-   AgenticAIHRSDAssessment
-   AgenticAICSMAssessment
-   agentic AI Assessment - ITSM - Change Request

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Filter the list by setting **Application** to `Now Assist Readiness Evaluation`.

3.  Select the job that you want to run.

4.  Select **Execute Now**.


## What to do next

**Important:**

For the Virtual Agent assessment to yield results, the following plugins must be active on your instance:

-   Virtual Agent \(com.glide.cs.chatbot\)
-   Catalog Conversational Coverage \(sn\_catalog\_con\_cov\)

Now Assist Readiness Evaluation's Virtual Agent assessment requires the Catalog Conversational Coverage \(sn\_catalog\_con\_cov\) plugin required for the assessment to run. For more information on Now Assist in Conversational Catalog Request, see [Now Assist in Conversational Catalog Request](https://www.servicenow.com/docs/r/servicenow-platform/service-catalog/now-assist-in-conversational-catalog-request).

