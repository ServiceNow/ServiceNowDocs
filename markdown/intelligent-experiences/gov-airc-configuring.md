---
title: Configuring Risk and Compliance in AI Control Tower
description: Risk and Compliance information appears in AI Control Tower only when the required governance applications, frameworks, and data are available in your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-airc-configuring.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [configure]
breadcrumb: [Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Configuring Risk and Compliance in AI Control Tower

Risk and Compliance information appears in AI Control Tower only when the required governance applications, frameworks, and data are available in your environment.

## Configuration overview

Risk and Compliance information in AI Control Tower reflects the current state of governance activity for your AI portfolio and for individual AI assets. The information shown is based on available governance data rather than on configuration performed directly in these views.

-   The relevant governance applications, frameworks, and governance processes are available in your environment.

-   AI systems have governance data that can be surfaced, such as assessment status, control-related outcomes, compliance posture, risks, issues, or policy exceptions.

-   Portfolio-level views such as regulatory risk classification, compliance posture, and risk heat maps depend on governance results that have already been produced.

-   Asset-level views may display states such as **To be determined**, **No data available**, or a zero compliance score when required governance activities haven't yet produced visible results.


## How configuration affects what users see

The Risk and Compliance views in AI Control Tower don't define governance logic. Instead, they surface the outcomes of configured governance activities, such as regulatory classification, framework-specific compliance information, aggregated risk ratings, and related governance records.

For example, compliance posture for priority frameworks appears only when relevant framework and control information is available. Similarly, regulatory classification and risk heat maps depend on the presence of underlying governance results for the selected assets.

If the necessary governance information isn't yet available, incomplete states may indicate the AI system or portfolio requires additional governance activity before a full posture can be displayed.

Risk and Compliance information depends on AI Risk and Compliance being installed and, for life-cycle-driven governance, integrated with AI Control Tower. Some capabilities also depend on additional plugins, such as the AI Risk and Asset Management for Now Assist plugin and, in new IRM deployments, the IRM Standard plugin for AI intake request forms. For the full list of dependencies, see [Governing AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-governing-ai-assets.md).

For the specific properties, applications, and publishing steps required for regulatory risk classification, aggregated risk score, and compliance score, see . For more information about configuring AI Risk and Compliance, see [Configuring AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/configuring-ai-risk-and-compliance.md).

