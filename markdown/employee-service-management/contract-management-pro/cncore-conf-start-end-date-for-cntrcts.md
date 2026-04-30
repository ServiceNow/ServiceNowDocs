---
title: Auto-populate the start date and end date for contract requests
description: Configure an extension point implementation to automatically add the start date and end date while creating a contract request.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up Contracts Core, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
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

    For a description of the field values, see [Scripted Extension Point form fields](../../legal-request-management/reference/scripted-extension-point-form-fields.md).

6.  In the **Script** field, add a method `populateDataForInitiateContractModal` to define the fields from which the values will be automatically added in the **Start date** and **End date** fields of a contract request.

    You can also define the exact dates for the **Start date** and **End date**.

7.  Select **Update**.


**Parent Topic:**[Set up Contracts Core](../concept/cncore-setup-cmpro.md)

**Related topics**  


[Create a contract type](cncore-create-contract-type.md)

[Create document template categories](cncore-create-doc-tmplt-cat.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Configure reminders for expiring contracts](cncore-config-rem-exp-cont.md)

[Configuring external applications for Contract Management Pro](../concept/cncore-set-ext-app-config.md)

[Configure extension point for notifications](cmpro-configure-action-extension-point-email-notification-admin.md)

[Use default email notifications](cmpro-send-receive-email-notification-admin.md)

