---
title: Create a list in the IT Remediation Workspace
description: With the List view in the IT Remediation Workspace, you can view remediation tasks and records assigned to you and your groups. You can also track your exception and false positive requests for remediation tasks \(VUL, AVUL, CVUL, and CRG\), vulnerable items \(VIT, AVIT, and CVIT\), and test results \(TRs\) and view solutions.
locale: en-US
release: yokohama
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Using the IT Remediation Workspace, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Create a list in the IT Remediation Workspace

With the List view in the IT Remediation Workspace, you can view remediation tasks and records assigned to you and your groups. You can also track your exception and false positive requests for remediation tasks \(VUL, AVUL, CVUL, and CRG\), vulnerable items \(VIT, AVIT, and CVIT\), and test results \(TRs\) and view solutions.

## Before you begin

Role required:

-   sn\_vul.remediation\_owner for host vulnerable items \(VITs\)
-   sn\_vul.app\_security\_champion for application vulnerable items \(AVITs\)
-   sn\_vul\_container.remediation\_owner for container vulnerable items \(CVITs\)
-   sn\_vulc.remediation\_owner for configuration test results \(CTRs\)

## Procedure

1.  Navigate to **All** &gt; **Vulnerability Response** &gt; **IT Remediation Workspace**.

2.  Select the List icon \(![List icon](../../secops-analyst-workspace/image/listview-icon.png)\).

    The List view displays.

    -   Click a filtered list to view the total number of active remediation tasks or records assigned to you or your group. See [Use remediation task records in the IT Remediation Workspace](vr-ws-remed-task.md) for more information about what you can do from these records.
    -   View the total number of VIs assigned to you or your groups that have solutions. Click the **Preferred solutions on VIs** card to display the list.
    -   See the vulnerable CIs assigned to you and your groups that have vulnerabilities on them on the **Vulnerable CIs** tab or on the Vulnerable CIs assigned to you and your group list on the List view.
3.  Select the **My Lists** tab.

4.  Select **Add new list**.

5.  Create the list either based on an existing list or your own setup.

<table id="choicetable_exp_nhg_jdc"><thead><tr><th align="left" id="d37290e163">

Creation type

</th><th align="left" id="d37290e166">

Actions

</th></tr></thead><tbody><tr><td id="d37290e172">

**List based on an existing list**

</td><td>

1.  Select the **Start from existing** tab.
2.  In the **List** field, select the existing list to use as a template fro the drop-down list.
3.  Provide the name for the list in the**List Name** field.


</td></tr><tr><td id="d37290e202">

**Newly created list**

</td><td>

1.  Select **Create your own**
2.  Provide the name for the list in the**List Name** field.
3.  Select the source whose data you want to filter in the list.


</td></tr></tbody>
</table>6.  Create a filtered list.

    1.  In the **Select columns** field, determine which columns will appear in the list by deleting any fields that you don't want to appear.

    2.  Provide conditions to filter the list.

        To add more than one condition, select **New condition set**.

        For example, if you wanted to create a list of active vulnerable items for a scanner you want to monitor, you might enter the conditions **\[Active\]\[is\]\[true\]** and **\[Source\]\[contains\]\[scanner-name\]**.

    3.  Select **Create**.

        Your new list is displayed.

        **Note:** If you leave the list module, the list displayed when you exit is the list you see when you return. To delete the custom lists you create, with the list displayed, on the right of the pane, select the gear icon and then select **Delete**.

7.  Refer to the following table for what you can do from the list view.

<table id="choicetable_vkx_cs4_1qb"><thead><tr><th align="left" id="d37290e299">

Task

</th><th align="left" id="d37290e302">

Description

</th></tr></thead><tbody><tr><td id="d37290e308">

**Click My Lists**

</td><td>

Create new lists and view the lists you have created. In the modal that displays, create another version of an existing list or a new one.

 The lists you create are displayed on the My List tab.

 To delete a list, with the list displayed, on the far right of the page click the gear icon.

</td></tr><tr><td id="d37290e326">

**Assign remediation task records to yourself**

</td><td>

On the Lists tab with **Assigned to my group** selected, click a remediation task record \(VUL\) to open it. On the record that displays, click **Assign to me**. This option is only available if a remediation task is not already assigned to you.

</td></tr><tr><td id="d37290e341">

**Open a remediation task \(VUL\)**

</td><td>

With a remediation task record displayed, click a related list item to open and view the following details: -   Overview - View remediation progress and other remediation task details.
-   Solutions - View both preferred and potential solutions you can use to fix the vulnerability. On the Solutions tab, child related list items show Preferred solutions and Potential solutions.
-   Details - More overview information including the associated vulnerability. You can edit these fields.
-   Change Requests - View the change requests associated with the record.
-   Requested Approvals - View the requested approvals. If there are no change request approvals, this related list item is not displayed.
-   State Change Approvals - View the false positive and exception requests associated with this record. If there are no requests, this related list item is not displayed.
 Opened records remain displayed as tabs until you close them. See [Use remediation task records in the IT Remediation Workspace](vr-ws-remed-task.md) for what you can do from the remediation task record.

</td></tr><tr><td id="d37290e385">

**Open a vulnerable item \(VIT\) record**

</td><td>

With a vulnerable item record displayed, click a related list item to open and view the following details: -   Overview - The affected asset, associated vulnerability, initial detection, and other details about the state and target date.
-   Details - More overview information including the preferred solution if available. You can edit these fields.
-   Detections - First found, last found, IP address, Port, Protocol and Proof information, if available.
-   Impacted services - Business criticality, support group and service
-   Remediation Tasks - The remediation tasks this VI is associated with.
 Opened VIT records remain displayed as tabs until you close them. See [Use remediation task records in the IT Remediation Workspace](vr-ws-remed-task.md) for what you can do from the remediation task record.

</td></tr><tr><td id="d37290e426">

**Set filters for a column on a list**

</td><td>

Select a column and expand the vertical dots menu to view options that further filter the data in the column. For example, from a list of vulnerable items selected, you might prefer to sort the Risk rating column so that only critical items are displayed.

</td></tr><tr><td id="d37290e438">

**Filter out items or match items from a row in a column**

</td><td>

Select a cell in a column and refine the data displayed by choosing one:-   Show Matching - Display only items that match the selected cell in the column.
-   Filter Out - Filter out the items from the column that match the selected cell in the column.


</td></tr><tr><td id="d37290e456">

**On the List view, to the left of the Number column with a list displayed, roll over a row and click the small information icon \(i\) for a record.**

</td><td>

Details about the records are displayed in the right side panel of the page.

</td></tr></tbody>
</table>
