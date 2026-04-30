---
title: Holiday schedules in a release
description: You can associate a holiday schedule with a release so that the phase and release durations are calculated considering non-working days.
locale: en-US
release: xanadu
product: Digital Product Release
classification: digital-product-release
topic_type: concept
last_updated: "2025-02-18"
reading_time_minutes: 6
breadcrumb: [Exploring Digital Product Release, Digital Product Release, IT Service Management]
---

# Holiday schedules in a release

You can associate a holiday schedule with a release so that the phase and release durations are calculated considering non-working days.

The following example of a release shows how holiday schedules affect its overall timeline to keep important dates on working days.

Let's say a release has four phases: Planning, Development, Testing, and Implementation, with durations of 10, 25, 15, and 10 days, respectively, totaling 60 working days. The release readiness target date is set to Sep 5, 2025, and has a public and weekend holiday schedule \(U.S. Federal + Weekend holidays in 2025\) associated. So, the start and end dates of each phase are adjusted to account for non-working days \(holidays and weekends on the schedule\), to keep the phase durations intact. Key dates also follow the same adjustment rule.

-   **Considerations:**

    -   Total release duration: 60 working days
    -   Phases and durations: Planning: 10 days; Development: 25 days; Testing: 15 days; Implementation: 10 days
    -   Release readiness target date: Sep 5, 2025
    -   Working days in a week: Mon through Fri \(5 days\)
    -   Non-working days on the associated schedule:
        1.  Weekends are non-working days so skipped.
        2.  Federal holidays in 2025, relevant to the release period are as follows:
            -   Jun 19: Juneteenth \(Thu\).
            -   Jul 4: Independence Day \(Fri\).
            -   Sep 1: Labour Day \(Mon\).
    -   Adjustment rules:
        -   The original end date of the last phase is the release readiness target date, usually a working day so no adjustment needed. All remaining phases prior to the last phase get their original end and start dates by counting all calendar days, including both working and non-working. Their adjusted end and start dates are the actual dates on a working day, skipping non-working days.
        -   The original start date is determined by counting all calendar days backward from the adjusted end date. The adjusted start date is the actual start date on a working day, skipping non-working days.
        -   If a key date or the phase start or end date falls on a holiday or weekend, shift to the previous working day.
        -   The duration of each phase \(in days\) remains fixed, but holidays and weekends within the phase period extend the calendar span.
    With these considerations, let's calculate the working days in the release timeline and adjust the phase and release duration accordingly.

-   **Calculation of release dates with holiday adjustments**

<table id="table_ssc_k2w_m2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Phase

</td><td>

Phase 4: Implementation

</td></tr><tr><td>

Original end date

</td><td>

Sep 5 \(Fri\)\(Same as the release readiness target date\)

</td></tr><tr><td>

Adjusted end date

</td><td>

Sep 5 \(Fri\)\(A working day, no adjustment needed\)

</td></tr><tr><td>

Original start date

</td><td>

Aug 27 \(Wed\)\(10 days counted backward from the phase's adjusted end date, includes weekends and holidays\)

</td></tr><tr><td>

Adjusted start date

</td><td>

Aug 22 \(Fri\)\(excludes weekends and holidays, see the End date calculation\)

</td></tr><tr><td>

Key dates

</td><td>

Deployment preparation: On 5th day from the phase's adjusted start – Aug 28 \(Thu\)\(Excludes weekends and holidays. Falls on a working day, no adjustment needed\)

</td></tr><tr><td>

Original duration

</td><td>

10 daysAug 27 \(Wed\) – Sep 5 \(Fri\)

</td></tr><tr><td>

Adjusted duration

</td><td>

15 calendar days \(10 working days + 5 non-working days\)Aug 22 \(Fri\) – Sep 5 \(Fri\)

</td></tr><tr><td>

End date calculation

</td><td>

Working days: 10-   Sep 5–2 \(Fri-Tue\): 4 days.
-   Aug 29–25 \(Fri-Mon\): 5 days \(total 9 days\).
-   Aug 22 \(Fri\): 1 day \(total 10 days\).
Non-working days: 5

-   1 holiday skipped: Sep 1 \(Labor day\)
-   2 weekends skipped: Aug 30-31; Aug 23-24


</td></tr></tbody>
</table><table id="table_bdf_wnv_m2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Phase

</td><td>

Phase 3: Testing

</td></tr><tr><td>

Original end date

</td><td>

Aug 21 \(Thu\)\(The day before the Phase 4 start date\)

</td></tr><tr><td>

Adjusted end date

</td><td>

Aug 21 \(Thu\)\(A working day, no adjustment needed\)

</td></tr><tr><td>

Original start date

</td><td>

Aug 7 \(Thu\)\(15 days counted backward from the phase's adjusted end date, includes weekends and holidays\)

</td></tr><tr><td>

Adjusted start date

</td><td>

Aug 1 \(Fri\)\(Excludes weekends and holidays, see the End date calculation\)

</td></tr><tr><td>

Key dates

</td><td>

Test plan approval: On 5th day from the phase's adjusted start – Aug 7 \(Tue\)\(Excludes weekends and holidays. A working day, no adjustment needed\)

</td></tr><tr><td>

Original duration

</td><td>

15 daysAug 7 \(Thu\) – Aug 21 \(Thu\)

</td></tr><tr><td>

Adjusted duration

</td><td>

21 calendar days \(15 working days + 6 non-working days\)Aug 1 \(Fri\) – Aug 21 \(Thu\)

</td></tr><tr><td>

End date calculation

</td><td>

Working days: 20-   Aug 21-18 \(Thu-Mon\): 4 days.
-   Aug 15–11 \(Fri-Mon\): 5 days \(total 9 days\).
-   Aug 8-Aug 4 \(Fri-Mon\): 5 days \(total 14 days\).
-   Aug 1 \(Fri\): 1 day \(total 15 days\).
Non-working days: 6

-   0 holiday skipped
-   3 weekends skipped: Aug 16–17; Aug 9–10; Aug 2–3


</td></tr></tbody>
</table><table id="table_pwk_1gv_m2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Phase

</td><td>

Phase 2: Development

</td></tr><tr><td>

Original end date

</td><td>

Jul 31 \(Thu\)\(The day before the Phase 3 start date\)

</td></tr><tr><td>

Adjusted end date

</td><td>

Jul 31 \(Thu\)\(a working day, no adjustment needed.\)

</td></tr><tr><td>

Original start date

</td><td>

Jul 7 \(Mon\)\(25 days from the phase's adjusted end date, includes weekends and holidays\)

</td></tr><tr><td>

Adjusted start date

</td><td>

Jun 26 \(Thu\)\(excludes weekends and holidays, see the End date calculation\)

</td></tr><tr><td>

Key dates

</td><td>

Sprint end: Every 10 working days from the phase's adjusted start – Jul 10 \(Thu\), Jul 24 \(Thu\)\(all working days, no adjustment needed\)

</td></tr><tr><td>

Original duration

</td><td>

25 daysJul 7 \(Mon\) – Jul 31 \(Thu\)

</td></tr><tr><td>

Adjusted duration

</td><td>

36 days \(25 working days + 11 non-working days\)Jun 26 \(Thu\) – Jul 31 \(Thu\)

</td></tr><tr><td>

End date calculation

</td><td>

Working days: 25-   Jul 31-28 \(Thu-Mon\): 4 days.
-   Jul 25–21 \(Fri-Mon\): 5 days \(total 9 days\).
-   Jul 18–14 \(Fri-Mon\): 5 days \(total 14 days\).
-   Jul 11-7 \(Fri-Mon\): 5 days \(total 19 days\).
-   Jul 3-Jun 30 \(Fri-Mon\): 4 days \(total 23 days\).
-   Jun 27-26 \(Fri-Thu\): 2 days \(total 25 days\).
Non-working days: 11

-   1 holiday skipped: Jul 4 \(Independence Day\)
-   5 weekends skipped: Jul 26-27; Jul 19-20; Jul 12-13; Jul 5-6; Jun 28-29


</td></tr></tbody>
</table><table id="table_b2k_l33_m2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Phase

</td><td>

Phase 1: Planning

</td></tr><tr><td>

Original end date

</td><td>

Jun 25 \(Wed\)\(The day before the Phase 2 start date\)

</td></tr><tr><td>

Adjusted end date

</td><td>

Jun 25 \(Wed\)\(a working day, no adjustment needed\)

</td></tr><tr><td>

Original start date

</td><td>

Jun 16 \(Mon\)\(10 days from the phase's adjusted end date, includes weekends and holidays\)

</td></tr><tr><td>

Adjusted start date

</td><td>

Jun 11 \(Wed\)\(excludes weekends and holidays, see the End date calculation\)

</td></tr><tr><td>

Key dates

</td><td>

Midpoint: On 5th working day from the phase's adjusted start – Jun 17 \(Tue\)\(a working day, no adjustment needed\)

</td></tr><tr><td>

Original duration

</td><td>

10 daysJun 16 \(Wed\) – Jun 25 \(Wed\)

</td></tr><tr><td>

Adjusted duration

</td><td>

15 days \(10 working days + 5 non-working days\)Jun 11 \(Wed\) – Jun 25 \(Wed\)

</td></tr><tr><td>

End date calculation

</td><td>

Working days: 10-   Jun 25–23 \(Wed–Mon\): 3 days.
-   Jun 20 \(Fri\): 1 day \(total 4 days\).
-   Jun 18–16 \(Wed-Mon\): 3 days \(total 7 days\).
-   Jun 13–11 \(Fri-Wed\): 3 days \(total 10 days\).
Non-working days: 5

-   1 holiday skipped: Jun 19 \(Juneteenth\)
-   2 weekends skipped: Jun 21-22; Jun 14-15


</td></tr></tbody>
</table>-   **Summary Timeline**

    The timeline extends beyond the 70-days original duration to account for weekends and associated holiday schedule, but the phase durations remain fixed in working days.

<table id="table_lgy_1lw_m2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Original calendar span

</td><td>

Jul 8 to Sep 5![Calendar view of a release timeline without considering any holidays and weekends.](../image/dpr-schedule-in-release-without.png)

</td></tr><tr><td>

Adjusted span, excluding non-working days

</td><td>

Jun 11 to Sep 5 ![Calendar view of a release timeline considering associated holiday schedule and weekends.](../image/dpr-schedule-in-release-with.png)

</td></tr><tr><td>

Original release duration

</td><td>

60 working days

</td></tr><tr><td>

Adjusted release duration

</td><td>

87 calendar days

</td></tr><tr><td>

Non-Working Days

</td><td>

87 – 60 = 27 days \(12 weekends + 3 holidays\)

</td></tr></tbody>
</table>
**Parent Topic:**[Exploring Digital Product Release](dpr-exploring-digital-product-release.md)

