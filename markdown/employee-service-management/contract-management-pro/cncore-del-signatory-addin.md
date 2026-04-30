---
title: Edit or delete participants using add-in
description: As a contract configurator, edit or delete a participant from a Microsoft Word document using the Microsoft Word add-in for ServiceNow Contracts.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Edit a contract template using Microsoft Word add-in for ServiceNow Contracts, Manage clauses, tables, and contract templates, Manage Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Edit or delete participants using add-in

As a contract configurator, edit or delete a participant from a Microsoft Word document using the Microsoft Word add-in for ServiceNow Contracts.

## Before you begin

A Microsoft Word document with content controls should have been uploaded into the contract template.

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open the Microsoft Word document with content controls.

2.  From the Microsoft Word ribbon, select ServiceNow Contracts add-in.

3.  On the add-in login screen, enter the credentials of the ServiceNow instance from where you downloaded the manifest file.

    For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](../task/cncore-config-word-addin.md)

4.  In the **Template** tab, select the contract template.

5.  Navigate to the **Signatory** tab.

6.  Select the Edit or delete signatory icon \(![Edit or delete signatory icon](../image/lsd-three-dots-icon.png)\).

7.  Edit or delete the signatory.

<table id="choicetable_phr_kxb_gzb"><thead><tr><th align="left" id="d550292e142">

Action

</th><th align="left" id="d550292e145">

Steps

</th></tr></thead><tbody><tr><td id="d550292e151">

**Edit the signatory**

</td><td>

1.  Select **Edit signatory**.
2.  Modify the signatory details.
3.  Select **Save**.


</td></tr><tr><td id="d550292e178">

**Delete the signatory**

</td><td>

1.  Select **Delete signatory**.
2.  Select **Delete** on the confirmation screen to delete the signatory.


</td></tr></tbody>
</table>
## Result

The changes made to the participants are synced to the ServiceNow instance in Participants related list.

**Parent Topic:**[Edit a contract template using Microsoft Word add-in for ServiceNow Contracts](../task/cncore-edit-ct-addin.md)

