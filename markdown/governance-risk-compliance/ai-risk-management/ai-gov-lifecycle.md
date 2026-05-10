---
title: AI governance life cycle
description: Learn more about how organizations can govern AI from initial demand through deployment and ongoing governance monitoring by using the AI Control Tower and AI Risk and Compliance applications together.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 15
keywords: [AI governance, AI life cycle, AI Control Tower, AI Risk and Compliance]
breadcrumb: [Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI governance life cycle

Learn more about how organizations can govern AI from initial demand through deployment and ongoing governance monitoring by using the AI Control Tower and AI Risk and Compliance applications together.

## AI governance across the life cycle

Governing AI is a continuous process that spans the entire life cycle of an AI asset, from initial demand and intake through deployment, monitoring, and value realization. You can use the AI Control Tower \(AICT\) and AI Risk and Compliance \(AIRC\) applications together to support a coordinated approach to enterprise AI governance.

AICT provides centralized visibility and life cycle state management for AI initiatives across the organization. AIRC delivers risk, regulatory, and ethical governance capabilities that help organizations evaluate whether AI systems are developed and operated responsibly and ethically.

When a new AI system is introduced or an existing system is significantly updated and registered for governance, it enters a governed life cycle. This life cycle spans intake, assessment, build, review, deployment, and monitoring. Governance activities across this life cycle help organizations understand risk, apply appropriate controls, and make informed deployment decisions.

As part of this life cycle, AI systems typically undergo impact and risk assessments to evaluate regulatory exposure, ethical considerations, and operational risk. Assessment outcomes inform risk classification, required controls, and review routing. During development, governance focuses on control attestation, issue management, and policy exception handling from a risk and compliance perspective.

Before deployment, AI systems are reviewed to confirm that required assessments are complete. Open issues and policy exceptions must be resolved or formally accepted, and the system’s residual risk posture must be understood. Based on this review, the AI system may be approved for deployment, returned for remediation, or blocked from release.

After deployment, AI systems move into an operational monitoring phase. Ongoing governance monitoring helps maintain visibility into emerging risks, changes in usage, and evolving compliance requirements. Significant changes or incidents may require governance activities to reenter earlier life-cycle phases.

By applying consistent governance across the AI life cycle, organizations can centralize visibility into AI use and align AI initiatives with business strategy. This approach also helps organizations assess and manage risk for both in-house and third-party AI and support scalable deployment with continuous oversight.

Treating AICT and AIRC as a coordinated governance framework enables consistent oversight across all life cycle processes, from demand through value realization and life cycle closure.

In summary, you can use each application as follows:

-   AICT manages the AI life cycle and serves as the system of record.

    For more information, see [AI Control Tower Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-control-tower-home-page.md), [AI asset lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-asset-lifecycle.md), and [Exploring AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/exploring-ai-control-tower.md).

-   AIRC performs independent risk, regulatory, and control governance.
-   Life cycle progression in AICT depends on risk and compliance decisions made in AIRC.

    For more information about how this information is shown in AICT, see [Risk and compliance tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/risk-compliance-tab-aict.md).

-   Neither application replaces the other; together they support a coordinated governance framework.

**Note:** The AI governance life cycle is supported by a set of life-cycle tasks that are executed across AICT and AIRC. These tasks provide operational checkpoints that help ensure that governance, risk, and compliance obligations are addressed at the appropriate stage of the life cycle.

## AI governance roles and responsibilities

The AI governance life cycle involves distinct roles with clearly separated responsibilities across AICT and AIRC.

AI asset owners \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] \(also referred to as product owners\) are accountable for AI systems, models, and datasets as AI assets. They initiate intake and provide business context during assessment.

AI asset owners authorize deployment and retirement decisions. These decisions are subject to applicable risk and compliance approval. AI asset owners also own outcomes such as value realization and life cycle closure.

AI Risk and Compliance managers \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_manager\] provide independent risk and regulatory oversight. They initiate and oversee impact and risk assessments, determine risk classification, validate control implementation, and approve or block life cycle progression.

AI Risk and Compliance business users \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_business\_user\] and AI stewards \[sn\_ai\_governance\_ai\_steward\] execute governance activities. These roles contribute assessment inputs, perform assigned tasks such as control attestations, and support remediation and issue management. They also help keep inventory records accurate throughout the life cycle.

Other governance stakeholders, such as security, legal, privacy, or data governance teams, participate as needed. They contribute expertise during assessment, review, and investigation activities. These stakeholders don’t own life cycle decisions.

For more information about roles in AICT and AIRC, see [Roles installed with AI Risk and Compliance](../reference/roles-installed-with-ai-risk-and-compliance.md) and [AI Control Tower roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/roles-installed-with-ai-control-tower.md).

## AI governance life cycle phases and processes

These phases describe AI governance activities at a conceptual level and may span multiple workflow steps within AICT and AIRC.

-   **Demand: Intake or onboard**

    The life cycle begins with intake, where new AI use cases, enhancements, and ideas are submitted for governance. Intake establishes a centralized entry point to capture the purpose, scope, intended outcomes, and usage context of an AI system. This phase provides early visibility into AI demand, enabling organizations to identify potential risk, duplication, or misalignment before development begins.

    Any team member with the AI asset owners, AI steward, or AIRC business roles can submit intake-related information with an intake request using the Employee Center to determine whether an AI initiative should enter the governed life cycle based on its intent, scope, and organizational alignment. If you have the AI asset owner or AI steward role, you can review and progress intake requests using the AI Control Tower Workspace after they are submitted through the Employee Center.

    For more information about intake requests in AIRC and AICT, see [Intake requests](airc-intake.md), [Request an AI use case](../task/request-ai-system.md), [Request an AI model](../task/request-ai-model.md), and [Request a dataset](../task/request-dataset.md).

    During intake, the following are created or required: an AI intake request, an initial AI system record, and business context for the AI initiative.

    All AI use-case intake, including both in-house and third-party AI use cases, is life cycle-managed in the AI Control Tower application. AI Control Tower is required to register AI systems and use cases that must enter the governed AI life cycle and acts as the system of record for life-cycle tracking and portfolio visibility.

    AIRC doesn’t own AI use-case intake. If you have AIRC, you can participate after intake by contributing risk and compliance governance context, such as impact assessments and regulatory evaluation, once an AI use case has been registered in AICT.

    Use the Employee Center to request an AI use case for review, or use AICT to add an AI asset directly as part of approved onboarding by a fulfiller. For more information, see [Create AI system assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/create-ai-system-assets.md), [Create an AI case in the AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/create-ai-case-in-the-ai-control-tower.md), [Create AI model assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/create-ai-model-assets.md), [Create prompt assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/create-prompt-assets.md), and [Create dataset assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/create-dataset-assets.md).

    Enhancement requests, ideas, and feedback can be submitted and managed if Strategic Portfolio Management is installed. Enhancement requests, ideas, and feedback don’t enter the AI governance life cycle through AICT or AIRC. For more information about Strategic Portfolio Management, see [Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/r_ITBusinessManagement.md).

    **Note:**

    An intake request represents a proposal to introduce or govern an AI use case. Submitting an intake request doesn’t create or deploy an AI asset. After intake review, AI systems, models, and datasets can be registered in AICT as part of approved onboarding and life cycle initiation. AI system or model categories selected during intake \(such as Agentic or Generative\) provide descriptive context only. Life cycle progression, assessment requirements, and governance decisions are driven by risk classification, assessment outcomes, and configured governance rules, not by category selection.

    AI asset inventory and discovery is a life cycle-wide capability that begins during the Demand phase and persists across all stages of the governed AI life cycle. As part of intake and approved onboarding, AI systems, models, datasets, prompts, and related artifacts are registered or discovered and recorded in a centralized AI inventory.

    The AI asset inventory provides an authoritative view of AI assets across the enterprise, including internally developed and third-party AI. Inventory records persist from intake through deployment and retirement, enabling traceability, visibility, and governance as assets progress through life-cycle workflows.

    AI assets can be added to the inventory through manual registration during intake and onboarding, as well as through automated discovery using configured integrations with supported cloud and third-party platforms. Discovered assets and relationships are reviewed and completed by AI asset owners and AI stewards to help ensure inventory accuracy and governance readiness.

    AICT owns and manages the AI asset inventory and acts as the system of record for AI asset records, relationships, and life cycle state. AIRC consumes inventory data for downstream governance activities such as impact assessments, risk classification, control evaluation, and regulatory reporting, but doesn’t create or own inventory records.

    **Note:**

    Automated discovery requires configuration of supported integrations. For more information about enterprise AI discovery and automated inventory ingestion, see [Enterprise AI discovery: Unlock Visibility, Governance &amp; Value](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/enterprise-ai-discovery.md) and [AI connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-discovery-setup.md).

-   **Build and validate: Assess**

    During this phase, governance activities are executed through life cycle playbooks. Playbooks are attached to AI asset records in AICT and define required assessment tasks, approvals, and handoffs across governance roles. Life cycle playbooks coordinate required tasks and handoffs across the AICT and AIRC applications.

    Life cycle playbooks guide the following roles through the assessment process:

    AI stewards initiate and manage the assessment phase in AICT by starting life cycle reviews, assigning playbook tasks, and monitoring overall life cycle progression across AI systems.

    AI asset owners provide system details and business context in AICT, and complete required assessments \(such as impact or risk assessments\) using information captured in the AI asset inventory.

    AIRC analysts perform governance evaluations in AIRC. These evaluations include regulatory impact assessments, risk classification, and identification of required controls based on system and business information from AICT.

    AIRC managers review assessment outcomes in AIRC, determine whether identified risks are acceptable, and approve required controls or mitigations before the AI system can advance in the life cycle.

    Throughout the assessment phase, AICT coordinates task execution, approvals, and status transitions between AICT and AIRC, providing visibility into whether required assessments are completed before life cycle progression.

    During assessment, the following are created or updated: impact assessment results, risk classification, identified risks, and recommended controls. These outcomes determine whether the AI system can proceed to the next life cycle phase.

    For more information, see [Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/playbooks.md), [Perform impact assessment on an AI use case](../task/perform-impact-assessment-of-ai-use-case.md), and [Perform risk assessments on AI systems](../task/perform-risk-assessments-on-ai-systems.md).

-   **Build and validate: Build and test**

    The build and test phase applies governance during development by helping ensure that risks identified during assessment are addressed through defined controls, remediation activities, and validation steps.

    Playbooks continue to guide remediation, control attestation, and evidence collection activities during build and test, with life cycle progression dependent on completion of required governance tasks.

    AICT continues to manage life cycle state and track governance progress. AIRC validates that required controls are implemented and that issues or exceptions are documented and addressed throughout the life cycle.

    AI asset owners and development teams implement required controls and remediation activities. AIRC business users and analysts review control attestations and submitted evidence to validate that required controls are implemented and operating as intended.

    Control attestations may occur at multiple stages of the life cycle, including during assessment, build and validation, and offboarding. Completion of control attestations contributes to governance readiness but doesn’t on its own approve deployment.

    AIRC managers verify that required controls and remediation actions are implemented and effective.

    During validation, the following records are created or updated: Control attestations, issue records, remediation evidence, and exception records.

    For more information, see [Manage controls using AI Risk and Compliance](manage-controls-in-airc.md), [Create control attestations for AI asset](../task/attest-controls-for-ai-systems.md), and [Remediate an issue in AI Risk and Compliance](../task/remediate-an-issue-in-airc.md).

-   **Build and validate: Pre-deployment review**

    Before deployment, AI systems undergo pre-deployment review to confirm that required assessments are complete, high-priority issues and exceptions are addressed, and residual risk is understood and documented.

    AICT manages the pre-deployment life cycle gate. AIRC performs a final governance review to determine deployment readiness based on risk posture, control implementation, and residual risk.

    During pre-deployment review, playbooks show governance readiness by displaying assessment completion, control status, open issues, and documented residual risk. Playbooks don’t approve deployment. Approval or rejection decisions are made by AIRC managers and reflected in the life cycle state managed by AICT.

    AIRC managers approve or block deployment based on governance readiness and residual risk.

    Governance decisions are made in AIRC, while life cycle state changes are recorded and enforced in AICT.

    For more information, see [Overview tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/overview-tab-in-ai-control-tower.md) and [Risk &amp; compliance tab](risk-and-compliance-tab-airc.md).

-   **Deploy, monitor, and assess value: Monitor**

    After deployment, governance activities monitor AI systems for reported events, operational changes, and governance signals. These activities support effective risk management and responsiveness to emerging risks through assessments, reviews, and regulatory updates. Continuous monitoring helps organizations identify emerging risks early and maintain an auditable governance posture after deployment.

    Ongoing monitoring may generate governance events that require investigation or formal decision-making. AI Case Management supports these event-driven governance activities by enabling investigation, exception handling, documentation, and reassessment without breaking life cycle continuity.

    AI Case Management is a cross‑life cycle capability in AIRC that supports investigation, exception handling, and regulatory response without changing the AI system’s life cycle phase unless governance decisions require it.

    AICT tracks life cycle state and operational signals. AIRC uses monitoring outputs to identify when reassessment, control updates, or governance intervention is required.

    AIRC managers determine whether changes, reassessments, or intervention are required based on operational or governance signals. Cases and inquiries are a normal part of ongoing AI governance and don’t necessarily indicate failure or non‑compliance.

    For more information, see [AI cases tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/ai-cases-tab-aict.md), [AI cases and inquiries](airc-cases-inquiries.md), and [Operations tab](operations-tab.md).

-   **Deploy, monitor, and assess value: Value**

    The value process focuses on measuring adoption, performance, and outcomes to understand whether AI initiatives are delivering expected business value and strategic impact. Measuring value helps organizations determine, with risk and compliance review, whether ongoing exposure to AI‑related risk is justified by realized business outcomes.

    AICT captures value, adoption, and outcome metrics and associates them with AI systems and use cases throughout the life cycle.

    AI asset owners determine whether to sustain, expand, adjust, or retire the AI system based on measured outcomes and business value. AIRC managers confirm that ongoing risk remains acceptable as part of this decision.

    Value measurement informs ongoing risk acceptance and helps justify continued exposure to AI‑related risk.

    Value outcomes captured in AICT can be made available to Strategic Portfolio Management to inform broader portfolio planning, funding, and prioritization decisions beyond individual AI assets.

    Governance actions identified during monitoring may result in reassessment, additional controls, or life cycle state updates managed through AICT.

    For more information, see [Value tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/aict-value-tab.md), [Adoption tab in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/aict-adoption-tab.md), and [AI risk heatmap workbench](ai-risk-heatmap-workbench.md).

-   **Life cycle closure: Retire and offboard**

    AI governance includes life cycle closure. AI systems, models, and datasets may be retired or offboarded when they no longer meet business needs, introduce unacceptable risk, or don’t deliver expected value. Life cycle closure reduces residual risk by helping ensure that AI assets are formally retired, documented, and no longer subject to active governance obligations.

    AICT manages life cycle closure and updates the AI system life cycle state. AIRC validates that final governance obligations are met and that no outstanding risk or compliance requirements remain.

    AI asset owners, with confirmation from AIRC managers, authorize retirement or offboarding decisions.

    During offboarding, the following are created or updated: updated life cycle state, retirement justification, and final governance record.

    For more information, see [Complete AI asset lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/complete-ai-asset-lifecycle.md) and [Offboarding AI assets review](airc-offboarding-ai-assets.md).


**Note:** Features described in this life cycle may require additional configurations, supporting applications, or content packs. Availability and behavior depend on installed products, assigned roles, and configuration.

