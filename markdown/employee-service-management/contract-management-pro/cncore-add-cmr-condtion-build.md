---
title: Provide access to contract request fields in condition builders
description: As an administrator, provide access to contract request fields so they can be selected in condition builders.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure contract request functionality, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Provide access to contract request fields in condition builders

As an administrator, provide access to contract request fields so they can be selected in condition builders.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**

2.  Select the application table whose variables should be used in condition builders.

3.  Add the contract request as a reference field to the table.

    1.  Select the **Columns** tab and select **New**.

    2.  In the **Type** field, select the Lookup using list icon \(![Lookup using list icon](../../workplace-lease-administration/images/look-up-icon.png)\) and search for `Reference` and select it.

    3.  In the **Column label**, enter unique label for the column.

    4.  In the **Column label**, enter unique field name of the column.

    5.  Select **Reference Specification** tab.

    6.  In the **Reference** field, select the Contract Request \[sn\_cm\_core\_contract\_request\] table.

    7.  On the Dictionary entry form, fill in the fields.

        For more information, see [Dictionary entry form](https://www.servicenow.com/docs/access?context=r_DictionaryEntryForm&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    8.  Select **Submit**.

4.  Select **Update**.


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

[Provide permissions to configure default contract document information](cncore-tbl-access-config-role.md)

