---
title: Add amendment tabs to contract repository record
description: To view the details of the contract amendment, add the amendment related tabs to the contract repository record.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Contract requests, Related list, Uptake steps for CM Pro, BU configuration]
breadcrumb: [Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Add amendment tabs to contract repository record

To view the details of the contract amendment, add the amendment related tabs to the contract repository record.

## Before you begin

Role required: admin

## About this task

Once the contract amendment is signed, you can see the details in the following tabs of the contract repository record:

-   Contract Documents: Provides access to all signed documents related to the contract, including those generated or updated as part of amendment processes.
-   Contract Requests: Displays all contract and amendment requests associated with the contract.
-   Amendment Field Changes: Shows a detailed log of all field changes made through amendments, enabling easy tracking of modifications over time.

You must add these tabs to the contract repository record for your workspace.

![Contract repository record showing amendment related details](../../lsd-sn-legal-contracts/image/lsd-amend-related-lists.png)

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**

2.  Select the table to which your form is associated.

3.  Select ![Context menu icon](../../universal-task/images/context-menu.png) and select **Configure** &gt; **Related Lists**.

4.  In the **View** list, select the workspace view that should include the amendment related tab.

5.  Add the Contract requests tab by moving **Contract Request**, **Contract documents**, and **Amendment history-&gt;Contract** from the Available list to the Selected list.

    ![Moving related lists from Available list to Selected list.](../image/cmpro-bu-add-cr-related-list.png "Add Related Lists")

6.  Select **Save**.

7.  Select **Update**.


## Result

The Contract amendment related tabs are available from your workspace to view the amendment details.

For more information on contract amendment, see [Contract amendments](cmpro-amend-landing.md).

**Parent Topic:**[Add and configure contract request functionality into your workspace](../concept/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates](cmpro-config-non-tsk-tbl-cn-tmplt.md)

[Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md)

[Add Contract requests tab to the contract request record](cncore-add-relatedlist-conreq.md)

[Add Contract documents tab to the contract repository record](cncore-add-con-doc-relatedl.md)

[Copy fields from parent request to contract request](cncore-copy-fld-frm-parent.md)

[Group contract documents by contract type in a contract request](cncore-config-srp-grouping.md)

[Add access to obligation management from contract repository records](cmpro-add-access-to-ob-mgmt.md)

[Configure the contract request form header for your workspace](cncore-configure-header.md)

[Assign a role for configuring template mappings](cncore-tbl-access-config-role.md)

[Enable contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

[Configuring the Playbook tab on contract repository records](cmpro-config-playbook-tab.md)

