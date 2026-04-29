---
title: Use Remediation Effort records
description: When Vulnerability managers and analysts create remediation efforts \(REs\), remediation Tasks \(VUL\) are automatically assigned to IT teams for remediation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Use Remediation Effort records

When Vulnerability managers and analysts create remediation efforts \(REs\), remediation Tasks \(VUL\) are automatically assigned to IT teams for remediation.

## Before you begin

You have to create a remediation effort before you can use it to monitor remediation progress on Remediation Tasks.

Role required: sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, sn\_vul\_container.vulnerability\_analyst, sn\_vul.app\_sec\_manager, sn\_vul\_container.vulnerability\_admin, or sn\_vulc.admin

## Procedure

1.  If not selected, in the upper left, click the List icon.

    The List view with active Remediation Effort records is displayed.

2.  From the List view landing page, with Active Remediation Efforts selected in the filtered lists, click a record to open it.

    The record displays. You can view the remediation tasks and records that are associated with the selected remediation effort.

3.  Refer to the following table for the actions that you can perform on the remediation effort record.

    After you create a record, it may take a few minutes for the remediation tasks and large numbers of records to display.

<table id="table_u43_ssc_nqb"><thead><tr><th>

UI action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add a tag

</td><td>

To the right of the header, click the small tag icon. You might want to add text that further helps you identify this record. For example, you might want to add a tag that this record has PCI or other critical data.

</td></tr><tr><td>

Add a work note to the record

</td><td>

In the far right of the screen, click the **Activity** icon \(lightening icon\) and enter a work note. Click the icon to toggle the panel.

</td></tr><tr><td>

Update the record

</td><td>

On the **Details** tab, for all fields that are editable, click a field to select it, make your changes, and click **Save** to update the record.

</td></tr><tr><td>

When displayed, click the filter icon to refine the data on the displayed page

</td><td>

With the **Remediation Tasks** or **Vulnerable Items** tabs selected, On the far right, click the filter icon to show the filters that apply to the tab.In the panel that is displayed, click **Advanced view** to add or change filter conditions for the items on the page. Click **Update** to save your changes.

 For example, on the **Vulnerable Items** tab, you might prefer to add the Age field and enter a range to display only records from a specific time period. Records that match the conditions that you set are displayed in the list.

</td></tr><tr><td>

Refine filters for items in a column

</td><td>

Select a column and click the three vertical dots menu expand it and enter conditions to refine and group the data in the column.

</td></tr><tr><td>

Filter out items or match items from a row in a column

</td><td>

Say, for example, you want to view only records that have a specific vulnerability. From the list of records, select the row of the record in the **Summary** column. Click the vertical dot menu that is displayed and choose one:

-   **Show matching** - show all the other records that have this vulnerability.
-   **Filter out** - show all records that don’t have this vulnerability.


</td></tr><tr><td>

Activate/deactivate a record

</td><td>

If you mark a remediation effort inactive \(**Active** check box not selected\) prior to fixing all its records, any remaining, active records on the record will be moved to a new remediation effort when you create one for this watch topic.

</td></tr></tbody>
</table>4.  From the Remediation Tasks and Vulnerable Items tabs, you can drill down into an individual Remediation Task \(VUL\) and Vulnerable item \(VIT\) records.


## What to do next

If you want to create a remediation task on-demand from a remediation effort, see [Create a remediation task on-demand from Remediation Effort in the Vulnerability Manager Workspace](sem-create-rt-frm-re.md).

-   **[Create a remediation effort in the Security Exposure Management Workspace](sem-create-rev16.md)**  
A remediation effort record is a static list of records that you create from a watch topic in the Security Exposure Management Workspace.
-   **[Create a remediation task on-demand from Remediation Effort in the Vulnerability Manager Workspace](sem-create-rt-frm-re.md)**  
Create a remediation task on-demand from a remediation effort. If you create a remediation task on-demand, you choose the records you want to add manually.
-   **[Create a recurring remediation effort in the Security Exposure Management Workspace](sem-create-recurringRE-steal-VI.md)**  
You can create and schedule recurring remediation efforts that are generated automatically on the dates and times that you set.
-   **[Transfer records to remediation efforts in the Security Exposure Management Workspace](sem-transfer-VI-to-RE.md)**  
You can transfer records from existing remediation efforts into new remediation efforts in the Vulnerability Manager Workspace.

**Parent Topic:**[Using Unified Security Exposure Management](../concept/using-unified-security-exposure-management.md)

