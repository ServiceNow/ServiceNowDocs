---
title: Copy fields from parent request to contract request
description: Configure the ContractManagementExt extension point to automatically copy required fields from the parent record to the contract request when it is initiated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/employee-service-management/contract-management-pro/cncore-copy-fld-frm-parent.html
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

    For a description of the field values, see [Scripted Extension Point form fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/legal-request-management/scripted-extension-point-form-fields.md).

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

**Parent Topic:**[Add and configure contract request functionality into your workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/employee-service-management/contract-management-pro/cncore-uptake-steps.md)

**Related topics**  


[Configure non-task tables for contract templates]()

[Add a workspace action button for initiating a contract request]()

[Add Contract requests tab to your workspace]()

[Add amendment tabs to contract repository record]()

[Display contract documents in a contract repository record]()

[Group contract documents by contract type in the contract request form]()

[Add access to obligation management from contract repository records]()

[Configure the contract request form header for your workspace]()

[Provide permissions to configure default contract document information]()

[Provide access to contract request fields in condition builders]()

