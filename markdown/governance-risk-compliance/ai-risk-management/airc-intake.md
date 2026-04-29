---
title: Intake requests
description: Intake requests are the entry point for managing and governing AI initiatives. They capture essential information about proposed AI systems, models, and datasets so that requests can be reviewed, triaged, and evaluated early in the AI life cycle.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
keywords: [AI intake, AI governance, AI risk classification, AI system, AI model, AI dataset]
breadcrumb: [AI governance life cycle, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Intake requests

Intake requests are the entry point for managing and governing AI initiatives. They capture essential information about proposed AI systems, models, and datasets so that requests can be reviewed, triaged, and evaluated early in the AI life cycle.

## Intake request overview

Intake requests are used to capture AI-related needs and concerns in a structured way. They help organizations understand what AI is being proposed, how it’s intended to be used, and what risk or compliance considerations may apply.

Submitting an intake request supports the creation of AI asset records that can be tracked in the AI Control Tower and evaluated using AI Risk and Compliance workflows as part of the AI governance life cycle. Intake can support early screening and initial risk-based classification, but doesn’t automatically approve or govern an AI asset.

## Request an AI use case

Use this intake request to propose a new or changed AI system that addresses a business problem. AI use case requests focus on the overall purpose, scope, and intended outcome of the AI capability.

After upgrading to version 22.0.3, if you have the AI risk and compliance user \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] role, you can support configurable risk‑based classification of AI systems at intake where this capability is enabled.

**Note:**

Risk‑based classification at intake occurs only when all required configuration steps are completed by a teammate with the AI Risk and Compliance Admin \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_admin\] role.

-   Set the Migrate to Advanced Risk Assessments property to publish Risk Assessment Methodologies \(RAMs\). For more information, see [Set up Advanced Risk assessments properties](../task/advanced-risk-assessments-properties-airc.md).
-   Publish assessment templates. For more information, see [Publish the assessment templates](../task/publish-the-assessment-templates.md).
-   Configure the `sn_grc_ai_gov.ai_system_automated_risk_classification_asmt_ram` to specify a default Risk Assessment Methodology \(RAM\) used for automated regulatory risk classification of AI systems at intake. For more information, see [Set up AI Risk and Compliance properties](../task/configure-airc-properties.md).
-   Configure the `sn_grc_ai_gov.aisystem_primary_ram` property to specify a default Risk Assessment Methodology \(RAM\) for AI systems. For more information, see [Set up AI Risk and Compliance properties](../task/configure-airc-properties.md).

If these prerequisites aren’t met, intake submissions are accepted but risk classification isn’t performed and the risk classification defaults to **To Be Determined**. After the AI asset is managed by an AI Steward, the Automated Risk Classification is performed to pre-classify as High/ Medium/ Low/Unacceptable.

Risk-based classification at intake provides an initial screening of AI systems based on how they’re intended to be used. This early classification helps organizations capture AI risk context at the start of the life cycle and determine the level of governance attention required.

Classification is derived from responses to screening questions in the **Use and purpose** section of the intake form and is evaluated using a configured Risk Assessment Methodology \(RAM\). The resulting classification \(for example, **Low**, **Medium**, **High**, **Unacceptable**, or **To Be Determined**\) is recorded on the AI system and used to guide downstream governance workflows.

Risk classification is re-evaluated automatically when Use and Purpose responses are updated. Changes to factors such as data sensitivity, system autonomy, or level of human involvement can result in an updated classification, which is captured in the activity history for audit purposes.

The Use and Purpose section is automatically enabled when risk-based classification at intake is configured. This section is delivered as part of the product and doesn’t require manual form customization or a separate enablement setting.

Submitting an AI use case request can result in an AI system record being created through configured intake and onboarding workflows. Once created, the AI system can be reviewed, risk-classified, and assessed as part of the broader AI governance life cycle.

**Note:**

Risk-based classification at intake provides early screening only. Risk Rating is evaluated for those AI system requests explicitly Managed by an AI steward \[sn\_ai\_governance.ai\_steward\]. It doesn’t approve deployment, initiate life-cycle workflows, or replace impact assessments, detailed risk assessments, or control evaluations.

For more information, see [Request an AI use case](../task/request-ai-system.md), [Request an AI use case form](../reference/request-ai-system-form.md), and [AI systems](ai-system-airc.md).

## Request an AI model

Use this intake request when the primary focus is on an AI model rather than a complete AI system. This intake request includes proposing the development, procurement, or onboarding of a specific model.

AI model requests capture model-specific details needed for review, such as intended usage, versioning, and risk considerations.

For more information, see [Request an AI model](../task/request-ai-model.md), [Request an AI model form](../reference/request-ai-model-form.md), and [AI models](ai-model-airc.md).

## Request a dataset

Use this intake request to request access to a dataset for purposes such as analysis, model training, or evaluation.

Dataset requests help ensure that data usage is reviewed before it’s used in AI-related activities.

For more information, see [Request a dataset](../task/request-dataset.md), [Request a dataset form](../reference/request-dataset-form.md), and [Datasets](dataset-airc.md).

## Intake request example: Email Assistant AI Agent for corporate communications

This example explains how an organization might use an intake request to propose and evaluate an AI use case.

A corporate IT team proposes an Email Assistant AI Agent to support internal business users with drafting, summarizing, and responding to work‑related emails. The AI agent is intended to improve productivity by generating suggested email responses, summarizing long email threads, and highlighting required actions for employees.

To initiate governance review, a team member, such as AI Product Owner, Use Case Submitter or Product Innovator from the Corporate Communication Business Unit submits a **Request an AI use case** intake request through the Employee Center. The intake captures key information, including:

-   The business purpose of the AI agent, such as improving response time and reducing manual effort in corporate communications.
-   The intended users, for example, employees using corporate email systems.
-   The types of data processed, including internal emails that may contain business‑sensitive or confidential information.
-   The level of automation, such as whether the AI generates suggestions only or can send emails automatically.
-   The role of human oversight, including employee review and approval of AI‑generated content before sending.

Based on responses in the **Use and purpose** section, the intake workflow performs an initial risk‑based classification. Factors such as data sensitivity, exposure to personal or confidential information, and the degree of human involvement contribute to the preliminary classification.

The resulting classification is recorded on the AI system and used to determine next governance steps, such as whether additional risk assessments, legal review, or security evaluations are required before deployment.

