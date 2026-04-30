---
title: Stage fields
description: The Stage field on the Ideas list displays the current state of an idea as it moves through the demand life cycle. The current state includes from an idea to a demand and then to the resulting project, enhancement, change, or defect.
locale: en-US
release: zurich
product: Demand Management
classification: demand-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Stage fields

The Stage field on the Ideas list displays the current state of an idea as it moves through the demand life cycle. The current state includes from an idea to a demand and then to the resulting project, enhancement, change, or defect.

The result of an idea depends on the initial settings in the **Category** and **Type** fields on the Demand form. The **Stage** field also appears on the Demands list. The **Stage** field is a display only field and can’t be searched or sorted.

**Important:** The **Stage** fields are no longer available starting from the New York release. Any instance provisioned in New York or later won’t have a Stage field on the Idea table. However, the **Stage** fields are available if you’re upgrading from an older release to New York or later.

A new idea is created in the **Submitted** state. An accepted idea is updated to the **Accepted** state and a deferred idea is updated to the **Skipped** state. When a demand is closed, the associated idea is marked as **Complete**.

Hovering over the **Stage** field displays a pop-up window that shows the progression of the idea along with the value of the **State** field for each step in the progression.

-   **Idea:** if an idea is being evaluated, the pop-up window displays the current state of the idea.
-   **Demand:** if an idea is promoted to a demand, the pop-up window displays the current state of the demand as well as the idea.
-   **Project**, **Enhancement**, **Change**, or **Defect**: if a demand is accepted, the pop-up window displays the current state of the resulting project, enhancement, change, or defect in addition to the demand and idea.

![Stage fields summary pop-up window.](../image/demand-stage-fields.png)

**Parent Topic:**[Demand Management reference](../../service-portfolio-management2/concept/demand-management-reference.md)

