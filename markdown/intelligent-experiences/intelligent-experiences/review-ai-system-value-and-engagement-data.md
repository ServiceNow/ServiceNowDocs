---
title: Review AI system value and engagement data
description: Review productivity gains, cost savings, and engagement results for AI systems. AI stewards see data for every AI system on the instance. Product owners see data for the AI systems that list them in the Managed by field.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Review AI system value and engagement data

Review productivity gains, cost savings, and engagement results for AI systems. AI stewards see data for every AI system on the instance. Product owners see data for the AI systems that list them in the Managed by field.

## Before you begin

-   You must have the AI steward role or the product owner role. Users without one of these roles can't open AI Control Tower.
-   If you have the product owner role, at least one AI system must list you in the **Managed by** field.

Role required: sn\_ai\_governance\_ai\_steward or the product owner \(sn\_ai\_governance\_ai\_asset\_owner\)

## About this task

Both roles use the same pages. The difference is the set of AI systems included in each chart.

|Role|AI systems included|
|----|-------------------|
|AI steward|All AI systems on the instance.|
|Product owner|AI systems that list the product owner in the **Managed by** field.|

For both roles, only AI systems in the Deployed state contribute to calculations. Retired AI systems and AI systems in other states are excluded.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home**.

2.  Navigate to **Insights** &gt; **Value**.

3.  Select a date range to set the reporting period.

    The change values shown against each AI system compare the selected period with the preceding period of the same length.

4.  Review the productivity gains data.

5.  To see the contributing AI systems for a chart, open the detail view.

    Because only AI systems in the Deployed state contribute, the count in the detail view can be lower than the number of AI systems in your scope.

6.  Select the **Engagement** tab to review engagement results.

7.  To review results limited to ServiceNow AI systems, open the **ServiceNow AI** tab.

8.  In the **ServiceNow AI** tab, select **Value**, **Engagement**, or **Creator skills** to view detailed information.


## Result

If you have the AI steward role, each chart shows results for every AI system on the instance.

If you have the product owner role, each chart shows results for the AI systems that you manage. If you don't manage any AI system in the Deployed state, the charts show zero values.

