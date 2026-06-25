---
title: Activate a system property to generate a certificate of completion
description: As a contract configurator, activate a system property to generate a certificate of completion for electronically signed contracts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/contract-management-pro/cncore-config-system-prop-COC.html
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Certificate of completion]
breadcrumb: [Configure additional features in CM Pro, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Activate a system property to generate a certificate of completion

As a contract configurator, activate a system property to generate a certificate of completion for electronically signed contracts.

## Before you begin

You must have configured an electronic signature provider. For more information, see [Configure an e-signature provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cncore-integrate-esign.md).

Role required: admin

## About this task

**Note:** This feature is applicable only for electronically signed contracts.

The certificate of completion provided by Docusign or Adobe Acrobat Sign includes the audit trail with the time stamp details about each signatory action during an electronic signature. The audit trail ensures non-repudiation and resolves any objections.

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for the `sn_cm_core.enable_executed_contract_audit_certificate` property.

    \[Omitted image "cmpro-audit-certificate.png"\] Alt text: Audit certificate property for executed contracts.

3.  Select the property.

4.  If you aren’t able to edit the property in the current application scope, select the word **here** in the message at the top of the page.

5.  Update the **Value** field to `true`.

6.  Select **Update**.


## Result

A certificate of completion will be generated for all electronically signed contracts.

**Parent Topic:**[Configure additional features in Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/contract-management-pro/cmpro-additional-feature.md)

**Related topics**  


[Configuring Contract Workspace]()

[Configure signature pause duration when modifying signatories]()

[Auto-populate the start date and end date for contract requests]()

[Enable users to view email details in activity stream]()

[Enable keyword search for contract templates]()

[Configuring contract summarization for Contract Management Pro]()

[Configure conditions to send reminder notifications for expiring contracts]()

[Copy fields from parent request to amendment request]()

[Manage notifications in Contract Management Pro]()

