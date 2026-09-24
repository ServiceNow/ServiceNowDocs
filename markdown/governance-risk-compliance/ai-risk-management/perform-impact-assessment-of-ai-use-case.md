---
title: Perform impact assessment on an AI use case
description: Perform an impact assessment of an AI use case to identify risks like copyright issues, bias, privacy breaches, misinformation, or surveillance, enabling improved oversight and risk management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/perform-impact-assessment-of-ai-use-case.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [impact assessment, FRIA, use and purpose, pre-populated]
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Perform impact assessment on an AI use case

Perform an impact assessment of an AI use case to identify risks like copyright issues, bias, privacy breaches, misinformation, or surveillance, enabling improved oversight and risk management.

## Before you begin

Role required: sn\_ai\_asset\_mgmt.ai\_asset\_owner or sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user

## About this task

The impact assessment template includes Use and purpose questions that evaluate the AI system's intended outcomes, affected populations, level of autonomy, and data usage. When Use and purpose information is captured during AI system intake, those responses are carried forward into the relevant impact assessment questions. Review the populated answers before submitting the assessment and update them if the information has changed.

**Note:**

The ServiceNow Risk products help customers address regulatory requirements under various jurisdictions. However, we do not guarantee compliance and customers are ultimately responsible for their own compliance with applicable regulations.

ServiceNow aims to provide software updates for new or updated major regulations and requirements within twelve to eighteen months of the regulation's publication. For regulations for which ServiceNow provides a level of support in the base system, ServiceNow aims to provide software updates for minor regulatory changes within 12 months and for major regulatory changes within up to 18 months depending on scope and impact. We differentiate between typical regulatory content updates, which do not require software updates or enhancements, and regulatory updates, which do require software updates or enhancements. Content updates are generally delivered on a shorter cadence than if software update or enhancement is required for the regulatory update or change.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower**.

2.  On the AI Control Tower dashboard, navigate to the Tasks section and select the assigned impact assessment task.

3.  Select **Take assessment**.

4.  To reassign the impact assessment to another user, select **Reassign** and do the following:

    1.  In the Reassign task dialog box, fill in the fields as appropriate.

        |Field|Description|
        |-----|-----------|
        |Assignee|Name of the user to whom you want to reassign the task.|
        |Additional comments|Additional information stating the reason for reassignment.|

    2.  Select **Reassign**.

5.  To initiate a sidebar discussion, select the more icon \[Omitted image "more-options.png"\] Alt text:, and select **Discuss**.

    1.  In the Start a Sidebar discussion dialog box, fill in the fields as appropriate.

<table id="table_pcl_lkb_11d"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subject

</td><td>

Option to provide a title for the sidebar discussion.

</td></tr><tr><td>

Add participants

</td><td>

Options to add participants for the sidebar discussion.**Note:** You can include any users with access to this record in this discussion.

</td></tr><tr><td>

Include a brief message for participants

</td><td>

Brief summary about the feedback to be discussed in the sidebar discussion.

</td></tr></tbody>
</table>    2.  Select **Start discussion**.

6.  To initiate the assessment, select **Start**.

7.  Review any instructions or reference information.

    You can see additional question guidance text for your review as you complete the questions.

8.  Answer all relevant questions in the questionnaire.

    Your responses are automatically saved, and based on them, relevant risk statements and control objectives are associated with the assessment. After the AI Risk and Compliance analyst marks the assessment state as Closed complete, risks and controls are generated from these risk statements and control objectives respectively and are mapped to the AI asset.

    **Note:** The system automatically maps risks and controls only when you use the default assessment questionnaire.

9.  Select **Submit**.

    The impact assessment is submitted for review. An AI Risk and Compliance analyst evaluates the completed assessment and the suggested list of risks and controls derived from your responses.


## Result

The impact assessment is submitted. The AI Risk and Compliance analyst receives the assessment in their task queue for review. After the analyst closes the assessment as **Closed complete**, risks and controls are automatically mapped to the AI asset based on the assessment responses.

## What to do next

After submitting the impact assessment, next steps vary depending on your role.

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] or AI Risk and Compliance Business User \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\]: Your task is complete. You may be contacted if the analyst needs additional information to complete their review.

AI Risk and Compliance analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]: Review the completed assessment in your task queue. Evaluate the responses and the suggested list of risks and controls. When your review is complete, close the assessment as **Closed complete** to trigger automatic mapping of risks and controls to the AI asset.

For more information, see [Initiate risk assessment on AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/initiate-risk-assessment-on-ai-systems.md).

**Parent Topic:**[Using AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/using-ai-risk-and-compliance.md)

**Related topics**  


[Intake requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-intake.md)

[Assessment templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-assessment-templates.md)

[Initiate risk assessment on AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/initiate-risk-assessment-on-ai-systems.md)

