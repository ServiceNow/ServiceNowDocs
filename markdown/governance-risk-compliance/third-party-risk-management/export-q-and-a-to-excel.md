---
title: Export questionnaire responses to a spreadsheet
description: Export received or returned questionnaires to Microsoft Excel spreadsheets. This option enables you to use the spreadsheet environment to review questions and answers.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Assess third-party risk, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Export questionnaire responses to a spreadsheet

Export received or returned questionnaires to Microsoft Excel spreadsheets. This option enables you to use the spreadsheet environment to review questions and answers.

## Before you begin

Role required: sn\_vdr\_risk\_asmt.vendor\_assessor

## About this task

You can export only questionnaires in the received or returned state.

**Note:** This is available when you’re using the Classic assessment engine.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Third-party risk management** &gt; **External risk assessments** &gt; **All open**.

2.  Select the External assessment \(VRA\) number of an assessment that is in the **Responses received** state.

3.  On the Risk overview tab, in the Questionnaires and document requests section, select the **Name** to open the questionnaire that you want and then fill in the questions.

    -   To export a single questionnaire:

        Select **View Responses** and then select **Export Responses**.

    -   To export more than one questionnaire:

        1.  Select the check boxes for the questionnaires that you want, then select **Export Questionnaire** from the **Actions on selected rows** list.
        2.  Select **Export**.
    -   To export all listed questionnaires:

        1.  Select **Export All**.
        2.  A pop-up lists the questionnaires to be exported.
        3.  Select **Export**.
        **Note:** Questionnaires in the received or returned state are available for exporting.

    The system generates a compressed file that contains a separate Excel file for each questionnaire. Exported files use the following file naming convention: `<assessmentName> - <questionnaireName>.xlsx`.

    The **Assessment details** tab in a spreadsheet shows the name and state of the assessment, the planned and completion dates, and signatory details. Each **Section** tab displays the question data for the assessment categories.


