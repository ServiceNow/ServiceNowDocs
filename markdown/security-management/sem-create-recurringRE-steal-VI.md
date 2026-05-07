---
title: Create a recurring remediation effort in the Security Exposure Management Workspace
description: You can create and schedule recurring remediation efforts that are generated automatically on the dates and times that you set.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use Remediation Effort records, Use, Unified Security Exposure Management, Security Operations]
---

# Create a recurring remediation effort in the Security Exposure Management Workspace

You can create and schedule recurring remediation efforts that are generated automatically on the dates and times that you set.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, or sn\_vul.vulnerability\_admin for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst or sn\_vul\_container.vulnerability\_admin for container vulnerable items \(CVITs\)
-   sn\_vulc.admin for configuration test results \(CTRs\)

## About this task

You can automatically create recurring remediation efforts on a schedule that helps you track vulnerabilities that might come up and require immediate and ongoing attention.

Starting with version 18.0, because you can’t create a recurring remediation effort for an inactive watch topic, the **Create Recurring Effort** option is inactive. If you deactivate a watch topic that has a recurring effort already scheduled, then a new remediation effort is not created until the watch topic is activated. Also, the **Effort recurrence** and **Next recurrence date** details disappear on the upper right. After you activate the watch topic, a remediation effort is created at the upcoming schedule.

## Procedure

1.  Navigate to **All** &gt; **Vulnerability Response** &gt; **Vulnerability Manager Workspace** &gt; **Watch Topics**.

2.  On the Watch Topics page, select a watch topic that you want to create a recurring remediation effort for.

    You can create one recurring remediation effort per watch topic.

    **Note:** You cannot transfer records from recurring remediation efforts into new remediation efforts. However, you can transfer records from existing, non-recurring remediation efforts into new remediation efforts. See [Transfer records to remediation efforts in the Vulnerability Manager Workspace](../../vulnerability-response/task/vr-ws-transfer-VI-to-RE.md) for more information about transferring records.

3.  On a watch topic, on the upper right from the Create Remediation Effort list, select **Create Recurring Effort**.

    The Create Recurring Effort modal is displayed.

4.  In step 1, Effort details, fill in the required fields.

    In the Short description field, enter the text that describes the recurring remediation effort that helps you locate it and track it from the effort list.

    In the Description field, enter more text about the context of the effort that helps you locate it easily from the list of remediation efforts. For example, `Vulnerabilities on External Facing Assets`.

5.  Click **Next**.

    Task generation details are displayed.

6.  In step 2, Task generation, choose one method from the list to bundle the vulnerable items in the remediation tasks that you generate from this remediation effort after it is created.

    -   By Assignment group
    -   By Assignment group and configuration item
    -   By Assignment group and vulnerability
    -   None \(No remediation tasks are created\). Use this method if you want to add records manually to a remediation task for this effort. See [Create a remediation task on-demand from Remediation Effort in the Vulnerability Manager Workspace](../../vulnerability-response/task/vr-ws-create-rt-frm-re.md).
7.  To automatically refresh the duplicate host vulnerable items, you must select the **Automatically refresh duplicate vulnerable items for the created remediation tasks** option.

    **Note:** This check box is available only for Host Vulnerabilities.

8.  Click **Next** to continue.

9.  In step 3, Recurrence, select the frequency.

<table id="choicetable_q1j_wyh_yxb"><thead><tr><th align="left" id="d439505e242">

Option

</th><th align="left" id="d439505e245">

Description

</th></tr></thead><tbody><tr><td id="d439505e251">

**Quarterly \(Every 3 months\)**

</td><td>

Schedules Remediation Effort once in every three month.**Note:**

If the month you select has only 30 days, the remediation effort is created on that last date of the month.

</td></tr><tr><td id="d439505e265">

**Monthly**

</td><td>

Schedules Remediation Effort once in every month.

</td></tr><tr><td id="d439505e274">

**Weekly**

</td><td>

Schedules Remediation Effort once in every week.**Note:** This option is available starting from the version 19.0 of Vulnerability Response.

</td></tr><tr><td id="d439505e288">

**Daily**

</td><td>

Schedules Remediation Effort everyday.**Note:** This option is available starting from the version 19.0 of Vulnerability Response.

</td></tr></tbody>
</table>    1.  Define the recurrence schedule.

        Use the lists to select the month/day/hour/minute you want the remediation effort created. The time zone for scheduling is by default your time zone.

        **Note:** If you have many vulnerabilities, you might prefer to set the creation for off-hours.

        If you want the job created on the last day of the month, the scheduled job creates the recurring remediation effort on the last day of the month. A message displays if the month does not have 31 days.

    2.  Select **Carry over vulnerabilities** to active vulnerabilities in this remediation effort to carry forward into each subsequent remediation effort that is created.

10. Click **Schedule recurrence**.

    A message is displayed that the recurring remediation record was created. The new remediation effort is not displayed immediately, it is created when you scheduled it. It is displayed on your lists after it is created by the scheduled job.

    The date the remediation effort will be created is shown on the corresponding watch topic. For more information on how the Remediation Tasks associated with the Remediation Efforts are impacted by records transfer, see [Life cycles of remediation efforts, remediation tasks, and records in the Vulnerability Response Workspaces](../../vulnerability-response/concept/vr-ws-re-lifecycle.md).


**Parent Topic:**[Use Remediation Effort records](sem-ws-remed-eff-rcd.md)

