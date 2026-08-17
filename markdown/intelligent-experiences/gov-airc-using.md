---
title: Review AI governance posture and compliance status
description: The Risk &amp; Compliance tab under Govern displays regulatory classification, risk posture, and governance readiness for AI assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-airc-using.html
release: zurich
topic_type: concept
last_updated: "2026-04-28"
reading_time_minutes: 3
keywords: [use]
breadcrumb: [Managing risk and compliance, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Review AI governance posture and compliance status

The Risk &amp; Compliance tab under **Govern** displays regulatory classification, risk posture, and governance readiness for AI assets.

## Overview of Govern

Use the **Govern** tab in AI Control Tower to monitor and understand the governance status of AI assets. Learn how AI systems are classified, what risks they present, what governance work is required, and whether governance information is sufficiently complete to support review and decision-making.

With the **Govern** tab, you can:

-   Review regulatory classification
-   Review AI risk posture
-   Track compliance posture
-   Monitor cases, issues, and governance actions

\[Omitted image "image.aict-govern-risk-compliance-tab"\] Alt text: Govern tab showing compliance posture and risk posture sections with analytics widgets for regulatory classification, compliance scores, and risk metrics.

The page is divided into the following components:

-   Compliance posture — Monitor compliance of implemented controls and regulatory risk across the AI portfolio.
-   Risk posture — Monitor inherent and residual risk across the AI portfolio.

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

Top 5 action items

</td><td>

Recommended action items along with other assigned and unassigned action items. Select **See all Recommendations in Activity Center** to view more details. Select the arrow to open Lifecycle tasks that require action. For more information, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-airc-regulatory-status.md)

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

-   Regulatory risk classification of assets in the portfolio. Use the drop-down selector to filter the assets into AI System, AI Model, and Dataset.
-   The assets are categorized based on their status. Select each status to drill down further.

For more information, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-airc-regulatory-status.md)

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
-   Compliance status for top regulatory frameworks. The progress indicator shows compliant and non-compliant controls and displays an alert badge for high priority issues. Toggle between Authority documents and Policies to view detailed information.

For more information, see [Reviewing regulatory classification and compliance status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-airc-regulatory-status.md)

</td><td>

-   Compliant
-   Non-compliant
-   To be determined

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr></tbody>
</table>## Risk posture

The widgets under risk posture provide an at-a-glance view of the inherent and residual risk across the AI portfolio. Use the drop-down selector to filter the assets into AI System, AI Model, and Dataset. To get an in-depth look at the risk and compliance posture, select **Take me there**. This takes you to the AI Risk and Compliance Workspace

<table id="table_risk_posture_widgets"><thead><tr><th>

Widget

</th><th>

What it displays

</th><th>

Status breakdown

</th><th>

Roles required

</th></tr></thead><tbody><tr><td>

AI system by aggregated risk score

</td><td>

AI system risk landscape, categorized by aggregated risk score. Use the drop-down selector to filter between Inherent and Residual risk. For more information, see [AI risk posture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-airc-risk-posture.md)

</td><td>

-   1-Critical
-   2-High
-   3-Medium
-   4-Low

</td><td>

 

</td></tr><tr><td>

Risk heat map

</td><td>

Assessed AI risks displayed in a color-coded matrix to help identify concentrations of higher-risk AI assets and compare current and intended risk posture. Use the drop-down selector to filter between Inherent and Residual risk. Select **Open heatmap workbench** to open the heatmap in the AI Risk and Compliance Workspace. For more information, see [AI risk posture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-airc-risk-posture.md).

</td><td>

-   High
-   Medium
-   Low

</td><td>

 

</td></tr></tbody>
</table>