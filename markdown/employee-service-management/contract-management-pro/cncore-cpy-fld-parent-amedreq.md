---
title: Copy fields from parent request to amendment request
description: Configure the ContractManagementExt extension point to automatically copy fields to contract request from the linked parent request and parent contract.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Automatic copy fields, Configure extension point]
breadcrumb: [Configure additional features in CM Pro, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Copy fields from parent request to amendment request

Configure the ContractManagementExt extension point to automatically copy fields to contract request from the linked parent request and parent contract.

## About this task

As an admin, you can configure fields for which the values from the contract repository record will be automatically copied to the amendment request. Configure common fields between the contract repository record and the amendment request so that the contract fulfiller can update them as per the requested amendments. Example: If you configure end date and payment terms to be available and automatically copied from the contract repository, the fulfiller can modify value for these fields as part of the amendment request.

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
    
    /**
    	 * @param {GlideRecord} parentRequestGr - GlideRecord of BU request record
    	 * @param {GlideRecord} contractGr - GlideRecord of signed contract record. This will be available only for amendments. 
            * For new contract request, this will be null.
       * Make sure to check for null before using contractGr
    	 * @param {String} requestType - Helps to identify if the request is `amendment` or `cmr`
    	 * @param {String} application - Id of application. Helps to identify to which Business unit or appplication the contract request belongs to
    	 * @returns {Object} - Key value pairs of fieldName and its value in data sub-object
       * contractGr will be provided only in case of amendment request type.
       * Based on the request type, can add required mapppings for CMR record.
       * For New contract request, mapping can be done from parentRequestGr to ContractRequest record
       * For Amendment, mapping can be done from parentRequestGr and contractGr to ContractRequest record
    	 * Example- { data: {'account': 'xyz_sys_id', 'end_date': '2025-12-07'} }
    	 */
    	copyDataFromBUToCMR: function(parentRequestGr, requestType, contractGr,  application) {
                data: {
                          'account': parentRequestGr.getValue('account'),
                          'end_date': parentRequestGr.getValue('contract_end_date'),
                	},
    
        type: 'ContractManagementExt'
    };
    ```

    **Note:** The data type of the parent contract repository record field and the contract request field must match.

7.  Select **Update**.

8.  In the Extension Point form, select **Update**.


## Result

When a contract request is initiated, the configured fields are automatically populated with the corresponding values from the associated contract repository record selected while initiating an amendment request.

**Parent Topic:**[Configure additional features in Contract Management Pro](../concept/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace](../concept/cncore-conf-cntrct-wrkspc.md)

[Configure signature pause duration when modifying signatories](cncore-pause-sig-property.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Enable keyword search for contract templates](cncore-enable-search-cont-tmplts.md)

[Configuring contract summarization for Contract Management Pro](cmpro-conf-cntr-summary.md)

[Configure conditions to send reminder notifications for expiring contracts](cncore-config-rem-exp-cont.md)

[Manage notifications in Contract Management Pro](../concept/cmpro-manage-notifications.md)

