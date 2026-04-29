---
title: Generate a register of information package
description: Use the CSV report option in the download page to generate regulator-ready Register of Information \(RoI\) packages.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [RoI, CSV report, DORA, TPRM]
breadcrumb: [Register of information regulatory packages, Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Generate a register of information package

Use the CSV report option in the download page to generate regulator-ready Register of Information \(RoI\) packages.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../../grc-workspace-vrm/image/ws-list-icon.png) and then navigate to **Digital resilience third-party registers**.

2.  Select **Excel download/upload requests** and then create an Excel download request by selecting **New**.

3.  On the form, select an option and fill in the remaining fields.

    The **Excel Master Template** option downloads documents to use for data preparation and internal review. The **Plain-CSV Reporting Package** option downloads documents that you can use for regulator submission and compliance validation.

    For descriptions of all these fields, see [Create New Excel download/upload request form](../reference/tprm-excel-upload-download-req.md).

    **Note:** Annual expense data is used during report generation for conversion and aggregation. Confirm that currencies and annual expense fields are accurate to avoid conversion failures or skipped aggregation.

4.  Select **Export info register** to initiate the download process.

    When a Register of Information \(RoI\) package is uploaded using the Plain-CSV Report Package option, the system automatically generates a ZIP file containing metadata and report folders with CSV files formatted to meet DORA specifications. Real-time validation is performed during the upload process. If any errors or warnings are detected, a validation report is generated and attached to the request record alongside the CSV package. This report includes mappings to regulator fields \(such as Template Code, Row Code, and Column Code\), rule expressions, field labels, and record identifiers to help you locate and resolve issues. An email notification is sent to whoever initiated the request once the download is complete. If no issues are found, only the CSV package is attached. You can access the report from the attachment area of the request record and cross-reference it with the downloadable Excel master template, which mirrors the CSV structure and assists with error resolution.

    For more information on validation, see [Validate Register of Information packages](tprm-valid-dora.md).


