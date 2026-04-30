---
title: Target breakdowns migration
description: As an administrator, when you run the Migrate BreakdownInterval To Checkinfrequency scheduled job, the existing values in the Review frequency and Breakdown interval fields are migrated to the Check-in frequency field in the target records.
locale: en-US
release: xanadu
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2024-10-15"
reading_time_minutes: 3
breadcrumb: [Migrate target breakdowns, Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Target breakdowns migration

As an administrator, when you run the **Migrate BreakdownInterval To Checkinfrequency** scheduled job, the existing values in the **Review frequency** and **Breakdown interval** fields are migrated to the **Check-in frequency** field in the target records.

The value in the **Actual to date** field for the target and values in the **Planned target value** and **Actual** fields for the target breakdowns are populated based on the current actual value of the target and values in the existing target breakdowns.

## Target breakdowns migration for targets with breakdown interval set to None

After running the job, the value in the **Check-in frequency** field for a target is populated based on the existing value in the **Review frequency** field of the target. If the existing value in the **Review frequency** field was set to any option other than **None**, then target breakdowns will be created for such targets based on the existing review frequency of the target. Even though **Breakdown interval** was set to **None** for a target, target breakdowns will be created for the target based on the existing review frequency of the target.

The following table describes how the check-in frequency value is populated for targets with different values in the **Review frequency** and **Breakdown interval** fields.

<table id="table_tzq_kwl_gdc"><thead><tr><th>

Review frequency \(Before upgrade\)

</th><th>

Breakdown interval \(Before upgrade\)

</th><th>

Check-in frequency \(After upgrading and running the job\)

</th></tr></thead><tbody><tr><td>

Yearly

</td><td>

None

</td><td>

Yearly

</td></tr><tr><td>

Quarterly

</td><td>

None

</td><td>

Quarterly

</td></tr><tr><td>

Monthly

</td><td>

None

</td><td>

Monthly

</td></tr><tr><td>

Fortnightly

</td><td>

None

</td><td>

FortnightlyThe Fortnightly option is retained and no target breakdowns will be created because the Fortnightly option is no longer supported.

After the owner or a contributor of the target updates the check-in frequency for the target, the target breakdowns will be created accordingly.

</td></tr><tr><td>

Weekly

</td><td>

None

</td><td>

Weekly

</td></tr><tr><td>

Daily

</td><td>

None

</td><td>

Daily

</td></tr><tr><td>

None

</td><td>

None

</td><td>

NoneIn this case, no target breakdowns will be created.

</td></tr></tbody>
</table>For example, consider a scenario where details of a target are as follows before upgrade:

-   The base value and target value of the target is 0 and 100, respectively
-   The review frequency is set to **Monthly** and Breakdown interval was set to **None**
-   The start date and end date of the target are 2024-01-01 and 2024-12-31, respectively
-   The current actual value of the target is 60 and the current month is August

In this case, after running the scheduled job 12 monthly target breakdowns are created for the target and the current actual value as 60 is populated in the August monthly breakdown. Also, the planned target value is populated for each breakdown.

## Target breakdowns migration for targets with breakdown interval set to Quarterly or Yearly

After running the job, the value in the **Check-in frequency** field for a target is populated based on the existing value in the **Review frequency** field of the target. Then, target breakdowns are created for the targets based on the existing review frequency of the target.

The following table describes how the check-in frequency value is populated for targets with different values in the **Review frequency** and **Breakdown interval** fields.

|Review frequency \(Before upgrade\)|Breakdown interval \(Before upgrade\)|Check-in frequency \(After upgrading and running the job\)|
|-----------------------------------|-------------------------------------|----------------------------------------------------------|
|Quarterly|Quarterly|Quarterly|
|Quarterly|Yearly|Quarterly|

**Note:** For targets with breakdowns interval set to Yearly, irrespective of the target is of type cumulative or non-cumulative, after running the scheduled job quarterly target breakdowns will be created and the Target value distribution is set to **Spread linearly across the time period \(cumulative\)** for the target.

For example, consider a scenario where details of a target are as follows before upgrade:

-   The base value and target value of the target is 0 and 80, respectively
-   The review frequency is set to **Quarterly** and Breakdown interval was set to **Yearly**
-   The start date and end date of the target are 2023-01-01 and 2024-12-31, respectively
-   The target is of type non-cumulative
-   The actual value achieved in each quarter is 10 starting from Q1-2023 till Q2-2024
-   The current total actual value of the target is 60 and the current quarter is Q2-2024

In this case, after running the scheduled job 8 quarterly breakdowns are created and the Target value distribution is set to **Spread linearly across the time period \(cumulative\)** for the target. The current actual value for Q1-2023, Q2-2023, Q3-2023, Q4-2023, Q1-2024, and Q2-2024 quarterly target breakdowns are populated as 10, 20, 30, 40, 50, and 60, respectively. Also, the planned target value is populated for each breakdown.

**Parent Topic:**[Migrate target breakdowns](../task/migrate-target-breakdowns.md)

