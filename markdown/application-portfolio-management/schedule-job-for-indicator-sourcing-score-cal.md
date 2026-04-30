---
title: Schedule a job to compute application scores
description: Enable the Load Application Indicators and compute Application Scores scheduled job to regularly compute the application and indicator scores.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Schedule a job to compute application scores

Enable the **Load Application Indicators and compute Application Scores** scheduled job to regularly compute the application and indicator scores.

## Before you begin

Role required: admin

## About this task

The job recalculates the scores of all indicators, the scoring profiles to which these indicators are attached, and the business applications that are associated to these scoring profiles.

The job generates scores for indicators according to the time period that is set in the **Frequency** field of the Indicator form. The job generates scores on the last day of the fiscal period set as frequency. That is, if the current day is the last day of the fiscal period, only then it generates the scores.

For example, if the **Frequency** option set for the **Functional Fit** indicator is monthly, then the scores for this indicator are generated on the last day of the month. If the frequency set for the **CSAT** indicator is quarter, then the scores for CSAT are generated on the last day of that quarter. Similarly, if the frequency for **Business Value** indicator is set as year, then the scores are generated on the last day of the year.

**Note:** If your frequency is yearly, then the scores of the indicators are generated on the last day of the year. Furthermore, scores are generated for the last quarter and the last month of the year as well, which are also inclusive of the last day of the year when the scores are generated.

However, if you want to generate scores, on demand, on any day and for a particular period of time, then you can generate scores using the **Regenerate Indicator score** option in the Indicator form of a particular indicator. This action does not update the existing scores but deletes them and generates new scores. See: [Create or edit an indicator to assess an application](create-application-indicators.md). You can also use the **Regenerate scores** option of the Scoring Profile form that generates scores for all indicators attached to that scoring profile. See: [Create an application score profile and attach profile indicators](create-an-appln-score-profile.md).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  Find and select the **Load Application Indicators and compute Application Score** scheduled job.

3.  On the form, fill in the fields.

    For field information, see [Scheduled Script Execution form](../reference/scheduled-script-execution-form-2.md).

4.  Right-click the form header and click **Save**.

5.  Click **Execute Now**.

    The job executes at the scheduled date and time.


## What to do next

Understand what the job does and how the assessment framework [normalizes the application scores](../concept/application-score-profile.md).

**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/configure-apm.md)

