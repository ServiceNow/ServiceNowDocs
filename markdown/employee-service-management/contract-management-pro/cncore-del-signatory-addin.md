---
title: Edit or delete participants using add-in
description: As a contract configurator, edit or delete a participant from a Microsoft Word document using the Microsoft Word add-in for ServiceNow Contracts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contract-management-pro/cncore-del-signatory-addin.html
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Edit a contract template in Microsoft Word, Manage clauses, tables, and contract templates, Manage, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
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

    For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-config-word-addin.md)

4.  In the **Template** tab, select the contract template.

5.  Navigate to the **Signatory** tab.

6.  Select the Edit or delete signatory icon \(\[Omitted image "lsd-three-dots-icon.png"\] Alt text: Edit or delete signatory icon\).

7.  Edit or delete the signatory.

<table id="choicetable_phr_kxb_gzb"><thead><tr><th align="left" id="d157603e142">

Action

</th><th align="left" id="d157603e145">

Steps

</th></tr></thead><tbody><tr><td id="d157603e151">

**Edit the signatory**

</td><td>

1.  Select **Edit signatory**.
2.  Modify the signatory details.
3.  Select **Save**.


</td></tr><tr><td id="d157603e178">

**Delete the signatory**

</td><td>

1.  Select **Delete signatory**.
2.  Select **Delete** on the confirmation screen to delete the signatory.


</td></tr></tbody>
</table>
## Result

The changes made to the participants are synced to the ServiceNow instance in Participants related list.

**Parent Topic:**[Edit a contract template using Microsoft Word add-in for ServiceNow Contracts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-edit-ct-addin.md)

