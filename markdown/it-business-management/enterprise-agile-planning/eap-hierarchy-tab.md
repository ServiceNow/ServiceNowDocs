---
title: Work item hierarchy for EAP teams
description: View and manage the complete work item hierarchy across your portfolio configurations directly from the Hierarchy tab in the Enterprise Agile Planning \(EAP\) workspace.
locale: en-US
release: zurich
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2026-02-04"
reading_time_minutes: 5
breadcrumb: [Use, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Work item hierarchy for EAP teams

View and manage the complete work item hierarchy across your portfolio configurations directly from the Hierarchy tab in the Enterprise Agile Planning \(EAP\) workspace.

Agile teams may often struggle to understand how their day-to-day work rolls up to larger organizational work. A story that is assigned to a developer might support a feature that belongs to a capability, which ultimately delivers on a strategic epic. However, tracing that hierarchy typically requires navigating multiple screens or running reports.

The Hierarchy tab in Enterprise Agile Planning \(EAP\) provides a unified view of work items across all levels of your portfolio structure, from high-level epics down to individual stories. This hierarchical display of work updates dynamically based on your selected portfolio configuration, giving team members immediate visibility into how their work contributes to broader objectives.

![Hierarchy tab of a Portfolio in Enterprise Agile Planning, in which the first Epic is expanded to show its child items Capability, Feature, and Stories in their hierarchy.](../images/eap-hierarchy.png "Hierarchy tab of a Portfolio in Enterprise Agile Planning")

## When to use

The Hierarchy tab is valuable when you need to know the complete context of work items rather than viewing them in isolation. Consider using it in the following cases:

-   Planning work and need to see what stories already exist under a feature before creating new ones.
-   Reviewing progress at the portfolio level and to drill down into execution details.
-   Onboarding team members who need to understand how their assigned work fits the bigger picture.

If you only need to track work items at a single level \(for example, just stories for your sprint\), the Backlog or Planning board views may be more efficient.

## Benefits

-   **For product owners**

    Quickly assess whether epics are broken down adequately, identify gaps in backlog refinement, and trace how customer requirements flow down through the hierarchy without switching between multiple views.

-   **For scrum masters**

    Understand cross-team dependencies at a glance, facilitate conversations about work that spans multiple agile teams, and help team members see how their sprint commitments connect to release-level objectives.

-   **For agile team members**

    Gain context for assigned work by seeing the parent feature and epic, get visibility into the business value behind technical tasks, and identify related stories that might affect their implementation approach.


## Key capabilities

-   **Multi-level hierarchy display**

    View work items across four portfolio levels: Portfolio, Solution Train, Agile Release Train \(ART\), and Agile Team, with each level displaying its default work item type such as Epics, Capabilities, Features, and Stories based on the configuration.

-   **Context-sensitive navigation**

    The hierarchy automatically adjusts based on your selected portfolio configuration. Selecting a Solution Train displays only the epics, capabilities, features, and stories relevant to that configuration.

-   **On-demand expansion**

    Child work items load only when you expand a parent item. This approach keeps the interface responsive, as you only retrieve the data you need.

-   **Interactive filters**

    Filter the hierarchy by work item type using the Filters option. Filtering enables you to focus on the work items that you need and are relevant for you.

    **Note:** Your filter selections do not persist across sessions; you must reapply filters each time you access the hierarchy.

-   **Personalized column display**

    Customize which columns appear in the hierarchy grid and adjust column widths to match your workflow. Your preferences persist across sessions, so you see your configured view each time you return. For more information, see [Personalize column layout of Hierarchy in EAP](../task/personalize-column-layout-of-hierarchy-in-eap.md).

-   **Direct record access**

    Open any work item in a new browser tab using the context menu or by clicking the Name field hyperlink. This allows you to view or edit full record details without losing your place in the hierarchy.


## Use cases

-   **Release planning and dependency mapping**

    During Program Increment \(PI\) planning, release train engineers and product managers need to know how work flows across multiple agile teams. A common scenario: your organization is planning a major platform upgrade that requires coordinated changes across three agile teams.

    Using the Hierarchy tab, the release manager can expand the epic to see all capabilities, then drill down to features assigned to each team. This visual mapping reveals which teams have dependencies on shared components, where hand-offs need to occur, and whether any critical path work lacks adequate story breakdown, all without leaving a single view or assembling data from multiple reports.

-   **Impact assessment for scope changes**

    When stakeholders request changes to a feature mid-sprint, product owners need to quickly assess the downstream impact. For example, a customer escalation requires adding new acceptance criteria to a feature that is already in progress.

    The product owner uses the Hierarchy tab to expand the affected feature and review all associated stories. They can immediately see which stories are in progress, which are complete, and which teams are involved. This visibility enables an informed conversation with stakeholders about the true cost of the change, whether it affects one story or ripples across multiple teams, before committing to revised scope.


## Considerations

-   **Initial load limits**

    For optimal performance, the hierarchy initially loads only the top 100 work items at each level, ordered by global rank. If your portfolio contains more than 100 top-level work items, use filters to narrow your view to the relevant subset.

    If you want to change this default number, work with your admin to create a **sn\_apw\_advanced.eap\_hierarchy\_items\_limit** system property. For more information, see [Modify display limit in Hierarchy tab of EAP](../task/hierarchy-display-limit-eap.md).

-   **Enabling the Hierarchy view**

    The Hierarchy tab requires your admin to enable it through the **sn\_apw\_advanced.enable\_hierarchy\_view** system property. See [Enable Hierarchy tab in EAP](../task/hierarchy-enable-eap.md).


## Getting started

To access the Hierarchy tab, navigate to the EAP workspace and select your Agile team. The Hierarchy tab is available alongside the Backlog and Planning board tabs.

