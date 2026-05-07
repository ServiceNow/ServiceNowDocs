---
title: Operations tab
description: The Operations tab on the AI Risk and Compliance workspace provides an overview of AI systems by state and department. You can see risk assessments, AI assessments, control assurance, and a breakdown of issues by priority and policy exceptions by risk rating. It also shows the number of AI cases by priority.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [AI Risk and Compliance workspace, Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Operations tab

The Operations tab on the AI Risk and Compliance workspace provides an overview of AI systems by state and department. You can see risk assessments, AI assessments, control assurance, and a breakdown of issues by priority and policy exceptions by risk rating. It also shows the number of AI cases by priority.

The Operations tab displays the widgets that are listed in the following table. You can drill down into the data on each widget.

**Note:** Dashboards in the AI Risk and Compliance Workspace \(Risk and Compliance, Operations, and AI Cases\) display data for **Managed** AI assets only. AI assets that are marked as **Unmanaged** are excluded from dashboard widgets, metrics, and summary counts, but remain visible in inventory and list views. If you have the AI steward \[sn\_ai\_governance\_ai\_steward\] role, you can mark assets as Managed or Unmanaged. For more information, see [Assets list managed and unmanaged assets](https://www.servicenow.com/docs/access?context=assets-list-managing-and-unmanaging-assets&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

<table id="table_nry_11l_bfc"><thead><tr><th>

Widget

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI systems by state

</td><td>

Displays the number of AI systems by state.

 -   New

Submitted/registered for governance and in early intake \(pre-build\) stages.

-   Assess

Governance assessments are in progress or under review \(for example, impact or high-risk assessments\).

-   Build

In development/build-and-test, including control implementation and related governance tasks.

-   Review for deployment

Pre-deployment review to confirm assessments are complete and key issues/exceptions are addressed.

-   Live and Monitor

Deployed and under ongoing governance monitoring for risks, issues, and compliance signals.

-   Offboard

In the retired/offboarding state. Governance reviews may be completed during this state before the asset life cycle is finalized as retired. Available substates depend on configuration and appear in the UI.


</td></tr><tr><td class="sub-head" colspan="2">

Assessments

</td></tr><tr><td>

Risk assessments

</td><td>

Displays the number of assessments that are open, in progress, overdue, and due in the 7 days.

</td></tr><tr><td>

AI assessments

</td><td>

Displays the number of assessments that are in draft, assigned, and work in progress states. It also shows the number of assessments that are open, overdue, and due in 7 days.

</td></tr><tr><td class="sub-head" colspan="2">

Control assurance

</td></tr><tr><td>

Attestations

</td><td>

Displays the number of attestations that are open and overdue.Drill-down to view the list of control attestations that are awaiting for response collection.

Apply the search filter to view Control Attestations powered by Smart Assessment by selecting **New** or view Control Attestations powered by Classic Survey by selecting **Classic** from the drop-down menu.

</td></tr><tr><td>

Indicators

</td><td>

Displays the number of indicators that are open and those that failed in the last 6 months.

</td></tr><tr><td class="sub-head" colspan="2">

Tracking

</td></tr><tr><td>

Issues

</td><td>

View the number of issues that are open, overdue, and due in 7 days and also view the pie chart of issues by priority.

</td></tr><tr><td>

Policy exceptions

</td><td>

View the number of policy exceptions that are open, overdue, and due in 7 days and also view the pie chart of policy exceptions by risk rating.

</td></tr><tr><td>

AI cases

</td><td>

View the number of AI cases that are active, overdue, and due in 7 days and also view the pie chart of AI cases by priority.

</td></tr></tbody>
</table>