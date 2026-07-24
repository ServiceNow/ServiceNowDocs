---
title: Configuring remediation target rules
description: By configuring remediation target rules, you can set the expected time frame for addressing findings, similar to how service level agreements \(SLAs\) set deadlines for fixing vulnerabilities.Create remediation target rules to ensure the timely remediation of high-risk vulnerabilities by setting up a remediation target rule at the findings level.The remediation target \(RT\) date defines when a finding must be remediated. Recalculation verifies that RT dates stay accurate and reflect the latest risk rating updates. When a finding’s risk rating changes, the system can recalculate RT dates using the most recent update date, helping maintain accurate SLAs and avoid outdated or overdue target dates.The following examples show how the system recalculates the remediation target date based on different rule selections and risk rating changes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-configure-remediation-target-rules.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Remediation target, Recalculate remediation target date]
breadcrumb: [Configure rules to manage findings, Implement, Unified Security Exposure Management, Security Operations]
---

# Configuring remediation target rules

By configuring remediation target rules, you can set the expected time frame for addressing findings, similar to how service level agreements \(SLAs\) set deadlines for fixing vulnerabilities.

The base system ships with three remediation target rules that are applicable only for application vulnerable items:

-   **Critical Risk Rating Rule**: A remediation target with a 1-Critical risk rating, a remediation target of 15 days, and a reminder of 7 days before the target date.
-   **Medium-High Risk Rating Rule**: A remediation target with either a 2-High or 3-Medium risk rating, a remediation target of 30 days, and a reminder of 7 days before the target date.
-   **Less Critical Risk Rating Rule**: A remediation target with a 4-Low risk rating, a remediation target of 45 days, and a reminder of 7 days before the target date.

These rules are inactive by default. If you choose to edit one, rather than create a new one, remember to check the Active box before saving. The remediation target and reminder are calculated from the date and time the finding was last opened.

## Recalculation of remediation target date

Starting with Unified Security Exposure Management version 30.0.4 and Vulnerability Response version 26.4.4, administrators can configure how the system recalculates the remediation target date when a finding’s risk rating changes.

-   Under normal conditions, the system calculates the RT date as:

    **Remediation Target** = **Target from \(date\)** + **Target \(days\)**

-   When the risk rating changes, the system calculates a new RT date using the following formula. The selected recalculation method determines whether this new date replaces the existing RT date.

    **Recalculated RT date** = **Field change time** + **Target \(days\)**

    **Field change time** captures when the risk rating changed. Target \(days\) uses SLA of new risk rating.


The following options define how the system applies the recalculated RT date when a risk rating changes:

<table id="table_ogs_hbs_3hc"><thead><tr><th>

Recalculation method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Default calculation

</td><td>

Recalculates the RT date using the standard formula \(Target from \(date\) + Target \(days\)\), based on the rule that currently matches the finding's risk rating. The Field change time-based recalculated date is not applied.

</td></tr><tr><td>

Recalculate from risk change date

</td><td>

Updates the Remediation Target date to: Field change time + Target \(days\) based on the new risk rating.

</td></tr><tr><td>

Recalculate from risk change date and always set to earliest target date

</td><td>

Compares the existing RT date with Field change time + Target \(days\) and applies the earlier date.

</td></tr><tr><td>

Recalculate from risk change date and set to earliest target date only when risk rating increases

</td><td>

If the risk increases: Compares the existing RT date and the recalculated RT date and applies the earliest date. If the risk decreases: Compares the existing RT date and the recalculated RT date and applies whichever date is later.

</td></tr></tbody>
</table>For configuration steps, see [Recalculate a remediation target date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-configure-remediation-target-rules.md).

**Parent Topic:**[Configure rules to manage findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-configure-rules-manage-findings.md)

**Related topics**  


[Defining your own service level agreements \(SLAs\) using remediation target rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-defining-your-own-sla.md)

## Create or edit remediation target rules

Create remediation target rules to ensure the timely remediation of high-risk vulnerabilities by setting up a remediation target rule at the findings level.

### Before you begin

Role required: See [Access control lists \(ACLs\) for administration rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-acls-for-admin-rules.md)

### Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Remediation target rules** tile.

4.  On the Rules page, select **Remediation target** in the navigation pane.

5.  Select **New**.

6.  On the remediation target rule form, enter the required details.

    For a full description of each field, see [Remediation target rule fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/sem-rt-rules-fields.md).

7.  Select **Save**.

    This rule goes into effect during the next run of the scheduled job, **Evaluate remediation targets** or when using the **Reapply** button on the Remediation target rules list view. The same is true when an existing rule is updated.


**Related topics**  


[Create or edit remediation target rules]()

[Recalculate a remediation target date]()

[Examples of recalculating a remediation target date]()

### Recalculate a remediation target date

The remediation target \(RT\) date defines when a finding must be remediated. Recalculation verifies that RT dates stay accurate and reflect the latest risk rating updates. When a finding’s risk rating changes, the system can recalculate RT dates using the most recent update date, helping maintain accurate SLAs and avoid outdated or overdue target dates.

#### Before you begin

**Note:** By default, recalculation applies only to findings that aren’t overdue. To include overdue findings in the recalculation, enable the **sn\_sec\_cmn.evaluate\_targetmissed\_records** system property.

Role required: admin

#### About this task

\[Omitted video\] Description: Recalculate remediation target date

#### Procedure

1.  Navigate to **Security Exposure Management** &gt; **Administration** &gt; **Remediation Target Rules**.

2.  Open an existing rule to make updates.

    If you need to create a new rule, select **New**.

    For instructions, see [Create or edit a Vulnerability Response remediation target rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/create-time-to-remediate-rule.md).

3.  Choose how the system should recalculate the remediation target \(RT\) date when the risk rating changes.

    -   In Workspace, this option appears in the Recalculate target date section
    -   In Classic view, use the **Target recalculation method** field.
<table id="choicetable_bb3_q3b_fhc"><thead><tr><th align="left" id="d426491e512">

Choice

</th><th align="left" id="d426491e515">

Description

</th></tr></thead><tbody><tr><td id="d426491e521">

**Default calculation**

</td><td>

Recalculates the RT date using the standard formula \(Target from \(date\) + Target \(days\)\), based on the rule that currently matches the finding's risk rating. The Field change time-based recalculated date is not applied.

</td></tr><tr><td id="d426491e532">

**Recalculate from risk change date**

</td><td>

Updates the Remediation Target date to: Field change time + Target \(days\) based on the new risk rating.

</td></tr><tr><td id="d426491e541">

**Recalculate from risk change date and always set to earliest target date**

</td><td>

Compares the existing RT date with Field change time + Target \(days\) and applies the earlier date.

</td></tr><tr><td id="d426491e550">

**Recalculate from risk change date and set to earliest target date only when risk rating increases**

</td><td>

If the risk increases: Compares the existing RT date and the recalculated RT date and applies the earliest date. If the risk decreases: Compares the existing RT date and the recalculated RT date and applies whichever date is farther out \(later\).

</td></tr></tbody>
</table>4.  Select **Save**.


#### What to do next

For more information on remediation target rules, see:

-   [Vulnerability Response remediation target rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/time-to-remediate-rules.md)
-   [Create or edit a Vulnerability Response remediation target rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/create-time-to-remediate-rule.md)
-   [Examples of recalculating a remediation target date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/sem-configure-remediation-target-rules.md)

#### Examples of recalculating a remediation target date

The following examples show how the system recalculates the remediation target date based on different rule selections and risk rating changes.

**Note:** By default, SLAs define the remediation window for each risk level:

-   Low risk: 30 days
-   Medium risk: 15 days
-   High risk: 10 days

|Target from \(date\)|Field change time|Initial risk \(Target \(days\)\) → New risk \(Target \(days\)\)|Existing RT date|Recalculated RT date|What happens|
|--------------------|-----------------|---------------------------------------------------------------|----------------|--------------------|------------|
|Default calculation|
|Feb 1|Feb 10|Medium \(15 days\) → High \(10 days\)|Feb 16|Feb 11 \(applied\)|Uses the standard formula with the new risk ratings target days, not the Field change time-based formula: Target from \(date\) + New risk Target \(days\) → Feb 1 + 10 = Feb 11.|
|Recalculate from risk change date|
|Feb 1|Feb 10|Medium \(15 days\) → High \(10 days\)|Feb 16|Feb 20 \(applied\)|Uses the recalculation formula: Field change time + Target \(days\) → Feb 10 + 10 = Feb 20.|
|Recalculate from risk change date and always set to earliest target date|
|Feb 1|Feb 10|Medium \(15 days\) → Low \(30 days\)|Feb 16 \(applied\)|Mar 12|Compares the existing RT date \(Feb 16\) with the recalculated date \(Feb 10 + 30 = Mar 12\) and selects the earliest date → Feb 16.|
|Recalculate from risk change date and set to earliest target date only when risk rating increases|
|Feb 1|Feb 10|Low \(30 days\) → High \(10 days\)|Mar 3|Feb 20 \(applied\)|Because the risk increased, the system compares the existing RT date \(Mar 3\) with the recalculated date \(Feb 20\) and applies the earlier date → Feb 20.|
|Feb 1|Feb 10|High \(10 days\) → Low \(30 days\)|Feb 11|Mar 12 \(applied\)|Because the risk decreased, the system compares the existing RT date \(Feb 11\) with the recalculated date \(Feb 10 + 30 = Mar 12\) and applies the later date → Mar 12.|

