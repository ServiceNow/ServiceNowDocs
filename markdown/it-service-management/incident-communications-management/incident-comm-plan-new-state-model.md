---
title: Incident communication plan state model
description: Incident communication plan state model helps you to understand the different states through which a plan can progress and track the plan through its states.
locale: en-US
release: yokohama
product: Incident Communications Management
classification: incident-communications-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Explore, Incident Communications Management, IT Service Management]
---

# Incident communication plan state model

Incident communication plan state model helps you to understand the different states through which a plan can progress and track the plan through its states.

Incident communication plans are created with an **Open** state. They follow a process that finishes with the **Closed** or **Canceled** state. The following state model is applicable to new customers starting the Madrid release.

![Stages of an incident communication plan](../image/icm-new-state-model.png "Incident communication plan state model")

The following two properties are responsible for different actions that take place on Incident Communication Plan and Incident Communication Task:

-   The **Close open Incident Communication Plans when Incident is closed or canceled** property \(**com.snc.incident.incident\_alert.closure**\) is responsible for the following action:
    -   When incident is closed, any open Incident Communication Plan is closed.
    -   When an incident is canceled, any open Incident Communication Plan is canceled.
-   The **Close open Incident Communication Tasks when an Incident Communication Plan is closed or canceled** property \(**com.snc.iam.incident\_alert\_task.closure**\) is responsible for the following actions:
    -   If an Incident Communication Plan is **Closed** or **Canceled**, then the state of any open Incident Communication Task on which communication is not yet performed, is set to **Skipped**.
    -   If an Incident Communication Plan is **Closed** or **Canceled**, then the state of any open Incident Communication Task on which communication is performed at least once, is set to **Complete**.

**Note:** The **Close open Incident Communication Plans when Incident is closed or canceled** and **Close open Incident Communication Tasks when an Incident Communication Plan is closed or canceled** property is visible when you activate the Incident Communications Management plugin \(com.snc.iam\). This property is set to false for both new and existing customers.

For more information on the old Incident Communications Plan state model, see [Incident communication plan state model \(old\)](../reference/r_IncidentAlertLifeCycle.md).

