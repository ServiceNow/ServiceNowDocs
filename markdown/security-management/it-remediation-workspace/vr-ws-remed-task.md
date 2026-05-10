---
title: Use remediation task records in the IT Remediation Workspace
description: Remediation tasks are created and assigned automatically from remediation efforts. IT teams and remediation owners can view remediation tasks in the IT Remediation Workspace.
locale: en-US
release: australia
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Create a remediation task manually in the IT Remediation Workspace, Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Use remediation task records in the IT Remediation Workspace

Remediation tasks are created and assigned automatically from remediation efforts. IT teams and remediation owners can view remediation tasks in the IT Remediation Workspace.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## About this task

When vulnerability managers and analysts create remediation efforts to drive remediation, remediation tasks are created automatically and assigned to IT teams based on the group that is associated with the records in a remediation effort.

See the vulnerable CIs assigned to you and your groups that have vulnerabilities on them on the **Vulnerable CIs** tab or on the Vulnerable CIs assigned to you and your group list on the List view.

## Procedure

1.  In your ServiceNow AI Platform instance, navigate to **Vulnerability Response** &gt; **IT Remediation Workspace**.

    The Home landing page is displayed.

2.  In the Remediation Tasks section, click a remediation task to open it.

3.  Alternatively, you can click the List icon in the upper left on the home page to see all the remediation tasks \(VULs, AVULs, CVULs and CRGs\) and records \(VITs, AVITs, CVITs and TRs\) assigned to you and your groups.

    For more information about how to use the list view, see [Create a list in the IT Remediation Workspace](vr-ws-IT-list-view.md).

4.  From either the Home page or the List view, click a remediation task to open it.

    In the **Details** tab, you can update some of the information on the record, such as assignment group, state, short description, and so on. Click **Save** to apply your changes.

5.  Refer to the following table for the UI actions you can perform from the remediation task record.

<table id="choicetable_rrb_qt4_1qb"><thead><tr><th align="left" id="d308800e149">

Task

</th><th align="left" id="d308800e152">

Description

</th></tr></thead><tbody><tr><td id="d308800e158">

**Click a related items link**

</td><td>

-   Overview - View your remediation progress with % of VIs remediated, the state, Risk rating, Assignment group, affected CIs and other task details. To see the Affected CIs, see the image following the table.
-   Solutions - View both preferred and potential solutions you can use to fix the vulnerability. On the record this that is displayed, child related list items show Preferred solutions and Potential solutions. See the images below the table.
-   Details - More overview information including the associated vulnerability. You can edit these fields.
-   Change Requests - View the change requests associated with the record.
-   Requested Approvals - View the submissions for change requests. If there are no change request approval requests, this related list item is not displayed.
-   State Change Approvals - View the false positive and exception requests associated with this record. If there are no requests, this related list item is not displayed.
 Opened records remain displayed as tabs until you close them.

</td></tr><tr><td id="d308800e192">

**Click a link to open a record**

</td><td>

From list displayed on opened records from the related items links, view more details about the records, the associated vulnerabilities, affected CIs \(assets\), detection data, impacted services, and associated records.

</td></tr><tr><td id="d308800e201">

**Click a UI action**

</td><td>

-   Assign to Me - This option is only displayed if the remediation task is not already assigned to you.
-   Mark as False Positive - Submit a request if, for example, a scanner finds a vulnerability but you determine that no vulnerability exists.
-   Create Change - You can create a new change request or add this remediation task to an existing change request.
-   Split Task - Identify a subset of VIs you want to include in a new remediation task
-   Request Exception - Submit a request if a target date is passed and you know you need some more time to resolve the vulnerability.
-   Resolve - Resolve this RT. The remediation task transitions to Resolved and all its VIs transition to Resolved.
-   Save - Save any changes and update the record.


</td></tr><tr><td id="d308800e235">

**Add a work note or attach a file**

</td><td>

In the far right of the screen, click the **Activity** icon \(lightening icon\) and enter a work note. Click the icon to toggle the panel.You can also upload a file.

</td></tr><tr><td id="d308800e251">

**Set filters for a column on a list**

</td><td>

Select a column and expand the vertical three dots menu to view options that further filter the data in the column. For example, with the Overview-related item selected, you might prefer to sort the Risk rating column so that only critical items display.

</td></tr><tr><td id="d308800e263">

**Filter a column by a selected row**

</td><td>

Select a cell in a column and refine the data displayed by choosing one:-   Show Matching - display only items that match the selected cell in the column.
-   Filter Out - filter out the items from the column that match the selected cell in the column.


</td></tr></tbody>
</table>    The Solutions tab in a host remediation task shows you both Preferred and Potential solutions information that best matches the vulnerability associated with the remediation task. Solutions are patches that your IT teams apply to resolve vulnerabilities.

    If the Vulnerability Solution Management application is installed, Preferred Solutions are the highest-superseding solutions that are applied to vulnerable items. The list of solutions is based on the vulnerable items in the host remediation task.

    Potential solutions are the list of all solutions that are available for VITs in a host remediation task.

    You can view the CIs \(assets\) that are affected by this vulnerability on the remediation task by navigating to **Overview** &gt; **Affected CIs**.


