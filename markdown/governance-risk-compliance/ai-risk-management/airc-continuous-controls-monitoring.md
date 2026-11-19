---
title: Continuous controls monitoring in the AI Risk and Compliance Workspace
description: Indicators in AI Risk and Compliance Workspace continuously monitor control compliance for AI systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/ai-risk-management/airc-continuous-controls-monitoring.html
release: zurich
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 2
keywords: [AI governance, continuous monitoring, control compliance, indicators]
breadcrumb: [Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Continuous controls monitoring in the AI Risk and Compliance Workspace

Indicators in AI Risk and Compliance Workspace continuously monitor control compliance for AI systems.

Risk and compliance managers can continuously monitor the controls attached to AI systems. Connect an external AI evaluation framework to the existing indicators framework in AI Risk and Compliance Workspace.

## Indicators for AI systems

In organizations managing Governance, Risk, and Compliance \(GRC\) workflows for AI systems, teams can be challenged when monitoring control effectiveness in real time. Manual control testing can leave gaps in visibility and increase the risk of undetected control failures. Without continuous insight into control performance, organizations can face delayed issue resolution, costly compliance violations, and reduced operational resilience. Continuous Controls Monitoring \(CCM\) automates control verification, reducing manual testing burden and providing real-time visibility into control health. AI Risk and Compliance Workspace evaluates whether a control is compliant or non-compliant using indicators that run on a schedule. When an indicator fails, a GRC issue is created so that the product owner of the affected asset can remediate it. The compliance score of the associated record decreases. This same indicator concept is extended to AI systems by using evaluation scores produced by an AI evaluation framework.

## Value for AI governance

Applying indicators to AI system entities gives an organization a single system of record for AI governance evidence. This approach enables continuous monitoring of model risk instead of relying on periodic manual reviews. It also provides an audit trail that supports Compliance Scoring for AI-specific control objectives and authorities, such as internal AI policies or external AI regulation.

## AI evaluation framework providers

A compliance evaluation configuration can evaluate an AI system using metrics from **ServiceNow** or from other evaluation framework providers, such as Traceloop. Each provider exposes a different set of base metrics, such as toxicity, PII detection, prompt injection, and agent goal accuracy. The provider selected in a configuration determines which metrics are available.

For more information, see [Create a compliance evaluation configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/ai-risk-management/airc-compliance-evaluation-configuration.md), [Use a compliance evaluation on an AI system record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/ai-risk-management/airc-use-compliance-evaluation-ai-system.md), and [AI evaluation base metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/ai-risk-management/airc-ai-evaluation-base-metrics.md).

## Monitoring lifecycle

After an AI use case is deployed, it moves into a monitor state. Its controls are evaluated continuously over the lifetime of the AI system, on a daily, weekly, or monthly frequency. Each evaluation checks the trace, session, or span records produced by the evaluation framework against the configured metric thresholds. If a control fails, an issue is raised against the AI system and its compliance score decreases; when the control becomes compliant again, the score increases.

**Related topics**  


[Create a compliance evaluation configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/ai-risk-management/airc-compliance-evaluation-configuration.md)

