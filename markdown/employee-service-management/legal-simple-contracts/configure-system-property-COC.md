---
title: Activate a system property to generate a certificate of completion
description: As an admin, activate the sn\_lg\_contracts.enable\_executed\_contract\_audit\_certificate system property to generate a certificate of completion for electronically signed non-disclosure agreements \(NDA\) and third-party contracts.
locale: en-US
release: zurich
product: Legal Simple Contracts
classification: legal-simple-contracts
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Legal Simple Contracts, Configure, Legal Simple Contracts, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Activate a system property to generate a certificate of completion

As an admin, activate the **sn\_lg\_contracts.enable\_executed\_contract\_audit\_certificate** system property to generate a certificate of completion for electronically signed non-disclosure agreements \(NDA\) and third-party contracts.

## Before you begin

You must have configured an electronic signature provider. For more information, see [Configure an e-signature provider for legal contracts](integrate-legal-contracts-esign.md).

Role required: sn\_lg\_ops.legal\_admin

## About this task

**Note:** This feature is applicable only for electronically signed contracts. For more information on submitting NDA and third-party contracts, see [Submit a legal request for a NDA](submit-legal-contract-request.md) and [Submit a legal request for a third-party contract review](submit-legal-request-tpc-review.md).

The certificate of completion provided by Docusign or Adobe Acrobat Sign includes the audit trail with the timestamp details about each signatory action during an electronic signature. The audit trail ensures non-repudiation and resolves any objections.

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for the `sn_lg_contracts.enable_executed_contract_audit_certificate` property.

3.  Select the property.

4.  If you aren’t able to edit the property in the current application scope, select the word **here** in the message at the top of the page.

5.  Update the **Value** field to `true`.

6.  Select **Update**.


## Result

A certificate of completion will be issued for the contract.

