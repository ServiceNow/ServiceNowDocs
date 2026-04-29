---
title: Guidelines for importing spreadsheet data
description: Before you try to import the questionnaire data from a Microsoft Excel spreadsheet into Third-party Risk Management tables, you must verify that its format meets particular guidelines.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Guidelines for importing spreadsheet data

Before you try to import the questionnaire data from a Microsoft Excel spreadsheet into Third-party Risk Management tables, you must verify that its format meets particular guidelines.

## Property settings that affect spreadsheet data

You can specify the following property settings:

-   **Text delimiter in spreadsheets \[`sn_vdr_risk_asmt.excel_choice_delimiter`\]**

    Character string that separates response text in questions of type ‘Choice’ and ‘Multiple Selection’.

    Common delimiters: \\r, \\n, \\t, \\r\\n, and the comma character.

-   **Maximum spreadsheet file size \[`sn_vdr_risk_asmt.excel_file_max_size`\]**

    Maximum file size in MB that can be imported.


See [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

## Supported columns

Required columns are marked with \*. Column headings must appear in the first row of the spreadsheet.

-   Serial number \*
-   Category \*
-   Question \*
-   Order \*
-   Data type \*
-   Description
-   Scored
-   Correct answer
-   Scale definition
-   Depends on
-   Displayed when
-   Min
-   Max
-   Weight
-   Mandatory
-   Allow additional information
-   Allow not applicable
-   All other columns of the Assessment Metric \[asmt\_metric\] table

## Supported question types

-   Check box
-   Yes/No
-   Choice
-   Attachment
-   Date
-   Date/Time
-   Percentage
-   String
-   Multiple Selection
-   Number
-   Numeric Scale

## Supported Excel formats

Requirements:

-   Each file can have only one worksheet.
-   You can separate multiple choices in a cell with line breaks \(Alt/Option + Enter\). Other options are available in System Properties.

-   .xlsx
-   .xls
-   .xlm
-   .xltx
-   .xlt
-   .xlw
-   .xlsb
-   .csv

**Note:** You can review the formatting requirements and view or download a sample spreadsheet to use as an example. Referencing a sample file can help you ensure that you are using values in the expected format.

![Helpful resources for preparing your spreadsheet. For the text description, refer to the note that preceded this.](../image/import-quest-template.png)

**Parent Topic:**[Third-party Risk Management reference](tprm-reference.md)

**Related topics**  


[Import a questionnaire from a spreadsheet](../task/import-questions-from-excel.md)

[Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md)

