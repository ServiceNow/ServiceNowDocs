---
title: AI risk heatmap workbench
description: Use the AI risk heatmap workbench to visualize assessed AI risks in a color-coded matrix. The heatmap helps you identify concentrations of higher-risk AI assets and compare current and intended risk posture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/ai-risk-heatmap-workbench.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [AI risk heatmap, AI risk visualization, AI risk governance]
breadcrumb: [Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# AI risk heatmap workbench

Use the AI risk heatmap workbench to visualize assessed AI risks in a color-coded matrix. The heatmap helps you identify concentrations of higher-risk AI assets and compare current and intended risk posture.

The AI risk heatmap workbench displays risks derived from completed AI risk assessments. The heatmap visualizes calculated risk data produced by the selected risk assessment methodology \(RAM\). Heatmap structure, scoring ranges, and rating thresholds are defined by your instance risk configuration.

You can use the heatmap to analyze different risk postures, including inherent, residual, and target risk, depending on the selected view.

\[Omitted image "risk-heatmap-ai-risks.png"\] Alt text: An AI risk heatmap visualizing assessed risks in a matrix, with selectable cells and a drill-down risk list.

## How risk is represented

The heatmap visualizes assessed AI risks in a matrix format. The axes and segmentation used depend on the selected **View risk by** option.

-   **Inherent risk**

    Displays risk exposure before any controls are applied. In this view, risks are typically positioned by likelihood and impact.

-   **Residual risk**

    Displays risk exposure after current controls are applied. In this view, risks are positioned based on inherent risk and control effectiveness.

-   **Target risk**

    Displays the intended future risk posture, representing where the organization aims to be after planned risk treatment actions and control improvements are implemented.


Each cell in the heatmap is color-coded based on the risk rating configured for the corresponding score range.

Availability and meaning of target risk values depend on the configuration of the selected risk assessment methodology. The heatmap reflects calculated risk assessment data and updates when risk scores are recalculated by the system.

## Drill-down

Select a heatmap cell to view the list of risks included in that classification. The **List** panel shows the risks that correspond to the selected heatmap cell.

Each risk entry displays key details such as risk rating, score, identifier, name, owner, and associated entity. Select a risk entry to open the full risk record.

-   Use the search field to locate a specific risk within the current results.
-   Use the pagination controls to navigate through the list.
-   Use the actions menu on a risk to access additional options, depending on configuration.

## Filters

Use the filter bar to control which risks appear in the heatmap.

-   **Risk assessment methodology**

    Select the risk assessment methodology \(RAM\) used to generate the risk data displayed in the heatmap. For information about the pre-shipped RAMs and risk ratings defined for AI assets, see [Risk assessment methodologies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-rams.md).

-   **Top risks**

    Limit the heatmap view to a subset of risks or select **Show all** to display all risks.

-   **Entity**

    Filter risks by the AI asset or entity they are associated with.

-   **View heatmap by**

    Select how risks are labeled within the heatmap cells, such as by risk name.

-   **View risk by**

    Select which risk posture to visualize:

    -   **Inherent**
    -   **Residual**
    -   **Target**

Select **Filter overview** to view or modify advanced filter conditions.

## UI elements

-   **List tab**

    Displays the drill-down list of risks for the selected heatmap cell or for the current filter set.

-   **My saved filters**

    Displays filter configurations you have saved for reuse.

-   **Filter icons**

    Use the filter icons above the heatmap to open filter options or export data, depending on your instance configuration.


**Note:** To understand more about configuring the heatmap and its filters, refer to [Configure risk heatmaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-risk-management-workspace/configure-risk-heatmap.md).

**Related topics**  


[AI Risk and Compliance workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/ai-risk-and-compliance-workspace.md)

