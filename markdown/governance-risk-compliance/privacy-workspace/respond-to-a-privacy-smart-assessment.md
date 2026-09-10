---
title: Respond to privacy impact assessment
description: Respond to an impact assessment from the Assessment Workspace. The assessment results help to understand the potential privacy risks and their mitigation measures.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/respond-to-a-privacy-smart-assessment.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Respond to privacy impact assessment

Respond to an impact assessment from the Assessment Workspace. The assessment results help to understand the potential privacy risks and their mitigation measures.

## Before you begin

Role required: sn\_privacy.business\_user

## About this task

A screening assessment is the first assessment that is sent to any responder to determine if the privacy teams need to be aware of any application that processes personal data. If there is personal data involved, then an impact assessment is sent to the key stakeholders. While the screening assessment only has the **General** section for questions, the impact assessment has two sections: **Personal data** and **Questionnaire**. Under the Personal data section, you find the following sections:

-   **Data elements**: This section displays the information object categories and each information object that belongs to that category. Based on your selection during template configuration, you can view either all information object categories or only the selected ones.
-   **Data subjects types**: In this section, you add the data subjects types whose personal data is involved in the processing activity.
-   **Hierarchy**: In this section, you specify the source and the destination of data. By adding new relationships to a hierarchy, you define how data flows across related entities and their corresponding locations.
-   **Legal basis**: In this section, you specify the lawful basis on which the data is processed. For example, an information is processed for legal obligations. Specify the granular levels of the create, read, update, delete operations that can be performed on the data and also where the data is coming from and where its being sent.

Because the assessments use the Smart Assessment Engine, the responders can see the detailed description of each question and the guidance that helps the responder in answering the questions.

## Procedure

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.

2.  On the Employee Center home page, select **GRC tasks**.

3.  Navigate to **Tasks** &gt; **My pending tasks** &gt; **Privacy assessments**.

4.  Select the privacy impact assessment you want to take.

    The assessment opens in the Assessment Workspace.

5.  To take the assessment, select **Start**.

6.  To reassign the assessment, select **Reassign**.

    You can only reassign the assessment to a user who has the privilege to respond to an assessment and is a key stakeholder. For more information, see [Add key stakeholders to a processing activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/add-stakeholders-to-a-pa.md).

7.  On the **Personal data** section, provide the responses for the following sections.

    1.  In the **Data elements** section, select all applicable data elements, then select **Next**.

    2.  In the **Data subject types** section, add impacted data subjects types.

        Only the data subjects you add here are available for selection while creating a new hierarchy relationship. For steps, see [Add data subject type to privacy impact assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/add-data-subject-type-to-pia.md).

    3.  In the **Hierarchy** section, create new relationships.

        For detailed description of the relationship forms, see [New hierarchy relationship forms in Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/new-relationship-forms.md).

    4.  In the **Legal basis** section, specify the lawful basis on which the data is processed.

8.  Select **Move to questionnaire**, and fill in your responses.

9.  Select **Submit**.

10. On the Submit dialog box, mark your confirmation, and select **Submit**.

11. To view your responses after submission, on the assessment page, select **View**.


## Result

After an assessment is submitted, the privacy team receives a notification about the assessment submission. The team can then choose to either act on it or reject it based on their analysis. To understand analyst actions on a privacy assessment, see [Review a privacy assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/review-a-privacy-assessment.md).

**Parent Topic:**[Using Privacy Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/using-privacy-mgmt.md)

