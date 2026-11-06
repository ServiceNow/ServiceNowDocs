---
title: Troubleshooting the Credit Dashboard
description: The AI Workflow Factory Prime Credit Dashboard doesn't populate capability data on initial install. Use the following troubleshooting guide to resolve the issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/aiwfp-credit-dashboard-troubleshooting.html
release: australia
topic_type: topic
last_updated: "2026-10-21"
reading_time_minutes: 1
breadcrumb: [Credit Dashboard, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Troubleshooting the Credit Dashboard

The AI Workflow Factory Prime Credit Dashboard doesn't populate capability data on initial install. Use the following troubleshooting guide to resolve the issue.

## Symptom

The Credit Dashboard displays an empty state on initial install of the application.

## Cause

The Credit Dashboard contains a known error in which the dashboard doesn't populate with data until specific scheduled jobs run, which sometimes occur up to 24 hours after the installation.

## Resolution

## Procedure

1.  Navigate to **System Scheduler** &gt; **Scheduled Jobs** &gt; **Scheduled Jobs**.

2.  Filter the list to display scheduled jobs related to AI Workflow Factory Prime.

    1.  Select the filter icon \[Omitted image "filter.png"\].

    2.  From the field options, select the drop-down menu and select **Name**.

    3.  In the value field, enter `AI WF`.

        \[Omitted image "aiwfp-scheduled-jobs-fix.png"\] Alt text: Filter the scheduled jobs to show only those related to AI Workflow Factory Prime.

    4.  Select **Run**.

3.  Select and hold \(or right-click\) the **AI WF Rate Card Sync** record and select **Execute Now**.

    Selecting **Execute Now** populates the capability configuration. It might take several seconds for the population to complete. Wait until the job is completed before proceeding to the next step.

4.  Select and hold \(or right-click\) the **AI WF Credit Aggregator** record and select **Execute Now**.

    Selecting **Execute Now** converts usage data into the AI Workflow Factory Prime credit model. Complete this step only after running the **AI WF Rate Card Sync** job.

5.  Return to the Credit Dashboard by navigating to **All** &gt; **AI Workflow Factory Prime Credit Dashboard** &gt; **Credit Dashboard**.

6.  Confirm that the dashboard displays correctly.


