---
title: Request an AI use case
description: Request the development or procurement of an AI system to initiate and document the need for an AI‑driven solution within an organization. This process helps ensure that AI implementations are aligned with business goals, compliant with regulations, and technically feasible.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Request an AI use case

Request the development or procurement of an AI system to initiate and document the need for an AI‑driven solution within an organization. This process helps ensure that AI implementations are aligned with business goals, compliant with regulations, and technically feasible.

## Before you begin

Role required: sn\_ai\_case\_mgmt.ai\_case\_business\_user \(Employee Center\), sn\_ai\_asset\_mgmt.ai\_asset\_owner \(AI Control Tower dashboard\)

To classify AI systems using a risk‑based approach at intake, a teammate with the AI Risk and Compliance Admin \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\] role must complete the following.

-   Set the Migrate to Advanced Risk Assessments property to publish Risk Assessment Methodologies \(RAMs\). For more information, see [Set up Advanced Risk assessments properties](advanced-risk-assessments-properties-airc.md).
-   Publish assessment templates. For more information, see [Publish the assessment templates](publish-the-assessment-templates.md).
-   Configure the `sn_grc_ai_gov.ai_system_automated_risk_classification_asmt_ram` to specify a default Risk Assessment Methodology \(RAM\) used for automated regulatory risk classification of AI systems at intake. For more information, see [Set up AI Risk and Compliance properties](configure-airc-properties.md).
-   Configure the `sn_grc_ai_gov.aisystem_primary_ram` property to specify a default Risk Assessment Methodology \(RAM\) for AI systems. For more information, see [Set up AI Risk and Compliance properties](configure-airc-properties.md).

**Note:**

If these prerequisites aren’t met, intake submissions are accepted but risk classification isn’t performed.

## About this task

If you’re using the AI Risk and Compliance \(AIRC\) application, you submit requests through the Employee Center and related tasks such as impact assessments and review tasks \(for example, legal, security, and architecture\). If you’re using the AI Control Tower \(AICT\) application, you can submit requests from the AI Control Tower dashboard and manage AI assets through AICT’s inventory and life cycle experience.

For more information on the end‑to‑end life cycle, see [AI governance life cycle](../concept/ai-gov-lifecycle.md).

The Request an AI system feature enables you to initiate requests for the development or procurement of AI‑based solutions. Whether you need a custom AI model, an automation tool, or an advanced analytics system, the platform streamlines the process by capturing key requirements and facilitating approvals.

For example, a financial institution wants to improve its loan approval process by implementing an AI‑based credit scoring system. The finance team submits an AI request detailing requirements such as risk assessment considerations, credit data analysis, and automated decision‑making. The request is reviewed for feasibility, budget, and compliance before development or procurement proceeds.

## Procedure

1.  Request an AI system from the Employee Center or from the AI Control Tower dashboard.

<table id="choicetable_afh_4hk_23c"><thead><tr><th align="left" id="d109665e178">

Option

</th><th align="left" id="d109665e181">

Description

</th></tr></thead><tbody><tr><td id="d109665e187">

**Request an AI system using AI Risk and Compliance**

</td><td>

Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**. 1.  Select **Help center** &gt; **Technology services** and then select **AI assets** from the Technology services topics section.
2.  Select the **Request an AI use case** card.
**Note:** AI Risk and Compliance Business User and AI Asset owner can complete this option.

</td></tr><tr><td id="d109665e237">

**Request an AI system using AI Control Tower**

</td><td>

Navigate to **All** &gt; **AI Control Tower**. 1.  On the AI Control Tower dashboard, select the list icon ![](../image/list-icon-airc-ws.png), and navigate to the **AI asset inventory - Managed** or **AI asset inventory - Unmanaged**
2.  Select **AI systems**, then select **Add AI system**.
**Note:** An AI Asset owner can complete this option.

</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    For full descriptions of the fields, see [Request an AI use case form](../reference/request-ai-system-form.md). For more information about adding an AI system using AI Control Tower, see [Create AI system assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/create-ai-system-assets.md).

3.  To add attachments, select **Add attachments**.

4.  To save the form as a draft and edit it later, select **Save as Draft**.

5.  Select **Submit**.

    After submission, the appropriate AI governance stakeholders \(such as AI Stewards or AI Center of Excellence teams, depending on configuration\) review the request and guide you through the next steps.


## What to do next

After submitting an AI use case request, next steps vary depending on your role.

AI Product Owner or Requester \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_user\]: Provide additional information as requested during intake and onboarding, including details about the AI system, related models, datasets, and intended business outcomes. You may be asked to complete impact assessment questionnaires and support reviews as the AI system progresses through assessment and validation.

For more information, see [Perform impact assessment on an AI use case](perform-impact-assessment-of-ai-use-case.md).

AI Steward or AI Center of Excellence \(AI CoE\) \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager, sn\_ai\_asset\_mgmt.ai\_asset\_owner\]: Review submitted requests for business and strategy alignment, initiate required assessments, and coordinate cross‑functional reviews. Continue to oversee the AI system through its life cycle, including inventory tracking, governance activities, and collaboration across stakeholders.

For more information, see [AI Control Tower dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-governance.md).

Risk and Compliance Manager \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\]: Assess the AI system for regulatory, policy, and risk considerations. Assign risk assessments, recommend controls and attestations, and monitor compliance throughout the AI system life cycle.

For more information, see [AI Risk and Compliance workspace](../concept/ai-risk-and-compliance-workspace.md), [Initiate AI assessment on an AI asset](initiate-assessment-on-an-ai-asset.md), [Initiate risk assessment on AI asset](initiate-risk-assessment-on-ai-systems.md), [Initiate risk assessment on AI asset's risks](request-risk-assessments-for-ai-systems.md), and [Manage controls using AI Risk and Compliance](../concept/manage-controls-in-airc.md).

For an overview of how AI systems move from intake through assessment, deployment, monitoring, and value tracking, see [AI governance life cycle](../concept/ai-gov-lifecycle.md).

-   **[Request an AI use case form](../reference/request-ai-system-form.md)**  
The Request an AI use case form is designed to streamline the request process for developing or procuring an AI-based solution. This intake form confirms that all necessary details, supporting documents, and compliance considerations are captured before moving forward with development and deployment of the AI-solution.

**Parent Topic:**[Using AI Risk and Compliance](../concept/using-ai-risk-and-compliance.md)

