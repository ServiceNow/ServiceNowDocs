---
title: Incident communication plan state model \(old\)
description: Incident communication plan state model helps you to understand the different states through which a plan can progress and also to track the plan through its states.
locale: en-US
release: zurich
product: Incident Communications Management
classification: incident-communications-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Incident communication plan state model, Explore, Incident Communications Management, IT Service Management]
---

# Incident communication plan state model \(old\)

Incident communication plan state model helps you to understand the different states through which a plan can progress and also to track the plan through its states.

Incident alerts are created with a **New** state. They follow a process that finishes with the **Closed** or **Canceled** state.

**Note:** The state model shown below is available only for customers prior to the London release. Beginning London release, customers who have upgraded to the latest release, can refer to [Incident communication plan state model](../concept/incident-comm-plan-new-state-model.md).

![Stages of an incident communication plan](../image/IncidentAlertStages.png "Incident communication plan stages")

The incident communication plan changes from the **New** state to the **Work in Progress** state when you update the **Actions Taken** field. Only the incident communication plan creator or a user with the admin role can cancel an incident communication plan.

The following two properties are responsible for different actions that take place on Incident Communication Plan and Incident Communication Task:

-   The **Close open Incident Communication Plans when Incident is closed or canceled** property \(**com.snc.incident.incident\_alert.closure**\) is responsible for the following actions:
    -   If an incident is closed or canceled when the incident communication plan state is **New** or **Work in Progress**, the incident communication plan state is set to **Canceled**.
    -   If an incident is closed or canceled when the incident communication plan state is **Resolved**, the incident communication plan state is set to **Closed**.
-   The **Close open Incident Communication Tasks when an Incident Communication Plan is closed or canceled** property \(**com.snc.iam.incident\_alert\_task.closure**\) is responsible for the following actions:
    -   If an incident communication plan is closed, the state of all open incident communication tasks is set to **Closed Incomplete**.
    -   If an incident communication plan is canceled, the state of all open incident communication tasks is set to **Closed Skipped**.

**Note:** The **Close open Incident Communication Plans when Incident is closed or canceled** and **Close open Incident Communication Tasks when an Incident Communication Plan is closed or canceled** property is visible when you activate the Incident Communications Management plugin \(com.snc.iam\). This property is set to false for both new and existing customers.

