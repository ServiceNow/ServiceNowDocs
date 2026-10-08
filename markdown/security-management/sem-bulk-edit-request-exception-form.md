---
title: Bulk edit form fields
description: The following table shows the fields on the Bulk Edit modal in the Security Exposure Management Workspace. The fields that appear depend on the State or Risk rating value you select.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/sem-bulk-edit-request-exception-form.html
release: brazil
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 4
breadcrumb: [Using bulk edit in the Security Exposure Management Workspace, Bulk edit in the Security Exposure Management Workspace, Use, Unified Security Exposure Management, Security Operations]
---

# Bulk edit form fields

The following table shows the fields on the Bulk Edit modal in the Security Exposure Management Workspace. The fields that appear depend on the **State** or **Risk rating** value you select.

<table id="table_t4d_4bd_5s"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td id="record-slection-field">

Record selection

</td><td>

Records to update. Choices are:-   Only Selected Items: Select this option if you want to update the records you selected using the check box.
-   All records that match filter: Select this option if you want to update the filtered records.
-   Remediation Task: Select this option if you want to update the records in a remediation task and then select the desired remediation task in the **Remediation task** field.
-   Vulnerability Entry: Select this option if you want to update the records specific to a vulnerability and then select a CVE or TPE in the **Vulnerability Entry** field.

**Note:** This field appears for host vulnerable items, application vulnerable items, and container vulnerable items.

-   Configuration test: Select this option if you want to update the test results specific to a test and then select a test in the **Configuration test** field.

**Note:** This option appears for Configuration test results only.


**Note:**

-   Records with invalid CI or CI decommissioned aren’t updated.
-   Only the records in the Open, Under Investigation, or Awaiting Implementation state are updated.

</td></tr><tr><td>

State

</td><td>

Select the Deferred state to request an exception for the selected records.

**Note:**

-   When you select this option, the Reason, Short description, Until, and Additional information fields appear.
-   When you defer records, a remediation task is created and this task is sent for approval.
-   Only findings in Open, Under investigation and awaiting implementation state can be deferred.

 Selecting a value for **State** hides the **Risk rating** field. You can change only one of **State** or **Risk rating** in a single bulk edit action.

</td></tr><tr><td>

Risk rating

</td><td>

Target risk rating for the selected vulnerable items. Leave this field set to **Select** if you don't want to change the risk rating.**Note:** Selecting a value for **Risk rating** hides the **State** field and displays the **Compensating controls** and **Modify risk until** fields.

</td></tr><tr><td>

Compensating controls

</td><td>

One or more compensating controls to associate with the risk change. Optional. This field appears only when **Risk rating** is selected. If compensating controls are associated with the vulnerability, only those controls appear. Otherwise, all active controls from the library appear.

</td></tr><tr><td>

Modify risk until

</td><td>

Date on which the modified risk rating expires. This field appears only when **Risk rating** is selected.

</td></tr><tr><td>

Preferred solution

</td><td>

Solution targeted for remediating the selected vulnerable items. For field details, see [Bulk edit host vulnerable items with patches and solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-patches-solutions.md).

</td></tr><tr><td>

Preferred patch

</td><td>

Patch targeted for remediating the selected vulnerable items. You must install Patch Orchestration to view the list of preferred patches. For field details, see [Bulk edit host vulnerable items with patches and solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-patches-solutions.md).

</td></tr><tr><td>

Unassign

</td><td>

Removes the assignment group and remediation owner from the selected items. This field appears when **State** is set to **Do Not Update**. For field details, see [Remove assignments for host vulnerable items in bulk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-unassign.md).

</td></tr><tr><td>

Assignment group

</td><td>

Assignment group to which the selected items are reassigned. All active assignment groups appear in this field. This field is deactivated when the **Unassign** check box is selected.

</td></tr><tr><td>

Reason

</td><td>

Reason for deferring records:-   Awaiting Maintenance Window
-   Fix Unavailable
-   Risk Accepted
-   Mitigating Control in Place
-   Other

**Note:** This field appears when you select the **State** as Deferred.

</td></tr><tr><td>

Short description

</td><td>

Brief note describing the reasons for deferral request. This information reflects in the **Description** field of the remediation task that is created for a deferral request.**Note:** This field appears when you select the State as Deferred and Closed-False positive.

</td></tr><tr><td>

Until

</td><td>

Date till which the record remains deferred.**Note:** This field appears when you select the State as Deferred.

</td></tr><tr><td>

Additional information

</td><td>

Any other necessary information. This information reflects in the Additional Information field in the Overview tab of the remediation task that is created for deferral and closed-false positive requests. If your deferral request is approved, this additional information appears as deferral notes for both VIT and remediation task.**Note:** This field appears when you select the **State** as Deferred and Closed-False positive.

</td></tr><tr><td>

Work notes

</td><td>

Text that you enter to describe the changes.

</td></tr></tbody>
</table>**Related topics**  


[Request bulk exception in the Security Exposure Management Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/sem-bulk-edit-request-exception.md)

