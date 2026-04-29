---
title: Using a Microsoft Excel spreadsheet template for external questionnaires
description: Third parties and engagements can use a Microsoft Excel spreadsheet to respond to questionnaires by downloading the template, completing it, and importing the final version into the Third-party portal. This enables respondents to provide information outside the third-party portal.
locale: en-US
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Manage the third-party portal, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Using a Microsoft Excel spreadsheet template for external questionnaires

Third parties and engagements can use a Microsoft Excel spreadsheet to respond to questionnaires by downloading the template, completing it, and importing the final version into the Third-party portal. This enables respondents to provide information outside the third-party portal.

## Downloading the questionnaire template

You can access the questionnaire template through the Vendor Management Workspace, Classic user interface, or through the third-party portal.

If you have the Third-party risk \(TPR\) assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] or TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] role, you can download the questionnaire template by navigating to the questionnaire you want and selecting **View responses**. For more information on the questionnaire template process, see [Respond using a Microsoft Excel template](../task/tprm-tpcontact-use-excel.md).

To view a questionnaire using the Classic user interface, select **All** &gt; **Self-Service** &gt; **Third-party risk management** &gt; **External risk assessments** &gt; **All open**, select the assessment you want, and then select **View responses** next to the questionnaire you want in the Questionnaire related list. After the questionnaire page has opened, select the Download Excel template link.

To view a questionnaire using the Vendor Management Workspace, select **Workspaces** &gt; **Vendor Management Workspace**, select the list icon ![](../image/icon-tprm-ws-list.png) and then navigate to **External risk assessments**. After choosing the assessment you want, navigate to the Questionnaires and document requests section of the Risk overview tab and select the questionnaire you want. After the questionnaire page has opened, select the Download Excel template link.

**Note:** As TPR assessor or TPR manager you can submit a questionnaire after completing this process on behalf of a third party or engagement contact if the **Allow assessors to answer/edit questionnaires for third-party contacts** property \(**sn\_svdp.allow\_assessor\_edit**\) is active. For more information on configuring this property and responding to questionnaires, see [Configure TPRM properties](../../grc-vendor-risk-implementation/task/tprm-properties-configure.md), [Respond to a questionnaire for a third party or engagement](../../grc-vendor-risk/task/tprm-respond-for-tp.md), and [Review responses to external questionnaires](../task/tprm-ws-assessment-rvw-response.md).

The following example shows the questionnaire page.

![View of a sample questionnaire page. For the text description, refer to the text that precedes and follows this example.](../../grc-vendor-risk/image/import-q-view.png "Sample questionnaire example")

**Important:** The questionnaire template is downloaded in the .xlsx format and after being completed must be uploaded in the same format.

## Completing the questionnaire template

You can view the instructions for filling out the template by navigating to the **Instructions** tab in the questionnaire template file. To add question data for each section of the questionnaire, go to the corresponding tab. Each tab is named after its section and contains the relevant question data.

**Important:** You must follow the instructions for each question type and column entry. Entries in the Question Details, Depends on, and Required when columns must match the tag, question name, or action being referenced. Validation for the questionnaire template is limited.

## Importing the questionnaire template

Import a completed questionnaire by selecting Import and then selecting the file from your file browser. A dialog box shows the progress status for your questionnaire template as answers are imported. After the import is complete, you can review the results and select **Copy** to copy the import log to your clipboard if applicable. Review the import log and correct any errors before attempting to upload the updated template.

The following example shows the dialog box and import log.

![View of an import log. For the text description, refer to the text that precedes this example.](../../grc-vendor-risk/image/import-log.png "Import log example")

## Limitations

The questionnaire template has the following limitations and requirements.

-   Don’t modify the structure or formatting of the document; only make selections or enter content as instructed.
-   Not all question types have validation, so some of your responses might not be checked for correctness or completeness.
-   Answer all mandatory questions; leaving them unanswered can result in an incomplete submission.
-   Complete certain question types, including Attachment, Reference, Image Scale, and Template, in the ServiceNow instance or with the help of a third-party representative, as the template doesn’t support them.
-   Rich text formatting \(for example, HTML tags such as &lt;b&gt; or &lt;p&gt;\) is not supported when importing questionnaire responses from an Excel file. Use plain text only.
-   Follow the additional conditions specified in the Required When column for conditional questions, which depend on your answers to previous questions, as indicated in the Depends On column.
-   Review the Question Details column carefully, as it provides additional context or information about the questions.
-   Disable any filters in the questionnaire template to help ensure you see and answer all questions, as filters can hide questions.
-   Avoid modifying or distributing the document without authorization, as this violates the copyright agreement and can result in penalties for you or your organization.

For more information about questionnaire template requirements, see the **Instructions** tab in the questionnaire template file.

For instructions that you can send to third-party contacts, see [Respond using a Microsoft Excel template](../task/tprm-tpcontact-use-excel.md).

**Note:** Due to license restrictions, you can’t download Shared Assessments Standardized Information Gathering \(SIG\) questionnaire templates. For more information about using SIG questionnaires, see [Using the SIG questionnaire for a risk assessment](../../grc-vendor-risk/concept/tprm-sig-use-and-support.md).

