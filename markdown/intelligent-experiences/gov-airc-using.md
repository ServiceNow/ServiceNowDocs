---
title: Reviewing AI governance posture and compliance status
description: The Risk &amp; Compliance tab under Govern displays regulatory classification, risk posture, and compliance information for AI assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-airc-using.html
release: brazil
topic_type: concept
last_updated: "2026-10-03"
reading_time_minutes: 3
keywords: [use]
breadcrumb: [Managing risk and compliance, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Reviewing AI governance posture and compliance status

The Risk &amp; Compliance tab under **Govern** displays regulatory classification, risk posture, and compliance information for AI assets.

## Overview of Govern

Use the **Risk &amp; Compliance** tab under **Govern** in AI Control Tower to monitor governance activities across your AI portfolio. Review AI asset classifications, identify risk and compliance concerns, track governance work, and investigate issues that require attention.

From here, you can:

-   Review and act on top recommendations
-   Review regulatory risk classification
-   Track compliance score and compliance posture
-   Review AI risk posture, including aggregated risk score and the risk heat map
-   Monitor cases, issues, and governance actions
-   View and manage business application associations with AI systems. For more information, see [Associate a business application with an AI system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/disc-asset-associate-business-application.md)

\[Omitted image "aict-govern-risk-compliance-tab.png"\] Alt text: Risk &amp; Compliance tab under Govern showing compliance posture and risk posture sections with analytics widgets for regulatory classification, compliance scores, and risk metrics.

The page is divided into the following components:

-   Compliance posture: Monitor compliance of implemented controls and regulatory risk across the AI portfolio.
-   Risk posture: Monitor inherent and residual risk across the AI portfolio.

## Compliance posture

The widgets under compliance posture display the top action items to execute and track the risk classification and compliance score of AI systems and controls. Each widget reflects the active filter state. View details for each metric area by selecting the arrow for each metric. Select an individual component on the widget to view underlying assets.

<table id="table_compliance_posture_widgets"><thead><tr><th>

Widget

</th><th>

What it displays

</th><th>

Status breakdown

</th><th>

Roles required

</th></tr></thead><tbody><tr><td>

Your top recommendations

</td><td>

Recommended action items along with other assigned and unassigned action items. For more information, see [Act on AI asset governance insight recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-resolve-ai-asset-insight-recommendations.md)

</td><td>

-   1-Critical
-   2-High
-   3-Medium
-   4-Low

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr><tr><td>

Regulatory risk classification

</td><td>

-   Regulatory risk classification of assets in the portfolio. Use the drop-down to filter the assets into **AI System**, **AI Model**, and **Dataset**.
-   The assets are categorized based on their status. Select each status to drill down further.

For more information, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-status.md)

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

-   Compliance scores for AI assets compared to adopted frameworks and policies.
-   Compliance status for top regulatory frameworks. The progress indicator shows compliant and non-compliant controls and displays an alert badge for high-priority issues. Toggle between **Authority documents** and **Policies** to view detailed information.

For more information, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-regulatory-status.md)

</td><td>

-   Compliant
-   Non-compliant
-   To be determined

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr></tbody>
</table>## Actionable intelligence insights

The **Your top recommendations** widget is powered by two AI-generated insights, Stalled Lifecycle Tasks and Significant Issues, that evaluate your AI portfolio and surface governance work that needs attention. AI-generated insights may not reflect all relevant context — review recommendations before acting on them. For what each insight identifies, how it's determined, and how to act on its recommendations, see [Detecting governance insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-insight-detection.md).

## Risk posture

The widgets under risk posture provide a summary view of the inherent and residual risk across the AI portfolio. Use the drop-down to filter the assets into **AI System**, **AI Model**, and **Dataset**. To view detailed information about the risk and compliance posture, select **Take me there**. This opens the AI Risk and Compliance Workspace.

<table id="table_risk_posture_widgets"><thead><tr><th>

Widget

</th><th>

What it displays

</th><th>

Status breakdown

</th><th>

Roles required

</th></tr></thead><tbody><tr><td>

Aggregated risk score

</td><td>

AI system risk landscape, categorized by aggregated risk score. Use the drop-down to filter between **Inherent** and **Residual** risk. For more information, see [Reviewing AI risk posture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-risk-posture.md)

</td><td>

-   High
-   Medium
-   Low

</td><td>

 

</td></tr><tr><td>

Risk heat map

</td><td>

Assessed AI risks displayed in a color-coded matrix to help identify concentrations of higher-risk AI assets and compare current and intended risk posture. Use the drop-down to filter between **Inherent** and **Residual** risk. Select **Open heatmap workbench** to open the heat map in the AI Risk and Compliance Workspace. For more information, see [Reviewing AI risk posture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-airc-risk-posture.md).

</td><td>

-   High
-   Medium
-   Low

</td><td>

 

</td></tr></tbody>
</table>