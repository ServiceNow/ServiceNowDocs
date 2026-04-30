---
title: Validate the Register of Information packages
description: Run real-time validation on Register of Information \(RoI\) packages to help ensure compliance with DORA requirements.
locale: en-US
release: yokohama
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 1
breadcrumb: [Configuring Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Validate the Register of Information packages

Run real-time validation on Register of Information \(RoI\) packages to help ensure compliance with DORA requirements.

## Before you begin

Role required: sn\_oper\_res.manager

Generate a Plain-CSV Reporting Package and an Excel Master Template. For more information, see [Generate a Register of Information package](opres-drtp-gen-roi-pkg.md).

## About this task

Validation is performed automatically when a ZIP file containing RoI CSV templates is uploaded via an Excel download/upload request. The system initiates real-time validation without requiring a separate request type.

Once validation is complete, the system sends an email notification to whoever initiated the request. If validation warnings are detected, both the validation report and the CSV package are attached to the request record. If no issues are found, only the CSV package is included.

The validation report contains mappings to regulator fields such as Template Code, Row Code, and Column Code, along with rule expressions, field labels, and record identifiers. These details help users locate and resolve issues efficiently.

To review and resolve validation errors, download the Excel template from the **Download/Upload Request** page. The template mirrors the CSV structure and includes field definitions, formats, and sample values. Use it to cross-reference the validation report and identify the location and context of each issue.

Validation reports are only generated when errors or warnings are present. If no issues are found, only the CSV package is returned.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Excel download/upload requests**.

2.  Open the request record you want.

3.  Download the validation report from the attachment area of the request record.

4.  Cross-reference the validation report with the Excel template to identify and correct issues.

5.  Update the affected records in the system or spreadsheet and re-upload the corrected package for re-validation.


**Parent Topic:**[Configuring Digital resilience third-party registers](../concept/conf-dg-resi-party-regi.md)

