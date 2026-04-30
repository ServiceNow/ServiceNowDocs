---
title: Activate a system property to generate a certificate of completion
description: As a contract configurator, activate a system property to generate a certificate of completion for electronically signed contracts.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up Contracts Core, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Activate a system property to generate a certificate of completion

As a contract configurator, activate a system property to generate a certificate of completion for electronically signed contracts.

## Before you begin

You must have configured an electronic signature provider. For more information, see [Configure an e-signature provider](cncore-integrate-esign.md).

Role required: sn\_cm\_core.contract\_config

## About this task

**Note:** This feature is applicable only for electronically signed contracts.

The certificate of completion provided by Docusign or Adobe Acrobat Sign includes the audit trail with the time stamp details about each signatory action during an electronic signature. The audit trail ensures non-repudiation and resolves any objections.

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for the `sn_cm_core.enable_executed_contract_audit_certificate` property.

3.  Select the property.

4.  If you aren’t able to edit the property in the current application scope, select the word **here** in the message at the top of the page.

5.  Update the **Value** field to `true`.

6.  Select **Update**.


## Result

A certificate of completion will be issued for the electronically signed contract.

**Parent Topic:**[Set up Contracts Core](../concept/cncore-setup-cmpro.md)

**Related topics**  


[Create a contract type](cncore-create-contract-type.md)

[Create document template categories](cncore-create-doc-tmplt-cat.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Configure reminders for expiring contracts](cncore-config-rem-exp-cont.md)

[Configuring external applications for Contract Management Pro](../concept/cncore-set-ext-app-config.md)

[Configure extension point for notifications](cmpro-configure-action-extension-point-email-notification-admin.md)

[Use default email notifications](cmpro-send-receive-email-notification-admin.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

