---
title: Use the List view in the Security Exposure Management Workspace
description: As a vulnerability manager, security manager and analysts, you can view remediation progress on records, drill down into findings, and view the status of their approval requests and exceptions.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use, Unified Security Exposure Management, Security Operations]
---

# Use the List view in the Security Exposure Management Workspace

As a vulnerability manager, security manager and analysts, you can view remediation progress on records, drill down into findings, and view the status of their approval requests and exceptions.

## Before you begin

Role required:

-   sn\_vul.vulnerability\_analyst, sn\_vul.vulnerability\_admin, or sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_sec\_manager, sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.vulnerability\_analyst, sn\_vul\_container.vulnerability\_admin, or sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.admin, sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management**.

2.  Select the **List** icon.

    The consolidated list of records, remediation tasks, remediation efforts, libraries are displayed. For more information on the type of lists on the List page, see [Security Exposure Management Workspace List view](../concept/sem-workspace-list-page.md).

3.  Select **My Lists** to create a list.

    For more information on how to create a list, see [Create a customized list of records](sem-create-custom-list.md).

4.  Refer to the following table for the actions that you can perform on the List page.

<table id="table_gtc_14c_nqb"><thead><tr><th>

UI action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open a remediation effort

</td><td>

With **Active** selected under the **Remediation efforts** list, select a remediation effort link to open it.

 A Remediation Effort is a set of records that are associated with a watch topic. The records listed on a remediation effort are static. They are not updated by new import data or changes that you make to watch topics.

 The related list items on the remediation effort record permit you to view overall remediation progress and status on the records associated with it. For more details and UI actions you can perform from a remediation effort, see [Use Remediation Effort records](sem-ws-remed-eff-rcd.md).

</td></tr><tr><td>

To the left of the Number column with a list displayed, roll over a row and select the small information icon **\(i\)** for a record.

</td><td>

Details about the records are displayed in the right side panel of the page. Details include:-   Assignment group
-   Vulnerability
-   Assigned to
-   Short description
-   Description
 You can edit the fields. If the Active check box is displayed, you can activate or deactivate the record. Select the **Update** to save your changes.

</td></tr><tr><td>

Refresh the list

</td><td>

With the refresh icon on the top right of the page, reload the current page.

</td></tr><tr><td>

Reset widths

</td><td>

Select the gear icon to adjust column widths on your lists. A copy of the original list is saved under **Your Lists**.

</td></tr><tr><td>

Copy the URL for the displayed page

</td><td>

Copy the URL for use elsewhere.

</td></tr><tr><td>

Export the page

</td><td>

In the modal, enter the file and delivery types and select **Export**.

</td></tr><tr><td>

Refine filters for the data on the page.

</td><td>

Select a column and expand the three vertical dots menu to view options that further filter the data in the column. For example, you might prefer to filter the Assignment group column from the active remediation tasks list by a specific assignment group.

</td></tr><tr><td>

Filter out items or match items from a row in a column

</td><td>

Select a cell in a column and refine the data displayed by choosing one:-   Show Matching - display only items that match the selected cell in the column.
-   Filter Out - Filter out the items from the column that match the selected cell in the column.


</td></tr></tbody>
</table>5.  You can create an application vulnerable item from the **Active** or **All** lists under **Application Vulnerable items** by selecting the **New** button on the upper right.


