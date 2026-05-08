---
title: Edit or delete table mappings in a contract template using Microsoft Word add-in
description: As a contract configurator, edit or delete table mappings in a contract template using the Microsoft Word add-in.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Edit a contract template in Microsoft Word, Manage clauses, tables, and contract templates, Manage, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Edit or delete table mappings in a contract template using Microsoft Word add-in

As a contract configurator, edit or delete table mappings in a contract template using the Microsoft Word add-in.

## About this task

Using table mappings you can map data source tables in your ServiceNow instance to tables in a contract template. The mappings determine which records from the data source table will be added in the contract and where it will be added.

## Before you begin

Role required: sn\_cm\_core.contract\_config and canvas\_user

## Procedure

1.  Open the contract template where you want to edit or delete the table mappings.

2.  From the Microsoft Word ribbon, select ServiceNow Contracts add-in.

3.  On the login screen, enter the credentials of the ServiceNow instance for which the Microsoft Word add-in is configured.

    For more information, see [Configure the Microsoft Word add-in for ServiceNow Contracts](cncore-config-word-addin.md)

4.  Select the **Table** tab.

5.  In the list of table mappings, select the mapping or find it by entering the table name in the search bar.

6.  Either modify or delete the table mapping.

<table id="choicetable_rvj_4rw_bcc"><thead><tr><th align="left" id="d136836e140">

Action

</th><th align="left" id="d136836e143">

Steps

</th></tr></thead><tbody><tr><td id="d136836e149">

**Delete the table mapping**

</td><td>

1.  Select the menu icon ![Menu icon](../../legal-simple-contracts/image/menu-icon.png).
2.  Select **Delete**.

The content controls related to the table mapping are removed from the Microsoft Word document.

</td></tr><tr><td id="d136836e181">

**Modify the table mapping**

</td><td>

1.  Select the menu icon ![Menu icon](../../legal-simple-contracts/image/menu-icon.png).
2.  Select **Edit**.

For more information, see [Map contract tables using the Microsoft Word add-in for ServiceNow Contracts](cncore-addin-table.md).

**Note:** When you update the fields in the **Table mapping details** section, you might need to map the table and columns again based on the following conditions:

    -   If you change the table in the **Table** field and select **Update**, all the sections in the Microsoft Word add-in screen are cleared and you must perform the mapping again.
    -   If you change the table name in the **Name** field and select **Update**, the content control of the mapped table in the Microsoft Word document is removed. You must map the table and table columns again.
    -   If you remove a column from the **Table column** field and select **Update**, the content control of the mapped table column in Microsoft Word document is removed.


</td></tr></tbody>
</table>
**Parent Topic:**[Edit a contract template using Microsoft Word add-in for ServiceNow Contracts](cncore-edit-ct-addin.md)

