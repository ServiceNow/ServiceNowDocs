---
title: VRM third-party risk tiering assessments
description: Organizations use risk tiering to classify their third parties into categories of potential risk posed at the time of onboarding. The standard predefined risk tiers are None, Low, Minor, Moderate, High, and Critical. Each risk tier has associated assessment questions and document requests.
locale: en-US
release: yokohama
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work in the VRM classic UI, Third-party Risk Management, Governance, Risk, and Compliance]
---

# VRM third-party risk tiering assessments

Organizations use risk tiering to classify their third parties into categories of potential risk posed at the time of onboarding. The standard predefined risk tiers are None, Low, Minor, Moderate, High, and Critical. Each risk tier has associated assessment questions and document requests.

## The more complete IRQ process replaces tiering

In the TPRM application, the IRQ is an internal questionnaire that improves the original tiering assessment process. IRQs enhance internal risk assessments with increased flexibility, control, and scalability. Unlike a tiering assessment where external questionnaires are determined solely by the risk tier, an IRQ can dynamically trigger external questionnaires based on both respondents' answers and risk tier.

To enable a seamless transition to TPRM, you have the option to duplicate existing tiering assessments and designate them as IRQ internal assessments. Risk tiering is supported as an unchanging legacy process.

## Legacy operation

1.  Most organizations import their third-party portfolio through a spreadsheet or an integration with another onboarding solution. Third-party risk \(TPR\) managers make ongoing updates to third-party information, including risk security scores and risk tiers.
2.  The TPR manager or TPR assessor determines the risk tier or categories of risk exposure for the third party.
3.  The TPR manager selects the third party, assigns the tiering questionnaire template, and assigns the internal assessor that is required to complete the assessment.

    ![Risk tiering assessment table relationship.](../../grc-vendor-risk/image/TieringAssessmentTableRelationship.png "Risk tiering assessment table relationship")

4.  Internal stakeholders navigate to **Self-service** &gt; **My Assessments and Surveys** to complete and submit the assessment.
5.  After the internal assessor has responded to the questionnaire, the system calculates the tiering score as the average of all scores. The TPR manager can initiate the risk assessment or a configured business rule can auto-send one. When the assessment is closed, the system assigns a risk tier to the third party based on the tiering score.

![Risk tiering assessment form.](../../grc-vendor-risk/image/VendorTierResponses.png "Risk tier calculation based on responses")

## Risk tiering scale and scoring calculations

![Risk tiering questionnaire and the risk tiering assessment, assessment instances, tiering score, and risk tier.](../../grc-vendor-risk/image/TieringScoreCalculations.png "Risk tiering process")

1.  The tiering assessment initiates an assessment instance for the assigned internal assessor.
2.  Response scores are averaged to generate the tiering score.
3.  The tiering score is mapped to risk tiers.
4.  The risk tier is assigned to the third party when the tiering assessment is closed.

