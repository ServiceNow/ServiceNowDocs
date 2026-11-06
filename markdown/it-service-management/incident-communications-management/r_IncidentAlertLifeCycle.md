---
title: Legacy incident communication plan state model
description: The legacy incident communication plan state model defines the states that a plan progresses through, from New to Closed or Canceled, on instances running releases before London.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/r\_IncidentAlertLifeCycle.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Incident communication plan state model, Exploring Incident Communications Management, Incident Communications Management, IT Service Management]
---

# Legacy incident communication plan state model

The legacy incident communication plan state model defines the states that a plan progresses through, from New to Closed or Canceled, on instances running releases before London.

Incident communication plans start in the New state and finish in the Closed or Canceled state.

**Note:** The state model in this topic applies only to releases before the London release. Starting with the London release, see [Incident communication plan state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/incident-comm-plan-new-state-model.md).

\[Omitted image "IncidentAlertStages.png"\] Alt text: Stages of an incident communication plan

The incident communication plan changes from the **New** state to the **Work in Progress** state when you update the **Actions Taken** field. Only the incident communication plan creator or a user with the admin role can cancel an incident communication plan.

The following properties control actions on incident communication plans and incident communication tasks:

-   The **Close open Incident Communication Plans when Incident is closed or canceled** property \(**com.snc.incident.incident\_alert.closure**\) controls the following actions:
    -   If an incident is closed or canceled when the incident communication plan state is **New** or **Work in Progress**, the incident communication plan state is set to **Canceled**.
    -   If an incident is closed or canceled when the incident communication plan state is **Resolved**, the incident communication plan state is set to **Closed**.
-   The **Close open Incident Communication Tasks when an Incident Communication Plan is closed or canceled** property \(**com.snc.iam.incident\_alert\_task.closure**\) controls the following actions:
    -   If an incident communication plan is closed, the state of all open incident communication tasks is set to **Closed Incomplete**.
    -   If an incident communication plan is canceled, the state of all open incident communication tasks is set to **Closed Skipped**.

**Note:** The **Close open Incident Communication Plans when Incident is closed or canceled** and **Close open Incident Communication Tasks when an Incident Communication Plan is closed or canceled** properties are visible when you activate the Incident Communications Management plugin \(com.snc.iam\). Both properties are set to false by default for new and existing customers.

