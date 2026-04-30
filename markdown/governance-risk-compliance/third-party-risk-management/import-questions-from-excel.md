---
title: Import a questionnaire from a spreadsheet
description: If you maintain questionnaires using Microsoft Excel spreadsheets, you can save time and effort by importing your spreadsheet data directly into TPRM tables. You can then create questionnaires automatically from templates.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Classic assessments, Configure, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Import a questionnaire from a spreadsheet

If you maintain questionnaires using Microsoft Excel spreadsheets, you can save time and effort by importing your spreadsheet data directly into TPRM tables. You can then create questionnaires automatically from templates.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_risk\_manager

## About this task

Before you import questionnaires, you must validate that the data in the spreadsheet meets certain requirements. To assist you before you import the spreadsheet, you can review the formatting requirements and view or download a sample spreadsheet to use as a guide. See [Guidelines for importing spreadsheet data](../concept/excel-formatting-guidelines.md).

You can specify the following property settings:

-   **Text delimiter in spreadsheets \[`sn_vdr_risk_asmt.excel_choice_delimiter`\]**

    Character string that separates response text in questions of type ‘Choice’ and ‘Multiple Selection’.

    Common delimiters: \\r, \\n, \\t, \\r\\n, and the comma character.

-   **Maximum spreadsheet file size \[`sn_vdr_risk_asmt.excel_file_max_size`\]**

    Maximum file size in MB that can be imported.


See [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md).

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Assessment Setup** &gt; **Questionnaire Templates** or to **Third-party Risk Management** &gt; **Tiering Setup** &gt; **Tiering Questionnaire Templates**.

2.  Select **Import from Excel** to open the Import Questionnaire Template form.

    ![Assessment metric types.](../image/asst-metric-types.png)

    ![Import questionnaire template.](../image/import-quest-template.png)

    **Note:** You can review the formatting requirements and view or download a sample spreadsheet to use as an example. Referencing a sample file can help you ensure that you are using values in the expected format.

3.  Perform any or all of the steps in the **Prepare your Excel file** section:

    -   Select **Download sample file** to download an active worksheet that is properly formatted for import into Third-party Risk Management. You can use the sample as a guide for reformatting your own spreadsheet, or you can copy data from your spreadsheet directly into the sample.
    -   Select **View sample** to open an image of a properly-formatted worksheet. You can compare this with your existing worksheet to validate that it contains the same columns and question formats.
    -   Select **Format guidelines** to view [Guidelines for importing spreadsheet data](../concept/excel-formatting-guidelines.md).
4.  When your spreadsheet is ready for import, either drag it into the **Drop an Excel file here** box, or select **Choose File**, navigate to your Excel file, and then select **Open**.

    Errors and warning appear if the file is formatted incorrectly. You must fix all errors before the questionnaires can be imported. You can import a file that has only warnings, but there might be issues in the resulting question data.

    ![Errors and warnings for an incorrectly formatted spreadsheet.](../image/excel-errors-warnings.png)

    **Note:** If there are warnings, you can continue with the import, but issues might arise. Consider fixing all errors and warnings before you import questionnaires.

5.  After you have fixed errors and warnings, enter a name for the template, and then select **Import**.

    The name must be unique. The name defaults to the worksheet name in your spreadsheet.

    A confirmation pop-up displays the imported questionnaire.

    ![Metric categories.](../image/metric-categories.png)

6.  You can expand a category to view the questions in each category.

    ![Expanded metric category.](../image/metric-category-expanded.png)


**Parent Topic:**[Governance, Risk, and Compliance](../../grc-common/reference/r_WhatIsGRC.md)

**Related topics**  


[Guidelines for importing spreadsheet data](../concept/excel-formatting-guidelines.md)

[Import existing data from other systems](../../grc-vendor-risk-implementation/task/tprm-historical-data-import.md)

