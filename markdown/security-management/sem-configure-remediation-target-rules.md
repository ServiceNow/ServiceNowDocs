---
title: Configuring remediation target rules
description: By configuring remediation target rules, you can set the expected time frame for addressing findings, similar to how service level agreements \(SLAs\) set deadlines for fixing vulnerabilities.Create remediation target rules to ensure the timely remediation of high-risk vulnerabilities by setting up a remediation target rule at the findings level.The remediation target \(RT\) date defines when a finding must be remediated. Recalculation verifies that RT dates stay accurate and reflect the latest risk rating updates. When a finding’s risk rating changes, the system can recalculate RT dates using the most recent update date, helping maintain accurate SLAs and avoid outdated or overdue target dates.The following examples show how the system recalculates the remediation target date based on different rule selections and risk rating changes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [Remediation target, Recalculate remediation target date]
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring remediation target rules

By configuring remediation target rules, you can set the expected time frame for addressing findings, similar to how service level agreements \(SLAs\) set deadlines for fixing vulnerabilities.

The base system ships with three remediation target rules that are applicable only for application vulnerable items:

-   **Critical Risk Rating Rule**: A remediation target with a 1-Critical risk rating, a remediation target of 15 days, and a reminder of 7 days before the target date.
-   **Less Critical Risk Rating Rule**: A remediation target with either a 2-High or 3-Medium risk rating a remediation target of 30 days, and a reminder of 7 days before the target date.
-   **Medium-High RIsk Rating Rule**: A remediation target with a 4-Low risk rating a remediation target of 45 days, and a reminder of 7 days before the target date.

These rules are inactive by default. If you choose to edit one, rather than create a new one, remember to check the Active box before saving.

**Parent Topic:**[Configure rules to manage findings](../task/sem-configure-rules-manage-findings.md)

**Related topics**  


[Defining your own service level agreements \(SLAs\) using remediation target rules](sem-defining-your-own-sla.md)

## Create or edit remediation target rules

Create remediation target rules to ensure the timely remediation of high-risk vulnerabilities by setting up a remediation target rule at the findings level.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](sem-acls-for-admin-rules.md)

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Remediation target rules** tile.

4.  On the Rules page, select **Remediation target** in the navigation pane.

5.  Select **New**.

6.  On the remediation target rule form, enter the required details.

    For a full description of each field, see [Remediation target rule fields](../../vulnerability-response/reference/sem-rt-rules-fields.md).

7.  Select **Save**.

    This rule goes into effect during the next run of the scheduled job, **Evaluate remediation targets** or when using the **Reapply** button on the Remediation target rules list view. The same is true when an existing rule is updated.


**Related topics**  


[Create or edit remediation target rules](sem-configure-remediation-target-rules.md#)

[Recalculate a remediation target date](sem-configure-remediation-target-rules.md#)

[Examples of recalculating a remediation target date](sem-configure-remediation-target-rules.md#)

### Recalculate a remediation target date

The remediation target \(RT\) date defines when a finding must be remediated. Recalculation verifies that RT dates stay accurate and reflect the latest risk rating updates. When a finding’s risk rating changes, the system can recalculate RT dates using the most recent update date, helping maintain accurate SLAs and avoid outdated or overdue target dates.

#### Before you begin

**Note:** By default, recalculation applies only to findings that aren’t overdue. To include overdue findings in the recalculation, enable the **sn\_sec\_cmn.evaluate\_targetmissed\_records** system property.

Role required: admin

#### About this task

Recalculate remediation target date 

#### Procedure

1.  Navigate to **Security Exposure Management** &gt; **Administration** &gt; **Remediation Target Rules**.

2.  Open an existing rule to make updates.

    If you need to create a new rule, select **New**.

    For instructions, see [Create or edit a Vulnerability Response remediation target rule](../../vulnerability-response/task/create-time-to-remediate-rule.md).

3.  Choose how the system should recalculate the remediation target \(RT\) date when the risk rating changes.

    -   In Workspace, this option appears in the Recalculate target date section
    -   In Classic view, use the **Target recalculation method** field.
<table id="choicetable_bb3_q3b_fhc"><thead><tr><th align="left" id="d407126e405">

Choice

</th><th align="left" id="d407126e408">

Description

</th></tr></thead><tbody><tr><td id="d407126e414">

**Default calculation**

</td><td>

Retains the existing RT date. The recalculated date isn’t applied.

</td></tr><tr><td id="d407126e423">

**Recalculate from risk change date**

</td><td>

Updates the Remediation Target date to: Field change time + Target \(days\) based on the new risk rating.

</td></tr><tr><td id="d407126e432">

**Recalculate from risk change date and always set to earliest target date**

</td><td>

Compares the existing RT date with Field change time + Target \(days\) and applies the earlier date.

</td></tr><tr><td id="d407126e441">

**Recalculate from risk change date and set to earliest target date only when risk rating increases**

</td><td>

If the risk increases: Compares the existing RT date and the recalculated RT date and applies the earliest date. If the risk decreases: Applies Field change time + Target \(days\) without comparison.

</td></tr></tbody>
</table>4.  Select **Save**.


#### What to do next

For more information on remediation target rules, see:

-   [Vulnerability Response remediation target rules](../../vulnerability-response/concept/time-to-remediate-rules.md)
-   [Create or edit a Vulnerability Response remediation target rule](../../vulnerability-response/task/create-time-to-remediate-rule.md)
-   [Examples of recalculating a remediation target date](sem-configure-remediation-target-rules.md#)

#### Examples of recalculating a remediation target date

The following examples show how the system recalculates the remediation target date based on different rule selections and risk rating changes.

**Note:** By default, SLAs define the remediation window for each risk level:

-   Low risk: 30 days
-   Medium risk: 15 days
-   High risk: 10 days

<table id="table_xf5_cfb_fhc"><thead><tr><th>

Target from \(date\)

</th><th>

Field change time

</th><th>

Initial risk \(Target \(days\)\) → New risk \(Target \(days\)\)

</th><th>

Existing RT date

</th><th>

Recalculated RT date

</th><th>

What happens

</th></tr></thead><tbody><tr><td colspan="6">

Default calculation

</td></tr><tr><td>

Feb 1

</td><td>

Feb 10

</td><td>

Medium \(15 days\) → High \(10 days\)

</td><td>

Feb 16 \(retained\)

</td><td>

Feb 20

</td><td>

The recalculated RT date isn’t applied. The system keeps the original RT date: Target from \(date\) + Target \(days\) → Feb 1 + 15 = Feb 16.

</td></tr><tr><td colspan="6">

Recalculate from risk change date

</td></tr><tr><td>

Feb 1

</td><td>

Feb 10

</td><td>

Medium \(15 days\) → High \(10 days\)

</td><td>

Feb 16

</td><td>

Feb 20 \(applied\)

</td><td>

Uses the recalculation formula: Field change time + Target \(days\) → Feb 10 + 10 = Feb 20.

</td></tr><tr><td colspan="6">

Recalculate from risk change date and always set to earliest target date

</td></tr><tr><td>

Feb 1

</td><td>

Feb 10

</td><td>

Medium \(15 days\) → Low \(30 days\)

</td><td>

Feb 16 \(applied\)

</td><td>

Mar 12

</td><td>

Compares the existing RT date \(Feb 16\) with the recalculated date \(Feb 10 + 30 = Mar 12\) and selects the earliest date → Feb 16.

</td></tr><tr><td colspan="6">

Recalculate from risk change date and set to earliest target date only when risk rating increases

</td></tr><tr><td>

Feb 1

</td><td>

Feb 10

</td><td>

Low \(30 days\) → High \(10 days\)

</td><td>

Mar 3

</td><td>

Feb 20 \(applied\)

</td><td>

Because the risk increased, the system compares the existing RT date \(Mar 3\) with the recalculated date \(Feb 20\) and applies the earlier date → Feb 20.

</td></tr><tr><td>

Feb 1

</td><td>

Feb 10

</td><td>

High \(10 days\) → Low \(30 days\)

</td><td>

Feb 11

</td><td>

Mar 12 \(applied\)

</td><td>

Because the risk decreased, no comparison is performed. The system sets RT date to: Field change time + Target \(days\) → Feb 10 + 30 = Mar 12.

</td></tr></tbody>
</table>