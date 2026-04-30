---
title: Review responses and perform inherent risk assessment
description: Compute the overall risk score for an application by performing an advanced risk assessment. After the IT application owner responds to the questionnaire, a risk manager reviews the responses and performs the inherent assessment.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Application risk assessment using Advanced Risk Assessment, Integrate, Risk Management, Governance, Risk, and Compliance]
---

# Review responses and perform inherent risk assessment

Compute the overall risk score for an application by performing an advanced risk assessment. After the IT application owner responds to the questionnaire, a risk manager reviews the responses and performs the inherent assessment.

## Before you begin

Role required: sn\_risk.manager

## About this task

After the risk assessor returns the assessment questionnaire, you can review the questionnaire as the risk manager. Based on your review, you can initiate a risk assessment for the application.

The risk assessment task is initiated to the group responsible for performing the assessment. The task is available in **My Group Tasks**. Any risk manager who is a part of the group can perform the assessment. The assessors usually don't vary.

You can choose to use either the manual factors or the automated factors. By default, there are three manual factors which are associated to a risk assessment methodology. There are also three automated factors which are not associated to any risk assessment methodology. The names of the factors are:

-   Confidentiality Impact
-   Integrity Impact
-   Availability Impact

Some of the factors or questions on the risk assessment instance might already have an answer or a response. These values are derived from the responses of the application owner. You can view how the value was calculated.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Risk Identification** &gt; **All**.

2.  Open the record with the assessment that you must review.

3.  In the Questionnaires related list, click **View responses** for the required assessment.

    1.  If you are not satisfied with the responses provided in the questionnaire, click **Reject Questionnaire**.

        The respondent receives an email and is asked to resubmit the questionnaire.

    2.  If you're satisfied with the responses provided by the application owner, then perform the inherent assessment by clicking **Perform Inherent Assessment**.

        The risk assessment instance link is created.

    To understand the risk assessment process and how to respond to questions, refer to [Understanding the risk assessment instance](../concept/understanding-risk-assessment-instance.md).

4.  Click the risk assessment instance link that is generated.

5.  Respond to the questions or manual factors.

6.  Right-click and save the form.

7.  Click **Request Approval**.


## Result

The approver selected in the Risk Identification Configuration form can review the inherent assessment. The state on the Risk Identification form is moved to the Risk Mapping state.

## What to do next

[Associate risks, citations, policies, and controls with a risk identification record](associate-risks-pols-citations-risk-idenfn.md).

**Parent Topic:**[Application risk assessment using Advanced Risk Assessment](../concept/risk-and-apm-better-together.md)

