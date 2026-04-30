---
title: Generate a Register of Information package
description: Generate a register of information package. Use the CSV report option in the download page to generate regulator-ready Register of Information \(RoI\) packages.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2025-11-18"
reading_time_minutes: 2
breadcrumb: [Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Generate a Register of Information package

Generate a register of information package. Use the CSV report option in the download page to generate regulator-ready Register of Information \(RoI\) packages.

## Before you begin

Role required: sn\_oper\_res.manager

## About this task

Register of Information \(RoI\) reports can be generated for both individual and consolidated legal entities. When viewing an individual entity, only contracts associated with its specific LEI are displayed. For a consolidated view, all contracts across the system are visible.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Excel download/upload requests**.

2.  Create an Excel download request by selecting **New**.

3.  On the form, fill in the fields.

    The **Excel Master Template** option downloads documents to use for data preparation and internal review. The **Plain-CSV Reporting Package** option downloads documents you can use for regulator submission and compliance validation.

    For descriptions of all these fields, see [Create New Excel download/upload request form](../../grc-vendor-risk/reference/tprm-excel-upload-download-req.md).

4.  Select **Export info register** to initiate the download process.

    When a Register of Information \(RoI\) package is uploaded using the Plain-CSV Report Package option, the system automatically generates a ZIP file containing metadata and report folders with CSV files formatted to meet DORA specifications. Real-time validation is performed during the upload process. If any errors or warnings are detected, a validation report is generated and attached to the request record alongside the CSV package. This report includes mappings to regulator fields \(such as Template Code, Row Code, and Column Code\), rule expressions, field labels, and record identifiers to help users locate and resolve issues.

    An email notification is sent to whoever initiated the request once the download is complete. If no issues are found, only the CSV package is attached. Users can access the report from the attachment area of the request record and cross-reference it with the downloadable Excel template, which mirrors the CSV structure and assists with error resolution.

    For more information on validation, see .


**Parent Topic:**[Using Digital resilience third-party registers](../concept/using-dg-registers.md)

