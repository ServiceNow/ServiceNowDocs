---
title: Governing AI asset risk and compliance
description: Get a consolidated view of your AI asset's regulatory risk classification, compliance posture, control effectiveness metrics, and governance artifacts from the Risk &amp; compliance tab.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-airc-ai-asset.html
release: zurich
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 2
breadcrumb: [Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Governing AI asset risk and compliance

Get a consolidated view of your AI asset's regulatory risk classification, compliance posture, control effectiveness metrics, and governance artifacts from the Risk &amp; compliance tab.

When you open an AI asset record, the Risk &amp; compliance tab provides a consolidated view of regulatory risk classification, compliance posture, control effectiveness metrics, and associated governance tasks.

\[Omitted image "image.aict-govern-asset-page-risk-compliance"\] Alt text: Risk and Compliance tab showing regulatory risk classification, compliance posture, aggregated risk rating, risk heat map, and governance sections.

The following table describes each section of the Risk &amp; Compliance Asset page.

<table id="ai-asset-page-risk-and-compliance"><thead><tr><th>

Section

</th><th>

What it displays

</th><th>

Status breakdown

</th><th>

Roles required

</th></tr></thead><tbody><tr><td>

Regulatory risk classification

</td><td>

Regulatory risk classification of the asset in the portfolio. For more information, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-airc-regulatory-status.md)

</td><td>

-   Low
-   Medium
-   High
-   Unacceptable
-   Critical
-   To be determined

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr><tr><td>

Compliance score

</td><td>

Overall compliance score for the AI asset and trend information over time. The score reflects the asset's compliance with adopted frameworks and policies.

</td><td>

0-100%

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr><tr><td>

Compliance posture for priority frameworks

</td><td>

-   Compliance scores for AI assets compared to adopted frameworks and policies.
-   Compliance status for priority frameworks showing the number of compliant and non-compliant controls associated with the AI asset. The progress indicator shows compliant and non-compliant controls and displays an alert badge for high priority issues. Toggle between Authority documents and Policies to view detailed information.

For more information, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-airc-regulatory-status.md)

</td><td>

-   Conforming
-   Non-conforming
-   To be determined

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr><tr><td>

Aggregated risk rating

</td><td>

Aggregated risk rating for the AI asset, including residual risk, inherent risk, and control effectiveness metrics.

</td><td>

-   High
-   Medium
-   Low

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr><tr><td>

Risk heat map

</td><td>

Identified risks associated with the AI asset. By default, the risk heat map applies the Residual risk filter, but you can filter the heat map by Inherent risk. Segmentation changes based on the selected filter. Risks appear under the respective combination of risk and control effectiveness, or impact and likelihood, depending on the selected risk classification filter.

</td><td>

The risk heat map consists of the following parameters along the X and Y axes:-   Residual risk
    -   Inherent risk \(X-axis\)
        -   Low
        -   Medium
        -   High
    -   Control effectiveness \(Y-axis\)
        -   Effective
        -   Needs improvement
        -   Ineffective
-   Inherent risk
    -   Impact \(X-axis\)
        -   Low
        -   Medium
        -   High
        -   Critical
    -   Likelihood \(Y-axis\)
        -   Unlikely
        -   Likely
        -   Highly likely
        -   Almost certain

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr><tr><td>

Governance

</td><td>

Risk assessments, controls, compliance tasks, and related governance artifacts for the AI asset. Governance-related items are organized into categories with expandable subsections. Select an artifact to open it in the AI Control Tower workspace. For more information, see[Governing AI asset risk and compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-airc-ai-asset.md).

</td><td>

NA

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr></tbody>
</table>**Parent Topic:**[Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-managing-ai-assets.md)

