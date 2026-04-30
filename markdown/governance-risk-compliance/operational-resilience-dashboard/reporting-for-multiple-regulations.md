---
title: Reporting incidents or security incidents for multiple regulations
description: You can now report incidents or security incidents for multiple regulations for various legal entities in Digital resilience incident reporting. The application streamlines operations by automating tasks, migrating data, helping to prevent duplicates, and verifying accurate reporting.
locale: en-US
release: xanadu
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: concept
last_updated: "2025-11-17"
reading_time_minutes: 3
breadcrumb: [Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Reporting incidents or security incidents for multiple regulations

You can now report incidents or security incidents for multiple regulations for various legal entities in Digital resilience incident reporting. The application streamlines operations by automating tasks, migrating data, helping to prevent duplicates, and verifying accurate reporting.

## Automated reporting workflow

Starting with Digital resilience incident reporting, release 21.1.1, the application uses an automated reporting workflow to generate reports within regulatory reporting timelines:

-   Regulatory reporting assessment of IT incidents
-   Initial Report \(within 24 hours\)
-   Intermediate Report \(every three days until resolved\)
-   Final Report

You can complete these tasks and generate reports in Microsoft Word format, as required by regulatory authorities for analysis.

## Case creation by adding entities

Digital resilience incident reporting is used for incident reporting and assessment for legal entities or other objectives according to regulations. You can now add entities to an incident, which automatically create a Digital resilience incident reporting case.

For information on setting up the entities, see [Set up entities for the targets](../task/set-up-entities-for-targets.md).

## Sequence of action tasks

The sequence of action tasks in the Digital Resilience Incident Reporting \(DIR\) process, as outlined in the document "Digital resilience incident reporting for multiple regulations," is primarily driven by template configurations. Here's an overview of how action tasks are created and sequenced:

Action task creation and sequence are explained:

1.  Initial action task creation: When a DIR case is created \(triggered by sources like incidents\), the system automatically generates action tasks. For example, the template shown creates the 'Regulatory reporting assessment of IT incidents' action task.
2.  Template configuration: Templates are configured to create specific action tasks. For example, the 'DRI Initial report' template, which runs only once, automatically creates the 'DRI Initial report' action task when the regulation’s reporting status changes to 'Reportable.' Administrators can then update its name, due date, and termination conditions.
3.  Closure of action tasks: When the 'DRI Initial report' is closed, the 'DRI Intermediate report' action task is created. If the 'DRI Initial report' task remains open, the system creates the 'DRI Intermediate report' action task every three days until the DIR case is closed or canceled, or the source incident is closed.
4.  Closure of incident: When the source incident or security incident is closed, the “DRI Final report” action task is created, with a due date of 30 days.
5.  Automated action task generation: These template configurations enable automatic creation of action tasks, as previously demonstrated. as administrators, you can create multiple action tasks and tailor their sequence to meet your organizational requirements and applicable regulations.
6.  Completion of action tasks: Action tasks are completed according to the conditions defined in their templates, promoting efficient process management and required task completion.

    **Note:** As administrators, you can customize the configurations available with the base version or add additional action tasks as needed.


For information on mapping regulations and setting up action task templates, see [Map regulations to the entities](../task/configure-case-types-map-regu.md) and [Set up action task templates in Regulatory agency profile](../task/set-up-action-task-templates.md).

For information on completing action tasks, refer to [Complete action tasks and report incidents associated with regulations](../task/work-on-action-tasks.md).

