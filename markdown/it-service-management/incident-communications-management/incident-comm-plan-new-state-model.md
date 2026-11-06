---
title: Incident communication plan state model
description: The incident communication plan state model defines the states that a plan progresses through, so you can track a plan from creation to closure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-communications-management/incident-comm-plan-new-state-model.html
release: australia
product: Incident Communications Management
classification: incident-communications-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Exploring Incident Communications Management, Incident Communications Management, IT Service Management]
---

# Incident communication plan state model

The incident communication plan state model defines the states that a plan progresses through, so you can track a plan from creation to closure.

Incident communication plans are created with an **Open** state. They follow a process that finishes with the **Closed** or **Canceled** state. The following state model is applicable to new customers starting with the Madrid release.

\[Omitted image "icm-new-state-model.png"\] Alt text: Diagram showing Open state transitioning to either Closed or Canceled.

The following properties control actions on incident communication plans and incident communication tasks:

-   The **Close open Incident Communication Plans when Incident is closed or canceled** property \(**com.snc.incident.incident\_alert.closure**\) is responsible for the following action:
    -   When an incident is closed, any open Incident Communication Plan is closed.
    -   When an incident is canceled, any open Incident Communication Plan is canceled.
-   The **Close open Incident Communication Tasks when an Incident Communication Plan is closed or canceled** property \(**com.snc.iam.incident\_alert\_task.closure**\) is responsible for the following actions:
    -   If an Incident Communication Plan is **Closed** or **Canceled**, then the state of any open Incident Communication Task on which communication is not yet performed is set to **Skipped**.
    -   If an Incident Communication Plan is **Closed** or **Canceled**, then the state of any open Incident Communication Task on which communication is performed at least once is set to **Complete**.

**Note:** The **Close open Incident Communication Plans when Incident is closed or canceled** and **Close open Incident Communication Tasks when an Incident Communication Plan is closed or canceled** properties are visible when you activate the Incident Communications Management plugin \(com.snc.iam\). These properties are set to false for both new and existing customers.

For details about the earlier incident communication plan state model, see [Legacy incident communication plan state model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-communications-management/r_IncidentAlertLifeCycle.md).

