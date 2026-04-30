---
title: Service level agreements for government service cases
description: A service level agreement \(SLA\) is a record that you use to guarantee a specific time that a service or information must be provided by, or that an agent must finish a task must by. The Public Sector Digital Services application uses SLAs with government service request cases.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Government Service Portal, Portals, Use, Public Sector Digital Services \(PSDS\)]
---

# Service level agreements for government service cases

A service level agreement \(SLA\) is a record that you use to guarantee a specific time that a service or information must be provided by, or that an agent must finish a task must by. The Public Sector Digital Services application uses SLAs with government service request cases.

You can attach an SLA to a service request in the Government Service Portal or to a service request in the Service Request Playbook. You can configure an SLA to start, pause, or stop depending on any government service case attributes that you or someone else assigned to the SLA.

An SLA is automatically associated to a case when the case is created or updated depending on the conditions that have been set up in the SLA definition. The specific record that gets attached to a case is the Task SLA record, which tracks the SLAs for that particular case. The Task SLA table \[task\_sla\] stores the Task SLA records. For more information on SLA definitions, see [Service Level Agreement \(SLA\) definition](https://www.servicenow.com/docs/access?context=c_SLADefinitions&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

An SLA sends notifications at certain events that are defined in the workflow. For information on defining SLA workflow events, see [Create an SLA definition](https://www.servicenow.com/docs/access?context=t_CreateAnSLADefinition&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

By default, SLA notifications are triggered and sent to the assigned agent on the following occasions:

-   A Service Request case is in the Intake stage for more than two days.
-   A Service Request case is in the Review stage for more than eight days.
-   A Service Request case is in Processing stage for more than eight days.
-   A Service Request case is in the Decision stage for more than two days.
-   A constituent's comment or query hasn’t been responded to for two days.
-   An SLA is at 50 percent of the duration that is specified in the SLA definition.
-   An SLA is at 75 percent of the duration that is specified in the SLA definition. A notification is sent to the agent and agent manager.
-   An SLA is breached. A notification is sent to the agent and agent manager.

An SLA's timer pauses when the case is awaiting information from the constituent who had a comment or query. The timer is canceled if the state of the case changes to **Closed** or **Cancelled**.

To learn more about SLAs, see [Service Level Management concepts](https://www.servicenow.com/docs/access?context=service-level-management-concepts&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

