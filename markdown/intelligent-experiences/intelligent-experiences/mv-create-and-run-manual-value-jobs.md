---
title: Create and run manual value jobs
description: Set up manual value jobs for AI systems that you onboard manually, so that the AI Control Tower calculates their value on a monthly or quarterly cadence.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Create and run manual value jobs

Set up manual value jobs for AI systems that you onboard manually, so that the AI Control Tower calculates their value on a monthly or quarterly cadence.

## Before you begin

Role required:sn\_ai\_governance\_ai\_steward

## About this task

Some AI systems don't have discovery integration but still need to be managed in the AI Control Tower. For these AI systems, you onboard them manually, create manual indicators, and the value job runs according to the cadence you set.

## Procedure

1.  Onboard the AI system manually through the inventory intake form.

    Complete the intake form details, follow the asset onboarding lifecycle, and map a value template. For more information, see [Creating AI assets manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/creating-ai-assets-newexperience.md).

2.  Create the manual indicators with a monthly or quarterly cadence.

    The AI Control Tower derives the run cadence from the indicator type. A monthly indicator runs as a monthly job, and a quarterly indicator runs as a quarterly job to capture productivity gains. For more information, see .

3.  Rerun the job.

    1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**.

    2.  Navigate to **Settings** &gt; **Rules and Templates** &gt; **Templates** &gt; **Scheduled value jobs**.

    3.  Select the job that you want to rerun, and then select **Re-run**.

        You can't rerun a daily cadence system.


## Result

The AI Control Tower calculates value for the AI system on the monthly or quarterly cadence set by its indicators.

