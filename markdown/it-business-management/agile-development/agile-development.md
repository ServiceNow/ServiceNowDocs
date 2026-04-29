---
title: Agile Development
description: The ServiceNow Agile Development application helps you deliver software projects more efficiently by managing and tracking software development life-cycles using an iterative, incremental, and flexible approach.
locale: en-US
release: australia
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Strategic Portfolio Management]
---

# Agile Development

The ServiceNow® Agile Development application helps you deliver software projects more efficiently by managing and tracking software development life-cycles using an iterative, incremental, and flexible approach.

When you have multiple standalone tools for development, testing, and project tracking, there could be a disconnect between enhancements and fixes, change processes, and deployment. Agile Development pulls these development life-cycle workflows together into one system and helps you manage the backlog, from inception through testing and deployment. By offering you the flexibility to use scrum or traditional waterfall method, Agile Development provides you increased visibility into the entire product development life cycle.

## Variants of ServiceNow® Agile Development

-   **Agile Development under Project Management**

    See [Agile Development 2.0 integration with Project Portfolio Management](../../sdlc-scrum/concept/c_SDLCIntegrationWithProjectPortfolioSuite.md) for project-based agile development.

-   **Agile Development 1.0**

    **Important:** The Agile Development 1.0 plugin \(com.snc.sdlc.scrum.pp\) is no longer available for activation. Activate the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\) for enhanced agile capabilities to manage your software development efforts.

-   **Agile Development 2.0**

    Agile Development 2.0 supports agile-based execution. It provides an agile software development environment for product-based or project-based efforts, using the scrum agile framework. With Agile Development 2.0, you have the flexibility to implement a pure agile approach over the entire life cycle of a product, or a hybrid approach using agile methods within a traditional project structure.

    For more information, see [Agile Development 2.0](../reference/agile-landing-page.md).


**Note:** If you upgrade to Agile Development 2.0 from Agile Development 1.0, Agile Development 2.0 replaces Agile Development 1.0 in your ServiceNow instance. If you are implementing ServiceNow® Agile Development for the first time, activate the Agile Development 2.0 plugin \(com.snc.sdlc.agile.2.0\).

## Key differences between the Agile Development variants

<table id="table_agile_differences"><thead><tr><th>

Feature

</th><th>

Agile Development \(Project Management\)

</th><th>

Agile Development 2.0

</th></tr></thead><tbody><tr><td>

Backlog

</td><td>

A story can be associated to only a project.

</td><td>

A personalized backlog can be created by defining filter criteria.

</td></tr><tr><td>

Release

</td><td>

A project story cannot be associated to a release.

</td><td>

A release is a definite timeline to execute prioritized stories from the backlog.-   Project-based execution — It allows the release backlog to be executed as one or more projects.
-   Non-project-based execution — It allows the release backlog to be executed by one or more assignment groups using their sprint schedules within a release timeline.

</td></tr><tr><td>

Theme and Epic

</td><td>

A story cannot be associated to a theme, or epic.

</td><td>

Backlog stories can be categorized by themes and epics.

</td></tr><tr><td>

Team versus Assignment Group

</td><td>

Assignment Group is used.

</td><td>

Assignment Group is used to create an assignment group of type Agile Team. The confusion between when to use release team versus assignment group is eliminated. An existing release team can be converted into an assignment group.

</td></tr><tr><td>

Sprints

</td><td>

Sprints are assignment group-based. Each group can have its own sprint schedule.

</td><td>

Sprints are generated for Assignment Groups. Different groups can use different sprint schedules or all the groups can follow the same schedule. The Agile Board **Sprint Planning** tab is used to manage sprints.

</td></tr><tr><td>

Sprint Planning

</td><td>

The Sprint Planning Board is used.

</td><td>

The Sprint Planning tab on the Agile board is used.

</td></tr><tr><td>

Task Progress board and Story progress board

</td><td>

VTB \(Visual Task Board\) is used.

</td><td>

The Sprint Tracking tab on the Agile board is used.

</td></tr></tbody>
</table>## Integration with Digital Portfolio Management

Digital Portfolio Management \(DPM\) provides a unified workspace for owners to view and collectively manage their services and applications through the full life cycle. By integrating DPM with Agile Development 2.0, DPM Managers can view Agile Development 2.0 data such as epics, stories, sprints, and releases in the context of the selected business application.

-   **[Agile Development 2.0](../reference/agile-landing-page.md)**  
ServiceNow Agile Development 2.0 provides an agile software development environment for product-based or project-based efforts, using the Scrum framework. Implement a pure agile approach over the entire life cycle of a product, or a hybrid approach using agile methods within a traditional project structure.
-   **[Mobile experience for Agile Development 2.0](../../agile-2-mobile/concept/agile-2-mobile-app-overview.md)**  
Track and update the status of your stories and scrum tasks of the current sprint from your mobile device using the Agile Development v2 mobile app.
-   **[Scrum Programs for Agile Development 2.0](../../scrum-programs/concept/scrum-programs-concept.md)**  
Plan and track the work of multiple teams that work together, either toward a common short-term outcome or on an ongoing basis.
-   **[Performance Analytics Content Pack for Agile 2.0](../../../use/dashboards/application-content-packs/pa-content-pack-for-agile-2.0.md)**  
Improve your Agile processes and practices using preconfigured dashboards with data visualizations from the Platform Analytics Content Pack for Agile 2.0.
-   **[Work Progress Status for Agile Teams](../../work-progress-agile/concept/work-progress-status-for-agile-teams.md)**  
The Work Progress Status for Agile Teams application provides you with indicators such as estimated completion date and progress status \(green, yellow, red\) for all your Agile Development 2.0 epics.

**Parent Topic:**[Strategic Portfolio Management](../../it-business-management/reference/r_ITBusinessManagement.md)

