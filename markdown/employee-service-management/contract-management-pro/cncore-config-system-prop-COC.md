---
title: Activate a system property to generate a certificate of completion
description: As a contract configurator, activate a system property to generate a certificate of completion for electronically signed contracts.
locale: en-US
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
keywords: [Certificate of completion]
breadcrumb: [Configure additional features in CM Pro, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
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

    ![Audit certificate property for executed contracts.](../image/cmpro-audit-certificate.png "Audit certificate property")

3.  Select the property.

4.  If you aren’t able to edit the property in the current application scope, select the word **here** in the message at the top of the page.

5.  Update the **Value** field to `true`.

6.  Select **Update**.


## Result

A certificate of completion will be generated for all electronically signed contracts.

**Parent Topic:**[Configure additional features in Contract Management Pro](../concept/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace](../concept/cncore-conf-cntrct-wrkspc.md)

[Configure signature pause duration when modifying signatories](cncore-pause-sig-property.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Enable keyword search for contract templates](cncore-enable-search-cont-tmplts.md)

[Configuring contract summarization for Contract Management Pro](cmpro-conf-cntr-summary.md)

[Configure conditions to send reminder notifications for expiring contracts](cncore-config-rem-exp-cont.md)

[Copy fields from parent request to amendment request](cncore-cpy-fld-parent-amedreq.md)

[Manage notifications in Contract Management Pro](../concept/cmpro-manage-notifications.md)

