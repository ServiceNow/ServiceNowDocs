---
title: Scrum and Kanban teams in an ART in EAP
description: Run Scrum and Kanban teams side by side in one Agile Release Train \(ART\) in Enterprise Agile Planning by setting the planning methodology for each Agile Team.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/enterprise-agile-planning/scrum-and-kanban-teams-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 2
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Scrum and Kanban teams in an ART in EAP

Run Scrum and Kanban teams side by side in one Agile Release Train \(ART\) in Enterprise Agile Planning by setting the planning methodology for each Agile Team.

An ART can include teams that work in different ways. Each Agile Team follows one of two planning methodologies, Scrum or Kanban.

## Scrum and Kanban teams comparison

-   **Scrum**

    The team plans work in Sprints. Sprints follow the planning calendar of the team or its ART.

-   **Kanban**

    The team works from a continuous backlog. It has no Sprints, and it doesn't use the shared calendar of its ART.


## Kanban team differences

Because a Kanban team doesn't use Sprints, you see the following differences:

-   **Backlog**

    The **Create next Sprint** button isn't available on the team Backlog.

-   **Sprint creation**

    When you create a Planning Interval for the ART, or add child Sprints, Sprints are created for Scrum teams only. Kanban teams are skipped.

-   **Story forms**

    The **Iteration** field is hidden on the forms of stories assigned to a Kanban team.

-   **Sprint states**

    You can't change the state of a Sprint that belongs to a Kanban team, except to complete or cancel it.

-   **Home tab**

    The **Home** tab of a Kanban team shows the Kanban Team dashboard instead of the Scrum dashboards. For more information, see [Kanban Team dashboard in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/kanban-team-dashboard-in-eap.md).

-   **Planning board**

    The Planning board of an ART doesn't display its Kanban teams, because they don't use iterations. A message indicates that some teams might not be displayed. For more information, see [Perform PI planning in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/pi-planning-eap.md).


## Team planning methodology

The **Planning methodology** field appears above the **Calendar** field on the Agile Team form. New teams default to Scrum. ARTs, Solution Trains, and Portfolios don't have this field.

When you add Agile Teams to an ART, you choose the planning methodology first. The choice applies to all teams that you add in that batch. For more information, see [Define agile structure in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/define-agile-structure-in-eap.md).

## Methodology after an upgrade

When you upgrade, existing Agile Teams that have a calendar of their own or a calendar from their configuration are set to Scrum. All other existing Agile Teams are set to Kanban.

## Team methodology changes

To move a team from Scrum to Kanban, see [Switch an Agile Team to Kanban in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/enterprise-agile-planning/switch-agile-team-to-kanban-in-eap.md). Switching a Scrum team to Kanban cancels the current and future Sprints of the team.

