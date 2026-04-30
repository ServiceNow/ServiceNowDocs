---
title: Configure the contract request form header for your workspace
description: As an administrator, configure the header of the contract request form for your workspace.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure contract request functionality, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure the contract request form header for your workspace

As an administrator, configure the header of the contract request form for your workspace.

## Before you begin

Role required: admin

## About this task

The form header contains a primary field and secondary fields. You can add your workspace to the base system form header tables to specify the fields that appear in a contract request header for your workspace.

![Contract request form header displaying the configured fields](../image/cmpro-cntrct-form-head.png "Contract request form header")

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Configuration Settings** &gt; **UX Form Header**.

2.  In the **Table** column, select the UX Form Header tables related to the contract form.

    |Contract request form fields|Table|
    |----------------------------|-----|
    |**Short description, Priority, Contract state, Parent record, Contract status, and Signature type.**|sn\_cm\_core\_contract\_request|
    |**Participant name**|sn\_cm\_core\_signer\_task|
    |**Name of the document, requester of the contract request, latest version of the document, storage details and the folder where the document is stored**|sn\_cm\_core\_document and select it.|

3.  Select the **UX Header Configurations** tab.

4.  Select **Edit**.

5.  Select your workspace from the Available list and move it to the Selected list.

6.  Select **Save**.

7.  Select **Update**.


**Parent Topic:**[Add and configure contract request functionality into your workspace](../concept/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates](cmpro-config-non-tsk-tbl-cn-tmplt.md)

[Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md)

[Add Contract requests tab to your workspace](cncore-add-relatedlist-conreq.md)

[Add amendment tabs to contract repository record](cncore-BU-amend-relatedlist.md)

[Display contract documents in a contract repository record](cncore-add-con-doc-relatedl.md)

[Copy fields from parent request to contract request](cncore-copy-fld-frm-parent.md)

[Group contract documents by contract type in the contract request form](cncore-config-srp-grouping.md)

[Add access to obligation management from contract repository records](cmpro-add-access-to-ob-mgmt.md)

[Provide permissions to configure default contract document information](cncore-tbl-access-config-role.md)

[Provide access to contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

