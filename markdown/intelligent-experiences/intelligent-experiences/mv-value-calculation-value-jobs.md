---
title: Value calculation and value jobs
description: Value jobs calculate the productivity value of your AI systems on a schedule. Automated jobs run each night, and manual jobs run monthly or quarterly for AI systems that you onboard manually.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Value calculation and value jobs

Value jobs calculate the productivity value of your AI systems on a schedule. Automated jobs run each night, and manual jobs run monthly or quarterly for AI systems that you onboard manually.

## Value jobs overview

A value job reads the usage recorded for your AI systems and calculates the productivity value from the mapped value template. The AI Control Tower \(AICT\) runs value jobs on a schedule and calculates value for the previous day. As a result, the Value dashboard shows the value from the previous day.

Value calculation uses Performance Analytics \(PA\) indicators. An out-of-the-box daily PA indicator job calculates the usage scores for the previous day. Any custom indicator you use for value calculation must also be daily. It must complete its run before 1:00 PM each day so the value job can use its scores.

## Key benefits

Value jobs provide the following benefits:

-   Calculate value automatically each night for integrated AI systems.
-   Run manual jobs on a monthly or quarterly cadence to match how you collect data.
-   Show failed manual jobs with the reason for the failure so that you can rerun them.

## Automated and manual value jobs

The AI Control Tower runs two kinds of value jobs:

-   **Automated value job:** Runs each night for ServiceNow AI systems and for third-party AI systems that use a usage integration. The job fetches the usage for the previous day and calculates value.
-   **Manual value job:** Runs for AI systems that you onboard manually through the inventory intake form and that do not have a usage integration. You create manual indicators, and the job runs on the cadence set by those indicators.

For manual value jobs, the AI Control Tower derives the cadence from the indicator type. A monthly indicator runs as a monthly job, and a quarterly indicator runs as a quarterly job.

## Failed value jobs

Automated daily jobs run without manual intervention and retry automatically if a run does not complete. You can't rerun a daily job manually. You can rerun a monthly or quarterly job that fails, for example after a timeout or when a server is unavailable. The manual value jobs list filters to failed transactions by default and shows a comment that describes why each job failed.

## Considerations

-   A value job requires an active user. If that user is inactive, value calculation stops until you assign an active user.
-   Both value and cost are calculated for the previous day, so configuration changes appear on the dashboard after the next scheduled run.

