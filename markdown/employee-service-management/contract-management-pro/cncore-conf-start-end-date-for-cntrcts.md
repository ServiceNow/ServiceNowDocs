---
title: Auto-populate the start date and end date for contract requests
description: Configure an extension point implementation to automatically add the start date and end date while creating a contract request.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Auto-populate dates in contract]
breadcrumb: [Configure additional features in CM Pro, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Auto-populate the start date and end date for contract requests

Configure an extension point implementation to automatically add the start date and end date while creating a contract request.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  In the **API Name** field, enter `sn_cm_core.ContractManagementExt`.

3.  Select the record.

4.  In the Related Links section, select **Create implementation**.

5.  On the Script Include form, fill in the fields.

    ![Extension point to add scripts.](../image/cmpro-extension-point.png "Scripted extension point for contracts")

    For a description of the field values, see [Scripted Extension Point form fields](../../legal-request-management/reference/scripted-extension-point-form-fields.md).

6.  In the **Script** field, add a method `populateDataForInitiateContractModal` to define the fields from which the values will be automatically added in the **Start date** and **End date** fields of a contract request.

    You can also define the exact dates for the **Start date** and **End date**.

7.  Select **Update**.


## Result

The **Start date** and **End date** fields in the Initial contract window are automatically updated from the parent record while creating a contract request.

For more information on initiating a contract request, see [Initiating a contract or amendment request](cncore-initiate-contract.md).

**Parent Topic:**[Configure additional features in Contract Management Pro](../concept/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace](../concept/cncore-conf-cntrct-wrkspc.md)

[Configure signature pause duration when modifying signatories](cncore-pause-sig-property.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Enable keyword search for contract templates](cncore-enable-search-cont-tmplts.md)

[Configuring contract summarization for Contract Management Pro](cmpro-conf-cntr-summary.md)

[Configure conditions to send reminder notifications for expiring contracts](cncore-config-rem-exp-cont.md)

[Copy fields from parent request to amendment request](cncore-cpy-fld-parent-amedreq.md)

[Manage notifications in Contract Management Pro](../concept/cmpro-manage-notifications.md)

