---
title: Reset a demand to draft state
description: Reset a demand to the Draft state when it has been moved past that state unintentionally or when changes to it are required. A demand can be reset to Draft until an entity is created from it or it has reached the Qualified state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/portfolio-planning/reset-a-demand-to-draft-state-ppw.html
release: australia
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage demands, Use, Next Experience for Demand Management in Portfolio Planning, Portfolio Planning, Strategic Portfolio Management]
---

# Reset a demand to draft state

Reset a demand to the Draft state when it has been moved past that state unintentionally or when changes to it are required. A demand can be reset to Draft until an entity is created from it or it has reached the Qualified state.

## Before you begin

Role required: it\_demand\_manager

## About this task

Once a demand is set back to the Draft state:

-   All score values in the **Assessment Results** tab are reset to default values.
-   All active assessments for the demand are canceled. The system triggers new assessments when the demand moves to the Screening state and if the **Assessment Required** field on the demand form is set to true.
-   All resource assignments are removed. Only the resource plans that don't have any reported active hours are available for allocation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Portfolio Planning Workspace**.

2.  Select the Demands icon \[Omitted image "demands-icon.png"\].

3.  Open a demand from the **List** page.

4.  Select **Details** from the navigation menu.

5.  Select **Reset to Draft**.

    A confirmation message appears if the demand has any of the following.

    -   Active assessments pending with stakeholders.
    -   Resource assignments created for the demand.
6.  Select the check box to replan the allocated resource plans that have no actual hours reported.

7.  Select **OK**.


