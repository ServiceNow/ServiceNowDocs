---
title: Governing AI assets
description: Manage AI assets across the life cycle using AI Risk and Compliance, with integrated Security and Privacy oversight for risk, compliance, and security.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-governing-ai-assets.html
release: australia
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [AI Control Tower, Enable AI experiences]
---

# Governing AI assets

Manage AI assets across the life cycle using AI Risk and Compliance, with integrated Security and Privacy oversight for risk, compliance, and security.

## Governance overview

Deploying AI at enterprise scale introduces regulatory, operational, and reputational risk. Regulations and frameworks in this space require organizations to demonstrate that AI systems are assessed, monitored, and controlled. Governance also addresses operational risks such as biased outputs, unauthorized data access, privileged agents operating without oversight, and inactive systems that retain active permissions.

AI Control Tower provides two complementary governance areas, risk and compliance, and security and privacy, that work alongside lifecycle management and approval workflows to support end-to-end AI governance. Each governance area is owned and managed by different teams using different tools, while contributing to a unified governance view in the AI Control Tower workspace.

For more information about how AI Control Tower and AI Risk and Compliance work together across the AI life cycle, see [AI governance life cycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-gov-lifecycle.md).

## Managing AI risk and compliance

Depending on your role, you can engage with AI Control Tower and AI Risk and Compliance in different ways. AI asset owners typically interact with this area through individual AI asset records to review risk, compliance, and governance outcomes. AI stewards and risk and compliance teams use aggregated dashboards, assessments, and cases to monitor posture, identify gaps, and initiate remediation.

The risk and compliance area in AI Control Tower helps AI stewards and compliance teams maintain visibility into how AI assets align with organizational policies and regulatory requirements. Aggregated views of risk classification, compliance posture, and regulatory context enable governance teams to evaluate AI risk without manually consolidating information from multiple systems.

Risk classification applies to AI systems, AI models, and datasets. Classifications, high, medium, low, and unacceptable, are determined through assessments that evaluate potential impact across multiple dimensions. Compliance is tracked against authority documents and organizational policies. AI Risk and Compliance includes built-in support for priority regulatory frameworks and supports organization-specific requirements.

The Risk posture section in AI Control Tower groups AI systems by aggregated risk score and displays a risk heat map. The heat map plots AI assets by inherent or residual risk level against control effectiveness. Switch between inherent and residual risk views to change the display.

The Risk and compliance page in the **Govern** area provides the following views:

-   Compliance score: Percentage of controls in a compliant state across mapped frameworks
-   Regulatory risk classification chart: Distribution of AI assets by risk level
-   Compliance posture for priority frameworks: Compliant and non-compliant control counts for the two highest priority frameworks
-   Top action items panel: Critical governance actions such as overdue lifecycle tasks and high-priority asset issue reviews, with options to open or automate follow-up actions

At the individual asset level, the Risk and compliance tab on an AI asset record provides the same risk and compliance widgets scoped to that asset. This includes aggregated risk rating, compliance score, regulatory risk classification, compliance posture for priority frameworks, and the risk heat map. The Governance section on the same tab provides access to assessments, risks, controls, attestations, issues, and policy exceptions associated with the asset.

AI cases and inquiries provide structured workflows for investigating and resolving governance concerns. Teams can create cases to track violations, risks, or compliance gaps through investigation and remediation. Inquiries support a lighter-weight process for compliance-related clarification requests.

For more information about risk assessment workflows, compliance framework configuration, and governance case management, see [AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-and-compliance.md).

**Note:** To use AI Risk and Compliance with AI Control Tower, you must install and activate the required applications and plugins. AI Risk and Compliance can be installed as a standalone application from the ServiceNow Store, but life-cycle-driven governance requires integration with AI Control Tower. AI Control Tower is used to register AI systems, models, and datasets and to manage life-cycle progression that triggers risk and compliance assessments, governance tasks, and case workflows.

Some AI risk and governance capabilities depend on additional plugins. Governance of ServiceNow AI assets with Now Assist requires the AI Risk and Asset Management for Now Assist plugin, which depends on integration between AI Risk and Compliance and AI Control Tower, and AI Asset Management. In new IRM deployments, the IRM Standard plugin is required to make AI intake request forms available for submitting AI systems, models, and datasets for governance and risk evaluation.

## Securing AI assets and managing privacy

The security and privacy area addresses security considerations specific to AI assets. In addition to user access and data protection, AI security accounts for autonomous systems and agents that hold permissions, execute workflows, and interact with external tools without direct human involvement.

AI Control Tower tracks multiple dimensions of AI security.

-   Access issues. Identifies AI agents that experience access-related errors that may prevent workflows from completing.

-   Privileged AI agents. Tracks agents with elevated permissions, such as admin or security admin, to support least-privilege review.

-   Dormant AI systems. Identifies agents that have been inactive for more than 90 days and still retain permissions, and generates review tasks for asset owners.

-   Access map. Visualizes relationships between ServiceNow agents, agentic workflows, and the tools they use to support access analysis and impact assessment.

-   AI asset security score. Provides a composite view of AI asset security posture based on access issues, privileged agents, guardrails, and dormant systems, with drill-down by asset.


For privacy, AI Control Tower integrates with the Data Privacy plugin to surface sensitive data detection and anonymization activity. The security dashboard shows enabled data patterns that are used to detect and anonymize sensitive information in AI prompts.

For organizations using Now Assist, ServiceNow AI Insights summarize observations across the AI security posture, including areas that may require attention and suggested remediation actions. This capability requires the Now Assist AICT Security Posture Summarizer skill.

