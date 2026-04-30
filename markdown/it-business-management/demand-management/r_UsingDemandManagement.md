---
title: Use Demand Management
description: Users with the demand manager role can create, view, and modify demands using the Demand Management application.
locale: en-US
release: xanadu
product: Demand Management
classification: demand-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Demand Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Use Demand Management

Users with the demand manager role can create, view, and modify demands using the Demand Management application.

You can also approve demands and create the following artifacts from the approved demands:

-   Project
-   Change
-   Enhancement
-   Defect

The type of artifact created from a demand depends on the selections in the **Category** and **Type** fields on the Demand form. Enhancements and defects can be created when the system administrator has activated the SDLC-SCRUM plugin.

## Demand Management Life Cycle

The demand management life cycle can be simplified as follows:

-   [Creating a demand](../task/t_CreatingDemands.md): The user submits an idea and the demand manager approves the idea, automatically creating a demand from that idea.
-   [Viewing a list of demands](../task/t_ViewDemands.md): The demand manager views demands on the [demand workbench](../concept/c_DemandWorkbench.md) or from a list view.
-   [Enhancing a demand](../concept/c_EnhancingDemands.md): The demand manager can send the demand to screening, which sends assessments to stakeholders.
-   [Assessing a demand](../concept/c_AssessingDemands.md):
    -   The demand manager can screen the demand and send surveys to stakeholders to complete assessments.
    -   The demand manager can set the state of the demand to qualify, defer, or incomplete.
    -   Demands can be analyzed and approved using the demand workbench.
-   Creating an artifact: The demand manager creates a project, enhancement, change, or defect.

The demand management application uses the following simplified demand states.

<table id="tbl_DemandManagementStates"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

The demand manager accepts a submitted idea.After reviewing or editing the record, click one of these buttons:

-   **Update**: The demand record is updated, but the demand remains in the current state.
-   **Submit demand**: The demand is moved to the submitted state.
-   **Delete**: The demand record is deleted.

</td></tr><tr><td>

Submitted

</td><td>

An accepted idea creates a demand record and the demand manager submits the demand.After reviewing or editing the record, click one of these buttons:

-   **Update**: The demand record is updated, but the demand remains in the current state.
-   **Screen**: The demand is moved to the screening state.
-   **Qualify** The demand is moved to the qualified state.
-   **Defer**: The demand is moved to the deferred state.
-   **Incomplete**: The demand is moved to the incomplete state.
-   **Delete**: The demand record is deleted.

</td></tr><tr><td>

Screening

</td><td>

The demand initiates assessments for the demand. After reviewing or editing the record, click one of these buttons:

-   **Update**: The demand record is updated, but the demand remains in the current state.
-   **Qualify** The demand is moved to the qualified state.
-   **Defer**: The demand is moved to the deferred state.
-   **Delete**: The demand record is deleted.

</td></tr><tr><td>

Qualified

</td><td>

The demand has been qualified and is ready for review.After reviewing the record, click one of these buttons:

-   **Update**: The demand record is updated, but the demand remains in the current state.
-   **Approve**: The demand is moved to the approved state.
-   **Defer**: The demand is moved to the deferred state.
-   **Delete**: The demand record is deleted.

</td></tr><tr><td>

Deferred

</td><td>

The demand has been put on hold. The demand can be revisited in future and reviewed.After reviewing the record, click one of these buttons:

 -   **Update**: The demand record is updated, but the demand remains in the current state.
-   **Approve**: The demand is moved to the approved state.
-   **Reset to Draft**: The demand is moved back to the draft state.
-   **Delete**: The demand record is deleted.

</td></tr><tr><td>

Approved

</td><td>

The demand is approved After reviewing or editing the record, click one of these buttons:

-   **Update**: The demand record is updated, but the demand remains in the current state.
-   **Close**: The demand is moved to the closed state.
-   **Delete**: The demand record is deleted.

</td></tr><tr><td>

Completed

</td><td>

The demand is moved to the completed state.

</td></tr></tbody>
</table>These states appear in the process flow indicator at the top of the Demand form. The process flow indicator:

-   Highlights the current state of the demand.
-   Checks off the states that a demand has passed through.
-   Leaves blank the states that have been skipped.

In this example, the demand is in the **Approved** state. It passed through the **Draft**, **Submitted**, and **Qualified** states but skipped the **Screening** state.

![Demand process flow indicator](../image/DemandProcessFlowIndicator.png)

-   **[Assess demands](../concept/c_AssessingDemands.md)**  
The Demand Management application comes with two demand visualization tools that can aid decision makers with demand assessment.
-   **[Create a demand](../task/t_CreatingDemands.md)**  
Create demands to capture your strategic and operational requirements and centralize information for stakeholder assessment and prioritization.
-   **[View demands](../task/t_ViewDemands.md)**  
You can view existing demands at any time.
-   **[Add details to demands](../concept/c_EnhancingDemands.md)**  
The demand manager typically works with a business relationship manager to identify stakeholders and elicit requirements, risks, and other important information.
-   **[RIDAC \(Risk, Issue, Decision, Action, and Request Changes\) record entries for a demand](../concept/ridac-entries-for-demand.md)**  
RIDAC is an acronym for Risk, Issue, Decision, Action, and Request Changes records. Create a risk record for your demand that you can convert to other records during the demand life cycle to track issues and to avoid having to manually copy relevant details in related records.
-   **[Reset a demand to Draft state](../task/reset-demand-to-draft-state.md)**  
A demand can be moved back to Draft state, if required.
-   **[Delete demands](../task/t_DeletingDemands.md)**  
Demands can be deleted only while in the Pending state.
-   **[Move and resize a demand](../task/t_MoveAndResizeADemand.md)**  
As the demand manager, you can move and resize bubbles in the bubble chart.
-   **[Train the similarity solution for Demand Management to find similar demands](../task/train-similarity-solution-dm.md)**  
Train the Similar Demands solution definition included within the Predictive Intelligence for PPM capability to find related demands when creating a demand.
-   **[PPM PIWB template - Find similar demands](../../itbm-PI-workbench/task/ppm-piwb-demand.md)**  
Use a guided template that walks you through training the Similar Demands solution definition for finding similar demands.

**Parent Topic:**[Demand Management](../concept/c_DemandManagement.md)

