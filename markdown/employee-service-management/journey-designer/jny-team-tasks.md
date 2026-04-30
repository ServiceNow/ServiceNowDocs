---
title: Team tasks
description: Team tasks enable managers to personalize employee journeys by adding tasks directly to activity sets that are originated by the Lifecycle Events app. Managers can tailor journeys to meet individual employee needs without adding stages or modifying the underlying journey configuration.
locale: en-US
release: zurich
product: Journey Designer
classification: journey-designer
topic_type: concept
last_updated: "2026-01-08"
reading_time_minutes: 3
breadcrumb: [Exploring Journey designer features, Journey designer, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Team tasks

Team tasks enable managers to personalize employee journeys by adding tasks directly to activity sets that are originated by the Lifecycle Events app. Managers can tailor journeys to meet individual employee needs without adding stages or modifying the underlying journey configuration.

Lifecycle Events automate cross-departmental processes during key employee transitions such as onboarding, offboarding, and leave of absence. While these automated workflows address common requirements, managers must often supplement them with tasks specific to their team or individual employees. Team tasks extend the personalization capabilities of Journey Accelerator stages to Lifecycle Events activity sets, giving managers flexibility to customize journeys while preserving the structure that administrators have defined.

Before team tasks, the activity sets and stages that appeared in the Stages widget were grouped separately for journeys that used both Lifecycle Events and Journey Accelerator. Managers could add tasks only to Journey Accelerator stages. Lifecycle Events activity sets were visible but contained HR tasks that were managed through the HR Lifecycle Events case.

Team tasks change this behavior by creating a corresponding Journey Accelerator stage for each Lifecycle Events activity set. The original Lifecycle Events activity set retains its existing functionality, where HR tasks are managed through the HR Lifecycle Events case. The corresponding Journey Accelerator stage enables managers to add Journey Accelerator tasks to what appears in the portal as a Lifecycle Events activity set.

From the manager’s perspective in the Employee Center portal, they can add tasks directly to activity sets. The underlying creation of Journey Accelerator stages isn’t visible in the portal interface, but administrators may observe this structure when configuring or troubleshooting journeys.

## Team tasks functionality

When team tasks is enabled, managers can use the Employee Center to insert tasks into Lifecycle Events activity sets from the Journey detail page. Tasks that managers add are created in a draft status, which means the employee can’t see the tasks that are added until the manager publishes them. This draft-to-publish process gives managers time to review and refine tasks before making them visible to the employee.

Managers can add the following task types to Lifecycle Events activity sets:

-   Add a learning assignment
-   Add a catalog request
-   Add an order guide
-   Complete a general to-do
-   Schedule a meeting

When placing tasks within an activity set, managers can adjust the order of the tasks they add. Managers can also change the order in which the Lifecycle Events activity sets and Journey Accelerator stages appear in the Stages widget. Adding tasks to an activity set doesn’t affect its progress calculation.

## Team tasks benefits

Team tasks reduce complexity for managers by eliminating the need to create additional Journey Accelerator stages when they want to personalize an employee’s journey. Managers can make targeted additions to existing Lifecycle Events activity sets, which streamline the personalization process and reduces overhead.

Team tasks also support the pre-hire phase of employee onboarding. Because Lifecycle Events handles activities that transpire before an employee’s start date, managers can use team tasks to personalize the pre-hire experience in ways that weren’t previously possible.

Organizations using agentic workflows benefit from team tasks as well. When AI agents assist with onboarding personalization, they can recommend tasks for managers to review and publish, extending the capabilities of agentic onboarding beyond Journey Accelerator stages.

## Configuration

Administrators control whether managers can add tasks to activity sets from the Employee Center. Administrators can select the journey configuration for which they want to enable team tasks and subsequently select the **LE activity sets can be personalized** check box to activate the feature.

**Related topics**  


[Enable team tasks](../task/enable-team-tasks.md)

[Add tasks to an activity set using Journey designer](../task/add-tasks-activity-set.md)

