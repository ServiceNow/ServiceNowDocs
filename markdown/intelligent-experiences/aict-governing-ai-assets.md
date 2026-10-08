---
title: Governing AI assets
description: Govern AI assets across the life cycle with integrated risk, compliance, security, and privacy oversight in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-governing-ai-assets.html
release: brazil
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 5
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Governing AI assets

Govern AI assets across the life cycle with integrated risk, compliance, security, and privacy oversight in AI Control Tower.

## Governance overview

Deploying AI at enterprise scale introduces regulatory, operational, security, privacy, and reputational risks. Regulations and frameworks in this space require organizations to demonstrate that AI systems are assessed, monitored, and controlled. Governance also addresses operational and security risks such as biased outputs, unauthorized data access, privileged agents operating without oversight, and inactive systems that retain active permissions.

The Govern area in AI Control Tower brings together Risk and Compliance and Security and Privacy to support end-to-end AI governance. These areas work alongside life-cycle management and approval workflows to support end-to-end AI governance. Different teams manage each governance area by using their respective tools, while AI Control Tower provides a unified view of governance information for AI assets.

Risk and Compliance provides visibility into regulatory classification, compliance posture, risk, assessments, and related governance records. Security and Privacy provides visibility into access concerns, privileged and dormant AI agents, AI asset security posture, and sensitive data protection.

For more information about how AI Control Tower and AI Risk and Compliance work together across the AI life cycle, see [AI governance life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-gov-lifecycle.md).

## Managing AI risk and compliance

Depending on your role, you can engage with AI Control Tower and AI Risk and Compliance in different ways. AI asset owners typically use individual AI asset records to review risk posture, compliance posture, and related governance records. AI stewards and risk and compliance teams use portfolio-level views, assessments, and cases to monitor governance posture, identify gaps, and initiate remediation.

The Risk and Compliance area in AI Control Tower provides visibility into how AI assets align with organizational policies and regulatory requirements. Summarized views of regulatory risk classification, compliance posture, compliance score, and aggregated risk score help governance teams evaluate AI risk without manually consolidating information from multiple systems.

Regulatory risk classification applies to AI systems, AI models, and datasets. Assessments determine whether an asset has a high, medium, low, or unacceptable regulatory risk classification by evaluating its potential impact across multiple dimensions. Compliance is tracked against authority documents and organizational policies. AI Risk and Compliance includes built-in support for priority regulatory frameworks and supports organization-specific requirements.

The Risk posture section in AI Control Tower groups AI assets by aggregated risk score and displays a risk heat map. The heat map plots AI assets by inherent or residual risk level against control effectiveness. You can switch between inherent and residual risk views.

The Risk and Compliance page in the Govern area provides the following information:

-   Compliance score: Percentage of controls in a compliant state across mapped frameworks.

-   Regulatory risk classification: Distribution of AI assets by regulatory risk level.

-   Compliance posture for priority frameworks: Compliant and noncompliant control counts for the two highest-priority frameworks.

-   Top recommendations: High-priority governance work, such as overdue life-cycle tasks and AI asset issues that require review.


For supported AI assets in the AI asset inventory, the **Risk &amp; Compliance** tab provides governance information scoped to the selected asset. This information includes regulatory risk classification, compliance score, aggregated risk score, compliance posture for priority frameworks, and a risk heat map. The Governance section on the same tab provides access to assessments, risks, controls, attestations, issues, and policy exceptions associated with the asset.

AI cases and inquiries provide structured workflows for investigating and resolving governance concerns. Teams can use cases to track violations, risks, or compliance gaps through investigation and remediation. Inquiries support compliance-related requests for clarification.

For more information about risk assessment workflows, compliance framework configuration, and governance case management, see [AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-and-compliance.md).

**Note:** To use AI Risk and Compliance with AI Control Tower, install the required applications from the ServiceNow Store and activate the required plugins. AI Risk and Compliance can be installed as a standalone application from the ServiceNow Store, but life-cycle-driven governance requires integration with AI Control Tower. AI Control Tower is used to register AI systems, models, and datasets and to manage life-cycle progression that triggers risk and compliance assessments, governance tasks, and case workflows.

Some AI risk and governance capabilities depend on additional plugins. Governance of ServiceNow AI assets with Now Assist requires the AI Risk and Asset Management for Now Assist plugin, which depends on integration between AI Risk and Compliance and AI Control Tower, and AI Asset Management. In new IRM deployments, the IRM Standard plugin is required to make AI intake request forms available for submitting AI systems, models, and datasets for governance and risk evaluation.

## Securing AI assets and managing privacy

The security area covers user access, data protection, and autonomous systems and agents that hold permissions, execute workflows, and interact with external tools without direct human involvement.

AI Control Tower provides visibility into the following dimensions of AI security:

-   Access issues: Identifies AI agents that experience access-related errors that can prevent workflows from completing.

-   Privileged AI agents: Identifies agents with elevated permissions, such as admin or security admin, to support least-privilege reviews.

-   Dormant AI systems: Identifies agents that have been inactive for more than 90 days and retain permissions, and generates review tasks for asset owners.

-   Access map: Visualizes relationships between ServiceNow agents, agentic workflows, and the tools that they use to support access analysis and impact assessment.

-   AI asset security score: Provides a composite view of AI asset security posture based on access issues, privileged agents, guardrails, and dormant systems, with details for individual assets.


For privacy oversight, AI Control Tower integrates with the Data Privacy plugin to display sensitive data detection and anonymization activity. The Security and Privacy area shows the enabled data patterns used to detect and anonymize sensitive information in AI prompts.

For organizations using Now Assist, ServiceNow AI Insights summarizes observations across the AI security posture, including areas that require attention and remediation actions. This capability requires the Now Assist AICT Security Posture Summarizer skill.

