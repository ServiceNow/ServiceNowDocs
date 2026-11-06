---
title: AI Risk and Compliance life cycle tasks
description: AI Risk and Compliance life cycle tasks track governance activities across the onboarding and offboarding of AI systems, AI models, and datasets. Each task is scoped to a life cycle phase.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/ai-risk-management/airc-life-cycle-tasks.html
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [AI Risk and Compliance, lifecycle tasks, AI governance]
breadcrumb: [AI governance life cycle, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI Risk and Compliance life cycle tasks

AI Risk and Compliance life cycle tasks track governance activities across the onboarding and offboarding of AI systems, AI models, and datasets. Each task is scoped to a life cycle phase.

AI risk and compliance life cycle tasks track governance activities as AI systems, AI models, and datasets move through onboarding and offboarding. When a new AI asset is onboarded it enters a governed life cycle. Governance activities throughout onboarding help organizations understand risk, apply appropriate controls, and make informed deployment decisions. Each of these important milestones are offered as pre-deployed phases which in turn consist of tasks. With these tasks, compliance managers, risk owners, and AI system owners can complete required reviews, assessments, and approvals at each life cycle phase.

## AI asset onboarding life cycle tasks

The Onboarding playbook for an AI asset moves through the Assess, Build &amp; Test, and Deploy phases. Each of these phases have associated tasks that are available predefined for your team to set up. Each life cycle phase and its associated tasks are dependent on the successful completion of the preceding phase.

<table id="AI-system-onboarding-tasks"><thead><tr><th>

Task name

</th><th>

Purpose

</th><th>

Associated actions and role-specific privileges

</th><th>

Assigned to

</th><th>

Conditional visibility logic

</th><th>

Applicable to AI asset

</th></tr></thead><tbody><tr class="sub-head"><td class="sub-head" colspan="6">

**Assess**

</td></tr><tr><td>

Impact assessment

</td><td>

Review and document how this AI asset may affect people, processes, and the business. Identify potential risks, ethical considerations, and regulatory requirements before operational use.

</td><td>

-   AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]: The AI asset owner can initiate the assessments.
-   AI Steward \[sn\_ai\_governance.ai\_steward\]: The AI steward can view response of the assessment

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

</td><td>

Appears during the assess phase when in the In Review or Draft state. Disappears when task is completed and transitions to Approved for Development state.

</td><td>

-   AI system
-   AI model

</td></tr><tr><td>

Perform risk assessment

</td><td>

Evaluate the likelihood and severity of risks associated with the AI asset and determine appropriate risk classification and required controls to inform governance requirements.

</td><td>

AI Risk &amp; Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]: Performs risk assessment

</td><td>

AI Risk &amp; Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]:

</td><td>

Appears when impact assessment is complete during Draft state. Disappears when task is completed and transitions to Approved for Development state

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr><tr><td class="sub-head" colspan="6">

**Build and test**

</td></tr><tr><td>

Collect information on the deployment regions of the AI system

</td><td>

-   Implement value templates to derive usage and adoption metrics
-   From AICT, the Collect Information on Deployment Regions task moves to In Review. In AIRC, the Share Deployment Details task progresses to complete — completing the task in both systems. Control attestations and risk assessments are completed from AIRC.

</td><td>

Asset Owner or AI Steward or AI Risk &amp; Compliance Analyst

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

</td><td>

 

</td><td>

AI system

</td></tr><tr><td>

Create control attestation

</td><td>

Each AI asset is associated with control objectives that define the requirements it must satisfy. You can attest to controls, capture supporting evidence, and monitor compliance status throughout the life cycle of the asset.

</td><td>

AI Risk &amp; Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]: Can update the states of the record from theAI Risk and Compliance Workspace

</td><td>

AI Risk &amp; Compliance Analyst \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\]

</td><td>

Appears when the asset is approved for deployment. Disappears when task is completed and the asset reaches Ready for Deployment state.

</td><td>

AI system

</td></tr><tr><td>

Perform control attestation

</td><td>

Use AI Risk and Compliance to attest controls associated with your AI systems. Control attestations confirm whether a control is operating effectively and help maintain your organization's compliance posture.

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]: -   The AI asset owner can move the task to In progress state
-   The AI asset owner can move the task can move the task to review state

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

</td><td>

Appears when the asset is approved for deployment during the build phase. Disappears when task is completed and when asset reaches Ready for Deployment state.

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr><tr><td>

Conformity assessment

</td><td>

Perform a conformity assessment to evaluate whether an AI asset conforms to applicable requirements in AI Risk and Compliance.

</td><td>

-   AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]: The AI asset owner can initiate assessments
-   AI Steward \[sn\_ai\_governance.ai\_steward\]: The AI Steward can view responses to assessments

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

</td><td>

Appears when asset is Approved for Deployment during the build phase. Disappears when task is completed; when asset reaches Ready for Deployment state.

</td><td>

AI system

</td></tr><tr><td class="sub-head" colspan="6">

**Deploy**

</td></tr><tr><td>

Deploy asset

</td><td>

When governance readiness is confirmed and deployment is approved, the AI system is deployed and transitions into the operational monitoring phase.

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

</td><td>

AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\]

</td><td>

Appears when asset is approved for deployment when all pre-deployment tasks are complete. Disappears when task is completed and the asset is move to the active state

</td><td>

-   AI system
-   AI model
-   Dataset

</td></tr></tbody>
</table>The Onboard playbook for an AI model and for a Dataset currently defines a smaller task set. Both asset classes generate **Impact assessment** \(AI model only\) and **Perform risk assessment** in the Assess phase, both marked **Production**. Neither asset class has Collaboration or Architecture review tasks defined.

