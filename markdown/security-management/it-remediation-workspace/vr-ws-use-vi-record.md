---
title: Use records in the IT Remediation Workspace
description: Use records to help you view your remediation progress and the impact of vulnerable items on your assets.
locale: en-US
release: australia
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Use records in the IT Remediation Workspace

Use records to help you view your remediation progress and the impact of vulnerable items on your assets.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  In your ServiceNow AI Platform instance, navigate to **Workspaces** &gt; **IT Remediation Workspace**.

    The Home landing page is displayed.

2.  Navigate to a vulnerable item record and open it from either the Home landing page or the List view.

    The details tab includes information in the form header at the top that relates to the nature of the vulnerability, for example, `CVE-2013-5014 detected on LINUX-DAL-4331`. Under the form header, values for the State, Risk rating, Remediation target date are displayed.

3.  Refer to the following table for the UI actions you can perform on the remediation task record.

<table id="choicetable_rrb_qt4_1qb"><thead><tr><th align="left" id="d255673e110">

Task

</th><th align="left" id="d255673e113">

Description

</th></tr></thead><tbody><tr><td id="d255673e119">

**Click a Related Items link**

</td><td>

-   Overview - View details such as the state, Risk rating, Risk score, source, last found, remediation status, associated vulnerability, affected configuration item, and initial detection information.
-   Details - More overview information including the Preferred solution. You can edit these fields.
-   Detections - View detection information imported from your scanners.
-   Impacted Services - View the services impacted by the vulnerability.
-   Remediation tasks - View the other remediation tasks associated with this vulnerable item.
 Opened records from the VIT remain displayed as tabs under the record tabs until you close them.

</td></tr><tr><td id="d255673e149">

**Click a link to open a record**

</td><td>

From list displayed on opened records from the related items links, view more details about the remediation tasks, detections, and impacted services.

</td></tr><tr><td id="d255673e158">

**Click a UI action**

</td><td>

-   Assign to Me - This option is only displayed if the remediation task is not already assigned to you.
-   Mark as False Positive - Report when a scanner finds a vulnerability but you determine that no vulnerability exists. Submit a request.
-   If the vulnerable item is assigned to you, you can rescan the VI.
-   Resolve - Resolve this vulnerable item. The associated remediation tasks transition to Resolved when all its VIs are Resolved.
-   Request Exception - If a target date is passed and you know you need some more time to resolve the vulnerability, submit a request.
-   Save - Save any changes and uppdate the record.


</td></tr><tr><td id="d255673e189">

**Add a work note or attach a file**

</td><td>

In the far right of the screen, click the **Activity** icon \(lightening icon\) and enter a work note. Click the icon to toggle the panel.You can also upload a file.

</td></tr><tr><td id="d255673e205">

**Set filters for a column on a list**

</td><td>

Select a column and expand the vertical dots menu to view options that further filter the data in the column. For example, with the Detections related item selected, you might prefer to sort the column so that only detections last found from a certain date are displayed.

</td></tr><tr><td id="d255673e217">

**Filter out items or match items from a row in a column**

</td><td>

Select a cell in a column and refine the data displayed by choosing one:-   Show Matching - display only items that match the selected cell in the column.
-   Filter Out - Filter out the items from the column that match the selected cell in the column.


</td></tr></tbody>
</table>
