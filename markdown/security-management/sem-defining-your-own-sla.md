---
title: Defining your own service level agreements \(SLAs\) using remediation target rules
description: Remediation target rules set the expected time frame for addressing findings, similar to how service level agreements \(SLAs\) set deadlines for fixing vulnerabilities. You can also send notifications to users and groups when target dates are approaching and when they are past due.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Automating prioritization and triaging, Security Exposure Management workflow, Explore, Unified Security Exposure Management, Security Operations]
---

# Defining your own service level agreements \(SLAs\) using remediation target rules

Remediation target rules set the expected time frame for addressing findings, similar to how service level agreements \(SLAs\) set deadlines for fixing vulnerabilities. You can also send notifications to users and groups when target dates are approaching and when they are past due.

For instance, if an asset contains Payment Card Industry \(PCI\) data, such as credit card information, the vulnerability must be resolved within 30 days, as per the PCI Data Security Standard \(PCI DSS\). You can create remediation target rules by specifying:

-   **The remediation target**: The deadline by which the vulnerability must be fixed.
-   **The reminder target**: The date when reminders should start.
-   **The reminder and notification recipients**: Who should be notified if the findings exceed the reminder or remediation target dates without being fixed.
-   **The recalculation method**: How the system updates the remediation target \(RT\) date when a vulnerable item’s risk rating changes.

Vulnerability analysts and managers can view the remediation target date in the findings form and list views, provided the findings are not in Deferred, Resolved, or Closed states. Remediation target rules are evaluated during import and re-evaluated if a finding is reopened.

In the findings list view, the remediation target dates are color-coded with dots:

-   **Green**: Findings that haven’t reached their notification date.
-   **Orange**: Findings approaching the remediation target date.
-   **Red**: Findings past the remediation target date.

A summary email is sent for each remediation target rule when one or more findings are either approaching their remediation target date or have passed it.

## Recalculation of remediation target date

Starting with Unified Security Exposure Management version 30.1.4 and Vulnerability Response version 26.4.4, administrators can configure how the system recalculates the remediation target date when a finding’s risk rating changes.

-   Under normal conditions, the system calculates the RT date as:

    **Remediation Target** = **Target from \(date\)** + **Target \(days\)**

-   When the risk rating changes, the system calculates a new RT date using the formula below. The selected recalculation method determines whether this new date replaces the existing RT date.

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

Retains the existing RT date. The recalculated date isn’t applied.

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

If the risk increases: Compares the existing RT date and the recalculated RT date and applies the earliest date. If the risk decreases: Applies Field change time + Target \(days\) without comparison.

</td></tr></tbody>
</table>For configuration steps, see [Recalculate a remediation target date](../task/sem-recalculate-rt-date.md).

## Deactivating or deleting remediation target rules

-   **Deactivating a rule**: When a rule is deactivated, the current remediation target dates for the findings it was applied to are cleared. If a finding meets the criteria of any active rule, that rule is applied; otherwise, the finding has no target date and its status is set to "No Target."
-   **Deleting a rule**: When a rule is deleted, the remediation target date and related fields on closed, deferred, or resolved findings are preserved. For non-closed findings, these fields are cleared, and any dependent rules are reapplied.

## Remediation target rule scenario

When multiple remediation target rules apply to the same findings, the most restrictive rule is used.

Remediation targets are calculated from the **Target from \(date\)**. The default value remains **Last opened date**.

For example, if a finding meets the conditions for two remediation target rules:

Scenario: Finding last opened on 03/01/2018 at 10:00:00.

-   Rule 1: Last opened on 03/07/2018; remediation target is 15 days since it was last opened; calculated remediation target date is 03/16/2018 10:00:00.
-   Rule 2: Last opened on 03/10/2018; remediation target is 10 days since it was last opened; calculated remediation target date is 03/11/2018 10:00:00.

In this scenario, Rule 2 applies to the finding because it has the more restrictive date \(10 days since the item was first identified, compared to 15 days\).

**Note:** Remediation targets are calculated from the "Last Opened" date plus the specified number of days \(measured in 24-hour increments\).

## About the Evaluate remediation targets scheduled job

**Evaluate remediation targets** job runs once daily at 4:00:00.

It processes all active rules, starting with those that have the earliest remediation target dates. The job evaluates findings that:

-   Aren't in a Closed, Deferred, or Resolved state.
-   Have no remediation target date.
-   Have a remediation target date later than the date specified in the rule.

If a finding lacks a remediation target date, the job adds one. If a rule results in an earlier date than the one in the record, the job updates the existing target date. It also updates the **Remediation target** and **Remediation status** fields in the findings form.

Once the job runs, any applicable notifications are sent. The job clears the remediation fields on the finding and stops sending notifications.

**Note:** The **sn\_sec\_cmn.evaluate\_targetmissed\_records** property, enabled by default, helps prevent the **Remediation Target Rules** scheduled job from evaluating missed findings.

## Reapplying remediation target rules

When you modify a remediation target rule, use the **Reapply** button on the Remediation target rules list page to rerun the changed rules on all active Open findings, excluding those in the Closed, Deferred, or Resolved states. Depending on the number of findings, this process may take some time.

**Note:**

-   If the **Evaluate remediation targets** job is running, you can’t initiate a reapply process. However, if a reapply process is already running and the scheduled job is triggered, they run in parallel.
-   As a vulnerability admin or analyst, you can obtain the latest remediation target date for selected findings in the Security Exposure Management Workspace. This method is more efficient than running the remediation target rules for all findings in the classic UI, which can be time-consuming. For more information, see [Re-evaluate the remediation properties of the records in the Security Exposure Management Workspace](sem-configure-remediation-target-rules.md#).

**Parent Topic:**[Automating prioritization and triaging](sem-automating-prioritization-triaging.md)

**Related topics**  


[Configuring remediation target rules](sem-configure-remediation-target-rules.md#)

