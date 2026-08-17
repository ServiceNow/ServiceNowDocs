---
title: Configuring Risk and Compliance in AI Control Tower
description: Risk and Compliance information appears in AI Control Tower only when the required governance applications, frameworks, and data are available in your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-airc-configuring.html
release: zurich
topic_type: concept
last_updated: "2026-05-13"
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

-   Asset-level views may display states such as **To be determined**, **No data available**, or a zero compliance score when required governance activities have not yet produced visible results.


## How configuration affects what users see

The Risk and Compliance views in AI Control Tower do not define governance logic. Instead, they surface the outcomes of configured governance activities, such as regulatory classification, framework-specific compliance information, aggregated risk ratings, and related governance records.

For example, compliance posture for priority frameworks appears only when relevant framework and control information is available. Similarly, regulatory classification and risk heat maps depend on the presence of underlying governance results for the selected assets.

If the necessary governance information is not yet available, incomplete states may indicate the AI system or portfolio requires additional governance activity before a full posture can be displayed.

For more information about configuring AI Risk and Compliance, see [Configuring AI Risk and Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/configuring-ai-risk-and-compliance.md).

