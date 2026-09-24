---
title: Operations tab
description: The Operations tab on the AI Risk and Compliance workspace provides an overview of AI systems by state, along with metrics for assessments, control assurance, issues, policy exceptions, and AI cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/ai-risk-management/operations-tab.html
release: brazil
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Operations tab, AI risk and compliance workspace, dashboard widgets, AI systems by state, risk assessments, control assurance, AI cases]
breadcrumb: [AI Risk and Compliance workspace, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Operations tab

The Operations tab on the AI Risk and Compliance workspace provides an overview of AI systems by state, along with metrics for assessments, control assurance, issues, policy exceptions, and AI cases.

## How dashboard metrics are derived

The widgets in the Operations tab display summarized data based on records associated with managed AI assets. Each widget aggregates information from underlying records such as AI assets, assessments, control attestations, indicators, issues, policy exceptions, and AI cases.

Metrics are calculated as counts grouped by state, status, priority, or risk rating, depending on the widget. For example, assessment widgets group records by life cycle or due-date status, while tracking widgets group records by priority or risk rating.

Select a widget or chart segment to open a filtered list view of the underlying records used to generate that metric.

## Operations tab widgets

**Note:** Dashboards in the AI Risk and Compliance Workspace \(Risk and Compliance, Operations, and AI Cases\) display data for **Managed** AI assets only. AI assets marked as **Unmanaged** are excluded from dashboard widgets, metrics, and summary counts, but remain visible in inventory and list views. If you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role, you can mark assets as Managed or Unmanaged. To mark an asset, see [Assets list- managed and unmanaged assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/assets-list-managing-and-unmanaging-assets.md).

The following table describes the widgets available on the Operations tab. Select any widget to view the underlying data.

<table id="table_nry_11l_bfc"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI systems by state

</td><td>

Displays the number of AI systems grouped by life cycle state.

 -   **New**

Submitted or registered for governance and in early intake \(pre-build\) stages.

-   **Assess**

Governance assessments are in progress or under review — for example, impact or high-risk assessments.

-   **Build**

In development and build-and-test, including control implementation and related governance tasks.

-   **Review for deployment**

Pre-deployment review to verify assessments are complete and key issues and exceptions are addressed.

-   **Live and Monitor**

Deployed and under ongoing governance monitoring for risks, issues, and compliance signals.

-   **Offboard**

In the retired or offboarding state. Governance reviews may be completed during this state before the asset life cycle is finalized as retired. Available substates depend on configuration and appear in the UI.


</td></tr><tr><td class="sub-head" colspan="2">

Assessments

</td></tr><tr><td>

Risk assessments

</td><td>

Displays the number of risk assessments that are open, in progress, overdue, and due in 7 days.

</td></tr><tr><td>

AI assessments

</td><td>

Displays the number of AI assessments in **Draft**, **Assigned**, and **Work in Progress** states, and the number that are open, overdue, and due in 7 days.

</td></tr><tr><td class="sub-head" colspan="2">

Control assurance

</td></tr><tr><td>

Attestations

</td><td>

Displays the number of control attestations that are open and overdue. Select the widget to view the list of control attestations awaiting response collection.

 To filter attestations by type, select **New** to view control attestations powered by Smart Assessment, or select **Classic** to view control attestations powered by Classic Survey.

</td></tr><tr><td>

Indicators

</td><td>

Displays the number of indicators that are open and those that failed in the last 6 months.

</td></tr><tr><td class="sub-head" colspan="2">

Tracking

</td></tr><tr><td>

Issues

</td><td>

Displays the number of issues that are open, overdue, and due in 7 days, and a pie chart of issues by priority.

</td></tr><tr><td>

Policy exceptions

</td><td>

Displays the number of policy exceptions that are open, overdue, and due in 7 days, and a pie chart of policy exceptions by risk rating.

</td></tr><tr><td>

AI cases

</td><td>

Displays the number of AI cases that are active, overdue, and due in 7 days, and a pie chart of AI cases by priority.

</td></tr></tbody>
</table>**Related topics**  


[AI Risk and Compliance workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/ai-risk-and-compliance-workspace.md)

[Offboarding AI assets review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/ai-risk-management/airc-offboarding-ai-assets.md)

