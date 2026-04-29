---
title: Convert and aggregate contractual expenses to regulator-required currencies
description: Convert and aggregate contractual expenses to regulator-required currencies and generate consolidated reports for reporting submission.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Currency conversion and third-party total expense aggregation, Use digital resilience third-party registers, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Convert and aggregate contractual expenses to regulator-required currencies

Convert and aggregate contractual expenses to regulator-required currencies and generate consolidated reports for reporting submission.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_admin or sn\_vdr\_risk\_asmt.vendor\_manager

## About this task

Administrators maintain the currency rates and validation rules. Currency rates populate automatically using a daily scheduled job once the instance is activated. Administrators or DORA administrators can update currency rates and validation rules to align with regulator requirements by navigating to **All** &gt; **Digital Operational Resilience Management** &gt; **Digital Resilience Choices** or **DPM Business Validation Rules**.

## Procedure

1.  Navigate to **Workspaces** &gt; **Vendor Management Workspace** &gt; **Digital resilience third-party registers** &gt; **Excel download/upload requests** and select **Excel master template** as the Type.

2.  Fill in the entity details including the LEI \(Legal Entity Identifier\), entity name, country, and type of entity and set the report type to **Consolidated**.

    For descriptions of all these fields, see [Create New Excel download/upload request form](../reference/tprm-excel-upload-download-req.md).

3.  Enable currency conversion by selecting **Yes** and specify the base currency \(for example, EUR\).

4.  Enable third-party total expense aggregation by selecting **Yes**.

5.  Enter the reference date and reporting date.

6.  Save the request to create it in Draft state and review the request details on the **Details** tab to verify all configuration settings.

7.  View associated contracts on the **Contractual arrangements** tab.

8.  To download the third-party information register, select the **Export info register** action and in the export dialog, enter a file name and select **Save**.

9.  Download the generated Microsoft Excel file containing the entity information in the DORA template format.

10. Download the Consolidated\_Reports.zip file from the Attachments section after the system processes and generates the consolidated reports package.

11. Extract the ZIP file to access the Currency\_Conversion\_Summary.csv and Third\_Party\_Aggregation\_Summary.csv reports and review the Currency Conversion Summary report to verify conversion details and amounts.

12. To generate a Comma-Separated Values \(CSV\) reporting package for regulatory submission, create a request and select **Plain-csv reporting package** as the type

13. Fill in the same entity configuration with currency conversion and aggregation settings and save the CSV package request to initiate asynchronous processing.

14. Monitor the Result section for processing messages including validation completion and package generation status and download the generated attachments including the Consolidated\_Reports.zip and the main CSV reporting package file once processing completes.

15. Open the CSV file to review the structured data formatted for regulatory reporting.

    If any providers were ineligible for aggregation, the aggregation summary and detail reports identify those providers and explains the reason they were skipped.


