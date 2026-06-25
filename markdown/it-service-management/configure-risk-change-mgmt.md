---
title: Configure risk for Simplified Change Management
description: Set up risk assessment questions, scoring thresholds, and risk levels so that the system can automatically evaluate the risk of a proposed change and route it to the appropriate approval workflow. Configuring risk helps your organization make consistent, data-driven decisions about change requests without requiring ITIL expertise.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/configure-risk-change-mgmt.html
release: australia
topic_type: task
last_updated: "2025-05-04"
reading_time_minutes: 3
keywords: [change management, risk configuration, risk assessment, risk scoring, change risk, admin experience, configuration console]
breadcrumb: [Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Configure risk for Simplified Change Management

Set up risk assessment questions, scoring thresholds, and risk levels so that the system can automatically evaluate the risk of a proposed change and route it to the appropriate approval workflow. Configuring risk helps your organization make consistent, data-driven decisions about change requests without requiring ITIL expertise.

## Before you begin

Role required: sn\_itsm\_chg\_admin.risk\_config

## About this task

Risk assessment works by presenting a short survey to the change requester when a change request is submitted. Each answer carries a score, and the total score maps to the risk levels - Low, Moderate, or High. The system then automatically routes the change to the matching approval workflow based on the risk level.

Risk configuration has two main parts:

-   Risk assessment questions: Survey questions that determine the risk score for a change.
-   Score thresholds: Score boundaries that map a cumulative score to a risk level \(Low, Moderate, or High\).

## Procedure

1.  From the header of your ServiceNow instance, navigate to **All** &gt; **Admin Home**.

2.  From the **Manage your products** section, select **View product overview** for IT Service Management.

3.  On the Product Hub page for IT Service Management, from the Configure your product section, select **Configure**.

4.  On the Configuration Console, from the left navigation panel, select **ITSM fulfiller experience &gt; Change Management &gt; Risk configuration**. \[Omitted image "simplified-change-risk.png"\] Alt text: Change risk configuration page

5.  Review the existing risk assessment questions in the Risk Assessment Questions table.

    The table displays the following columns for each question:

    -   Question: Survey question text.
    -   Order: Sequence in which the question appears in the survey.
    -   Data type: Response type \(for example, Single select\).
    -   Active: Indicates whether the question is currently included in the survey.

        **Note:** You can double-click on a cell of the Active column and set the value for a question to **false** to disable the question.

    The system provides eight pre-seeded questions by default. You can activate, deactivate, or add questions as needed.

6.  To add a new risk assessment question, select **New** in the Risk Assessment Questions section.

    1.  On the Question: page, enter the survey question in plain language in the **Question text** field.

        Write the question clearly and specifically. For example: "Does this change affect a business-critical application or service?"

        **Note:** The **Set as active** option is enabled by default for the question.

    2.  In the Response type options section, enter the response text and corresponding score for each answer option.

        To add more response options, select **+ Add response**. Each response must have both a **Response** label and a **Score** value.

    3.  Select the **Mandatory** option if the requester must answer this question before submitting the risk assessment.

    4.  In the **Order** field, specify the position of this question in the survey sequence.

        Questions are sorted in ascending order. The default value for a new question is the value next to the question having the highest order value. To insert the question earlier in the survey, enter a lower order value.

    5.  Select **Save** to save the new question.

7.  Review the score ranges in the What are the score ranges that define the risk level? section.

    The default score ranges are:

    -   0 to 25 — Low risk
    -   26 to 50 — Moderate risk
    -   51 and above — High risk
8.  In the Adjust thresholds section, modify the score boundaries for the Moderate and High risk levels.

    Enter a numeric value in the **Moderate risk threshold** and **High risk threshold** fields to adjust where each risk level begins. The score ranges update automatically to reflect the new boundaries.

    **Note:**

    The Moderate risk threshold must be less than the High risk threshold.

9.  Select **Save** to save all risk configuration changes.

10. When you have finished configuring, select **Mark as configured** to save your settings and mark this step as complete.

    To revert changes made in the current session before saving, select **Undo**.

    As an alternative to the form-based wizard, you can also complete this configuration through the **Configure with Now Assist** conversational flow, accessible from the banner at the top of the page.


## Result

Risk assessment is now configured. When a change requester submits a change request, the system presents the active risk assessment questions, calculates a cumulative score from the responses, and automatically maps the score to a risk level. The change is then routed to the appropriate approval workflow based on that risk level.

**Parent Topic:**[Configuring Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configuring-change-management-experience-in-it-service-management.md)

**Related topics**  


[Risk assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/c_RskAsmtCalc.md)

