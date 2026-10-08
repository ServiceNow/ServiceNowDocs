---
title: View classification, risk, and compliance scores
description: View the regulatory risk classification, aggregated risk score, and compliance score of an AI asset on its record or in a workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-airc-view-classification-risk-compliance-scores.html
release: brazil
topic_type: task
last_updated: "2026-10-05"
reading_time_minutes: 2
keywords: [regulatory risk classification, aggregated risk score, compliance score, Risk &amp; Compliance tab]
breadcrumb: [Reviewing AI governance posture and compliance status, Managing risk and compliance, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# View classification, risk, and compliance scores

View the regulatory risk classification, aggregated risk score, and compliance score of an AI asset on its record or in a workspace.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

You can view an AI asset's regulatory risk classification, aggregated risk score, and compliance score in three places: on the asset's own record, at the portfolio level in AI Control Tower, or at the portfolio level in the AI Risk and Compliance. The **Govern** area of AI Control Tower and the AI Risk and Compliance Workspace render the same underlying Risk and Compliance information.

## Procedure

-   View the scores for a single AI asset:

    1.  Open the AI asset from the AI asset inventory.

    2.  Select the **Risk &amp; Compliance** tab on the asset record.

        The tab shows the asset's regulatory risk classification, aggregated risk score, compliance score, compliance posture for priority frameworks, and risk heat map together. For more information, see [Governing AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/aict-governing-ai-assets.md).

-   View portfolio-level scores in AI Control Tower:

    1.  Navigate to **Workspaces** &gt; **AI Control Tower** &gt; **Govern** &gt; **Risk &amp; Compliance**.

    2.  In the Compliance posture section, view the Regulatory risk classification and Compliance score widgets.

        For more information, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-status.md).

    3.  In the Risk posture section, view the Aggregated risk score and Risk heat map widgets.

        For more information, see [Reviewing AI risk posture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-risk-posture.md).

-   View portfolio-level scores in the AI Risk and Compliance Workspace:

    1.  Open the AI Risk and Compliance Workspace and select the **Risk and compliance** tab.

    2.  In the Compliance overview section, view the Regulatory risk classification donut chart and the compliance scores for authority documents and policies.

    3.  In the Risk overview section, view the AI systems by aggregated risk score chart and the Risk heatmap.

        For more information, see [Risk &amp; compliance tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/risk-and-compliance-tab-airc.md).


## Result

You can see the AI asset's current regulatory risk classification, aggregated risk score, and compliance score, scoped to either a single asset or your full AI portfolio.

If the Risk and Compliance dashboards on the AI asset record page or the landing page show a `No data found` error, see [Risk score and compliance score dashboard errors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-ref-troubleshooting.md).

**Related topics**  


[Classifying AI assets by regulatory risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-classification.md)

[Risk rating calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-risk-score-calculation.md)

[Compliance score calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-compliance-score-calculation.md)

[Reviewing AI governance posture and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-using.md)

