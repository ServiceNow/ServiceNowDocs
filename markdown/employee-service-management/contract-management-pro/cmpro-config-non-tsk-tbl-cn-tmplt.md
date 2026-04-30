---
title: Configure non-task tables for contract templates
description: Add non-task tables in the script of an extension point implementation so you can select them while creating contract templates. A non-task table does not extend task tables, and stores records, reference data, or configuration information used across the platform.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure contract templates for a contract request, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure non-task tables for contract templates

Add non-task tables in the script of an extension point implementation so you can select them while creating contract templates. A non-task table does not extend task tables, and stores records, reference data, or configuration information used across the platform.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, enter `sn_cm_core.DocumentTemplateNonTaskTableConfiguration`.

3.  Select the record.

4.  In the Related Links section, select **Create implementation**.

5.  On the Script Include form, fill in the fields.

    For a description of the field values, see [Scripted Extension Point form fields](../../legal-request-management/reference/scripted-extension-point-form-fields.md).

6.  In the **Script** field, enter the name of non-task tables that you want to configure for contract templates.

    Use a comma \(,\) to separate the non-task table names in the script.

    The following example shows a script in which two non-task tables are being added.

    ```
          var DocumentTemplateNonTaskTableConfiguration = Class.create();
    DocumentTemplateNonTaskTableConfiguration.prototype = {
        initialize: function() {},
    
        /** 
         * Description: return the list of non-task tables that needs to
         * be added in the table choices in the document template
         * @return {Array} list of tables
         */
        getNonTaskTables: function() {
    		return ['sn_spend_psd_procurement_request_line','sn_quote_mgmt_core_quote']; 
        },
    
        type: 'DocumentTemplateNonTaskTableConfiguration'
    };
    ```

7.  Select **Update**.


## Result

The non-task tables are available for selection in the **table** drop-down list in the Contract templates view of the Word Templates page of the Contract Administration application.

For more information, see [Create a contract template](cncore-create-contract-template.md).

