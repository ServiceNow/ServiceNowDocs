---
title: Run remediation
description: Run the appropriate remediation action to fix the non-compliant cloud configuration identified during the Cloud Configuration Governance scan run.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Remediation, Using Cloud Configuration Governance, Cloud Configuration Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Run remediation

Run the appropriate remediation action to fix the non-compliant cloud configuration identified during the Cloud Configuration Governance scan run.

## Before you begin

-   The scan run is complete
-   Role required: sn\_itom\_ccg.ccg\_operator

## Procedure

1.  Navigate to **Cloud Configuration Governance** &gt; **Scan Run**.

2.  Open the scan run during which **Cloud Configuration Governance** reported the audit issues.

3.  Select **Show audit results**.

4.  Select the violation type that you want to fix.

    Cloud Configuration Governance groups the violations per the violation type. During a remediation run, you can fix one or more violations of the same type only.

5.  Select one or more violations.

6.  Select **Remediate**.

    **Note:** You can select **Ignore for Now** to ignore the issue. When you ignore an issue, Cloud Configuration Governance doesn't report the issue as a violation and it is not represented in the dashboard reports.

7.  Review the list of resources selected for remediation.

8.  Select the remediation action.

9.  Select **OK**.


## Result

## What to do next

From the Remediation Runs related list, select the change request and review the status of the remediation. You can also view the list of all the remediation requests in the Remediation requests module.

