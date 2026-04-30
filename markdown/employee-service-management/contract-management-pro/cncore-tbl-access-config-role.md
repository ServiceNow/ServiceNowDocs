---
title: Provide permissions to configure default contract document information
description: As an administrator, enable a contract user to configure information placed in the contract document by assigning a contract configurator role.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure contract request functionality, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Provide permissions to configure default contract document information

As an administrator, enable a contract user to configure information placed in the contract document by assigning a contract configurator role.

## Before you begin

Role required: admin

## About this task

Template mappings automatically insert default values in the contract document. To configure template mappings, the contract user requires a contracts configurator \(sn\_cm\_core.contract\_config\) role. For more information on how to configure template mappings, see [Update contract template mappings](cncore-template-mapping.md).

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Users**.

2.  Search for and select the user.

3.  In the Roles related list, select **Edit**.

4.  Move the sn\_cm\_core.contract\_config role from the Available list to the Selected list.

5.  Select **Save**.

6.  Save the user record by selecting **Update**.


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

[Configure the contract request form header for your workspace](cncore-configure-header.md)

[Provide access to contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

