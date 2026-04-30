---
title: Copy fields from parent request to contract request
description: Configure the ContractManagementExt extension point to automatically copy required fields from the parent record to the contract request when it is initiated.
locale: en-US
release: yokohama
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-06-17"
reading_time_minutes: 2
breadcrumb: [Configure contract request functionality, Configuring Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Copy fields from parent request to contract request

Configure the ContractManagementExt extension point to automatically copy required fields from the parent record to the contract request when it is initiated.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, enter sn\_cm\_core.ContractManagementExt.

3.  Select the record.

4.  In the Related Links section, select **Create implementation**.

5.  On the Script Include form, fill in the fields.

    For a description of the field values, see [Scripted Extension Point form fields](../../legal-request-management/reference/scripted-extension-point-form-fields.md).

6.  In the **Script** field, update the copyDataFromBUToCMR function to configure the fields that you want to copy from the parent record to the contract request.

    For example, if you want to copy the **Account** and **End date** fields from a parent record to contract request, you can use the following:

    ```
    copyDataFromBUToCMR: function(parentRequestGr) {
    	return {
             data: {
              'account': parentRequestGr.getValue('account'),
              'end_date': parentRequestGr.getValue('contract_end_date'),
       }
      };
    },
    ```

    **Note:** The data type of the parent record field and the contract request field must match.

7.  Select **Update**.

8.  In the Extension Point form, select **Update**.


## Result

When a contract request is initiated, the configured fields are automatically populated with the corresponding values from the associated parent record.

**Parent Topic:**[Add and configure contract request functionality into your workspace](../concept/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates](cmpro-config-non-tsk-tbl-cn-tmplt.md)

[Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md)

[Add Contract requests tab to your workspace](cncore-add-relatedlist-conreq.md)

[Add amendment tabs to contract repository record](cncore-BU-amend-relatedlist.md)

[Display contract documents in a contract repository record](cncore-add-con-doc-relatedl.md)

[Group contract documents by contract type in the contract request form](cncore-config-srp-grouping.md)

[Add access to obligation management from contract repository records](cmpro-add-access-to-ob-mgmt.md)

[Configure the contract request form header for your workspace](cncore-configure-header.md)

[Provide permissions to configure default contract document information](cncore-tbl-access-config-role.md)

[Provide access to contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

