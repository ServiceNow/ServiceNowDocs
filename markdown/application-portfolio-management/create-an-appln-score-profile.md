---
title: Create an application score profile and attach profile indicators
description: You can create an application score profile and update the default application profile with new profile indicators per your requirements. After you create a score profile, you have to associate it with indicators.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Use, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Create an application score profile and attach profile indicators

You can create an application score profile and update the default application profile with new profile indicators per your requirements. After you create a score profile, you have to associate it with indicators.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy scoring profiles module is moved to the Enterprise Architecture Workspace. To learn more, see [Configure scoring profiles](../concept/eaw-concept/eaw-configure-scoring-profiles.md).

Role required: sn\_apm.apm\_admin

## About this task

You can create or update the scoring profile with new indicators and associate it with the business application. You can also use the same indicators within many scoring profiles, which generate indicator scores unique to that scoring profile.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Scoring Profiles**.

2.  Click **New**.

3.  On the form, fill in the fields.

    For field information, see [Scoring Profile form](../reference/scoring-profile-form.md).

4.  Right-click the form header and click **Save**.

    After creating a score profile, you must associate a profile indicator to the score profile.

5.  In the Profile Indicators related list, add indicators.

    1.  Click **New**.

    2.  On the form, fill in the fields.

<table id="table_ftq_5q2_cy"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Profile

</td><td>

Name of the application profile.

</td></tr><tr><td>

Indicator

</td><td>

Name of the application indicator.

</td></tr><tr><td>

Evaluate within Application Scoring Profile

</td><td>

Option for considering the business applications tied to the selected scoring profile in the evaluation of scores.Clearing the check box entails evaluation of all business applications within the enterprise or across all scoring profiles.

</td></tr><tr><td>

Domain

</td><td>

The domain to which this indicator belongs.

</td></tr><tr><td>

Used in CI score calculation

</td><td>

Option for using the application indicator in calculating the application score.

</td></tr><tr><td>

Weightage

</td><td>

Numeral for the indicator.Weightage provided in the application score profile for an indicator contributes to the total score of the application.

</td></tr></tbody>
</table>        An indicator that is added to the profile can be a parent indicator with dependent child indicators. When such a parent indicator is added to a scoring profile, then all its dependent child indicators are also added with weightage 0, if they are not already present in the scoring profile.

        For more information on how to create a dependent indicator, see [Create or edit an indicator to assess an application](create-application-indicators.md).

    3.  Click **Submit**.


## What to do next

**Regenerate scores**: Click the **Regenerate scores** button to regenerate the scores of all the indicators attached to the scoring profile. This action deletes the existing scores and generates new scores instead of just updating the existing scores. Therefore, the scores of all the business applications that are associated to this scoring profile are also recalculated.

You can [schedule a job to calculate application scores](schedule-job-for-indicator-sourcing-score-cal.md) periodically.

**Parent Topic:**[Using Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/using-apm.md)

