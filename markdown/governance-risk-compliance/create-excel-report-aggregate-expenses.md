---
title: Convert and aggregate contractual expenses to regulator-required currencies
description: Convert and aggregate contractual expenses to regulator-required currencies and generate consolidated reports for reporting submissions. Beginning with Digital Operational Resilience Management \(sn\_dora\_accel\), version 22.x.x, these currency conversion and third-party aggregation capabilities are supported for DORA reporting.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Currency conversion and third-party aggregation, Using Digital resilience third-party registers, Maintaining Digital resilience third-party registers, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Convert and aggregate contractual expenses to regulator-required currencies

Convert and aggregate contractual expenses to regulator-required currencies and generate consolidated reports for reporting submissions. Beginning with Digital Operational Resilience Management \(sn\_dora\_accel\), version 22.x.x, these currency conversion and third-party aggregation capabilities are supported for DORA reporting.

## Before you begin

Role required: sn\_oper\_res.admin, sn\_oper\_res.manager

## About this task

Two download types are supported: \(1\) Excel master template — for internal review and analysis; does NOT require Competent Authority, Reference Date, or Date of Reporting fields. \(2\) Plain-CSV reporting package — for regulatory submission; requires Competent Authority, Reference Date, and Date of Reporting; includes Level 3 DPM validation on generation. Currency conversion and aggregation settings are available for both types.

Once the instance is activated, currency rates populate automatically via a daily scheduled job. To align with regulator requirements, administrators or DORA administrators can update currency rates and validation rules at **All &gt; Digital Operational Resilience Management &gt; Digital Resilience Choices or DPM Business Validation Rules**. For more information, see [Currency conversion and third-party aggregation](../concept/currency-conversion-aggregation.md).

![DPM business validation rules.](../image/dora-excel-validation-rules.png)

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **Digital resilience third-party registers** &gt; **Excel download/upload requests** and select **Excel master template** as the Type.

    The example shows the Excel template form.

    ![Excel template.](../image/dora-excel-dload-req-excel-master-temp.png)

2.  Fill in the entity details including the LEI \(Legal Entity Identifier\), entity name, country, and type of entity and set the report type to **Consolidated**.

3.  To enable currency conversion, select **Yes** and specify the base currency \(for example, EUR\).

4.  To enable third-party total expense aggregation, select **Yes**.

    When both currency conversion and aggregation are enabled, aggregation operates on the already-converted base-currency amounts. Raw converted values are summed first; the total is rounded to the nearest whole unit afterward \(for example, 94 + 94 = 188 → 189 EUR\).

5.  Enter the reference date and reporting date and select **Save** to save a request in the Draft state.

    The Reference date defaults to the last day of the prior calendar year; Date of reporting defaults to today's date. Both can be manually overridden before saving.

    After selecting Save, the request is created in Draft state \(number format: REQ000XXXX\).

    The reference date and reporting date are shown in the example.

    ![Request details are filled in.](../image/dora-excel-dload-req-excel-req-form.png)

6.  Verify configuration settings on the **Details** tab.

7.  On the **Contractual arrangements** tab, review and select relevant contracts.

    Review the contracts that will be included in the export as shown in the example.

    ![Contractual arrangements.](../image/dora-excel-dload-req-excel-req-contractual-arrange.png)

8.  To download third-party information register, select the **Export info register** action, enter a file name in the export dialog, and select **Save**.

    The Export info register dialog prompts for a file name. The file name is used as the workbook name in the downloaded Excel file.

9.  Download the generated Microsoft Excel file containing the entity information in Digital Operational Resilience Act \(DORA\) template format.

    ![DORA template with contractual information.](../image/dora-excel-dload-req-excel-output3-201.png)![DORA template with contractual information for 501 format.](../image/dora-excel-dload-req-excel-output4-501.png)

10. Download the "Consolidated\_Reports.zip" file from the Attachments section after the system processes and generates the consolidated reports package.

    For the Excel master template type, the ZIP contains two summary CSVs: Currency\_Conversion\_Summary.csv and Third\_Party\_Aggregation\_Summary.csv.

11. Extract the ZIP file to access the "Currency\_Conversion\_Summary.csv" and Third\_Party\_Aggregation\_Summary.csv reports and review the "Currency Conversion Summary report" to verify conversion details and amounts.

    ![Output formats.](../image/dora-excel-dload-req-excel-consolidated-report-2-outputs.png)

12. To generate a Comma-Separated Values \(CSV\) reporting package for regulatory submission, create an Excel Upload/Download request and select the **Plain-CSV reporting package** type.

    The Plain-CSV reporting package type is shown in the example.

    ![Plain-csv reporting package type.](../image/dora-excel-dload-req-csv-option.png)

13. Fill in the entity configuration with the currency conversion and aggregation settings, then save the CSV package request to initiate asynchronous processing.

    ![CSV reports.](../image/dora-excel-dload-req-csv-option-csv-reports.png)

    On Save, an info banner displays: "Plain-csv reporting package generation initiated. Processing time varies based on data volume." No page refresh is needed.

14. Monitor the Result section for processing status, including validation and package generation and download the generated attachments — "Consolidated\_Reports.zip" and the main CSV reporting package file once processing completes.

    The Attachments panel displays the generated report files. Download the reporting package and submit it to the regulator. The package contains three CSV files: Currency\_Conversion\_Summary, Level3\_DPM\_Validation\_Summary, and Third\_Party\_Aggregation\_Summary. The DPM validation report lists each data point, the number of records checked, the number of records that passed, and any rule violations identified before submission.

    The Result &gt; Messages section displays timestamped log entries, for example: \[2026-01-28 12:07:06\] Plain-csv reporting package generation initiated. \[2026-01-28 12:07:19\] Level 3 DPM validation completed successfully. \[2026-01-28 12:07:19\] Consolidated reports \(Third-party total expense aggregation, Level 3 DPM validation\) have been generated and attached to this request. \[2026-01-28 12:07:19\] Plain-csv reporting package generated successfully.

15. Open the CSV file and review the structured data formatted for regulatory reporting.

    **Note:** The CSV file is comma-delimited. Opening it in Excel may trigger a data-loss warning. For review, open directly in a text editor or CSV viewer to preserve formatting fidelity.

    The example shows the CSV file with structured currency data.

    ![CSV file with currency data.](../image/dora-excel-dload-req-csv-option-csv-3.png)

    When selecting Plain-CSV reporting package type, these additional fields are required: Competent authority \(for example, "CA"\), Reference date \(defaults to last day of prior year, for example, 2025-12-31\), and Date of reporting \(defaults to today, for example, 2026-01-28\). These fields do not appear on the Excel master template request form.

    **Note:** If any providers were ineligible for aggregation, the aggregation summary and detail reports identify those providers and explain the reason they were skipped.


**Parent Topic:**[Currency conversion and third-party aggregation](../concept/currency-conversion-aggregation.md)

