---
title: Configure non-task tables for contract templates
description: Add non-task tables in the script of an extension point implementation so you can select them while creating contract templates. A non-task table does not extend task tables, and stores records, reference data, or configuration information used across the platform.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
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

    ![Scripted extension point for non-task table.](../image/cmpro-non-task-table.png "Scripted extension point")

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

**Parent Topic:**[Add and configure contract request functionality into your workspace](../concept/cncore-uptake-steps.md)

**Related topics**  


[Add a workspace action button for initiating a contract request](cncore-config-initiate-cont.md)

[Add Contract requests tab to the contract request record](cncore-add-relatedlist-conreq.md)

[Add amendment tabs to contract repository record](cncore-BU-amend-relatedlist.md)

[Add Contract documents tab to the contract repository record](cncore-add-con-doc-relatedl.md)

[Copy fields from parent request to contract request](cncore-copy-fld-frm-parent.md)

[Group contract documents by contract type in a contract request](cncore-config-srp-grouping.md)

[Add access to obligation management from contract repository records](cmpro-add-access-to-ob-mgmt.md)

[Configure the contract request form header for your workspace](cncore-configure-header.md)

[Assign a role for configuring template mappings](cncore-tbl-access-config-role.md)

[Enable contract request fields in condition builders](cncore-add-cmr-condtion-build.md)

[Configuring the Playbook tab on contract repository records](cmpro-config-playbook-tab.md)

