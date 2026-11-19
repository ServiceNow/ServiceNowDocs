---
title: Reporting incidents for multiple regulations
description: You can now report incidents or security incidents for multiple regulations for various legal entities in Digital resilience incident reporting. The application streamlines operations by automating tasks, migrating data, helping to prevent duplicates, and verifying accurate reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/reporting-for-multiple-regulations.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Manage, Using Digital resilience incident reporting, Manage, Operational Resilience, Governance, Risk, and Compliance]
---

# Reporting incidents for multiple regulations

You can now report incidents or security incidents for multiple regulations for various legal entities in Digital resilience incident reporting. The application streamlines operations by automating tasks, migrating data, helping to prevent duplicates, and verifying accurate reporting.

## How reporting for multiple regulations works

An incident or security incident can affect several legal entities, and each entity can be subject to one or more regulations. The application handles this as follows:

-   Each entity that you add to an incident or security incident is mapped to the regulations that apply to it.
-   The application creates a single Digital resilience incident reporting case for the incident and adds a regulation record to the case for each mapped regulation. You can also add a regulation to a case manually from the Regulations related list on the case.
-   The application tracks the reporting status of each regulation record separately.
-   The application creates action tasks, such as the initial, intermediate, and final reports, for each regulation from the action task templates that are configured for that regulation. Each regulation therefore follows its own reporting sequence.

For example, a case can list two regulations, with one marked as Reportable and the other as Non-reportable. You then complete only the reports that apply to the Reportable regulation.

## Automated reporting workflow

Starting with Digital resilience incident reporting, release 21.1.1, the application uses an automated reporting workflow to generate reports within regulatory reporting timelines:

-   Regulatory reporting assessment of IT incidents
-   Initial Report \(within 24 hours\)
-   Intermediate Report \(every three days until resolved\)
-   Final Report

You can complete these tasks and generate reports in Microsoft Word format, as required by regulatory authorities for analysis.

**Note:** If you upgrade to release 21.1.1 or later from a release that supported only the Digital Operational Resilience Act \(DORA\), existing DORA cases are migrated automatically. A DORA regulation record is created on each existing case, and the reporting status of the case is carried over to it.

## Case creation by adding entities

Digital resilience incident reporting is used for incident reporting and assessment for legal entities or other objectives according to regulations. You can now add entities to an incident, which automatically create a Digital resilience incident reporting case.

**Note:** When an entity is mapped to an incident or security incident, the 'DRI case creation on incident entity insert' or 'DRI case creation on SIR entity insert' flow runs and a Digital Resilience Incident Reporting case is created automatically in the Digital Resilience Incident Reporting module with the prebuilt flow. For information on the flows, see [Configure Digital resilience incident reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/workflow-confi-auto-trigger-inci-repo-cases.md).

You cannot add the same entity to the same incident or security incident more than once. If you try, the application displays an error message and does not save the duplicate.

For information on setting up the entities, see [Add entities to an incident or security incident](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/set-up-entities-for-targets.md).

## Reporting status for each regulation

Each regulation on a case has its own reporting status. The status can be To be determined \(the default\), Reportable, Non-reportable, or Potentially reportable. When the status of a regulation changes to Reportable, the application creates the Initial report action task for that regulation.

**Note:** If you send a regulatory reporting assessment of IT incidents task back to Work in progress from Review, the reporting status of all regulations on the case is reset to Potentially reportable. Reassess each regulation before you continue.

## Sequence of action tasks

The sequence of action tasks in the DIR process is outlined in the document "Digital resilience incident reporting for multiple regulations." It is primarily driven by template configurations. Here's an overview of how action tasks are created and sequenced:

The sequence runs separately for each regulation on the case, using the action task templates that are configured for that regulation. A regulation creates action tasks only if templates are configured for it. Out of the box, the templates are configured for the Digital Operational Resilience Act \(DORA\). For other regulations, you configure the templates yourself. When the source incident or security incident is closed, a Final report action task is created for each regulation that has an active Final report template. This applies regardless of the reporting status of the regulation.

Action task creation and sequence are explained.

1.  Initial action task creation: When a DIR case is created \(triggered by sources like incidents\), the system automatically generates action tasks. For example, the template shown creates the 'Regulatory reporting assessment of IT incidents' action task.
2.  Template configuration: Templates are configured to create specific action tasks. For example, the 'DRI Initial report' template runs only once. It automatically creates the 'DRI Initial report' action task when the regulation’s reporting status changes to 'Reportable.' Administrators can then update its name, due date, and termination conditions.
3.  Closure of action tasks:

    When the 'DRI Initial report' is closed, the 'DRI Intermediate report' action task is created. If the 'DRI Initial report' task remains open, the 'DRI Intermediate report' action task is created every three days until the DIR case or source incident is closed.

    **Note:** It is not mandatory to close every intermediate report assessment that was generated during the lifecycle of the incident. The Final report action task is created automatically when the source incident is closed, independent of the open intermediate assessments. Any intermediate assessments that remain open after the source incident is closed are no longer required - the periodic generation stops as soon as the termination conditions configured on the DRI Intermediate report template are met \(typically when the source incident state is 'Closed' or the DRI case state is 'Closed'/'Canceled'\).

4.  Closure of incident: When the source incident or security incident is closed, the “DRI Final report” action task is created, with a due date of 30 days.
5.  Automated action task generation: These template configurations enable automatic creation of action tasks, as previously demonstrated. as administrators, you can create multiple action tasks and tailor their sequence to meet your organizational requirements and applicable regulations.
6.  Completion of action tasks: Action tasks are completed according to the conditions defined in their templates, promoting efficient process management and required task completion.

    **Note:** As administrators, you can customize the configurations available with the base version or add additional action tasks as needed.


For information on mapping regulations and setting up action task templates, see [Map regulations to the entities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/configure-case-types-map-regu.md) and [Set up action task templates in Regulatory agency profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/set-up-action-task-templates.md).

For information on completing action tasks, refer to [Complete action tasks and report incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/work-on-action-tasks.md).

