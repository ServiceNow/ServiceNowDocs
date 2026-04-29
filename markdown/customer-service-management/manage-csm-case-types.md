---
title: Manage customer service case types
description: Manage the settings and the configuration for a case type from the Case Type form.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer service case types, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Manage customer service case types

Manage the settings and the configuration for a case type from the Case Type form.

After using the Customer Service Management Guided Setup to create and [configure a case type](../task/configure-csm-case-types.md), you can view and manage the settings and configuration for the case type from the [Case Type form](../reference/customer-service-case-type-form.md). To access a Case Type form, navigate to **Customer Service** &gt; **Case Types** &gt; **Manage Case Types** and select a case type from the list.

## Case Type form related links

The Case Type form includes the following related links.

<table id="table_m43_l53_3kb"><thead><tr><th>

Related link

</th><th>

Description

</th></tr></thead><tbody><tr><td>

View Case Type Configuration

</td><td>

Displays the current configuration for this case type, including:-   Business rules
-   Client scripts
-   Dictionary entries and overrides
-   Notifications
-   UI actions
-   Access controls
-   UI policies
-   Data policies
-   Styles
-   View rules
-   Flows

</td></tr><tr><td>

Launch Guided Setup for Case Types

</td><td>

Goes to the Case Types setup tasks in Customer Service Management Guided Setup.

</td></tr><tr><td>

Launch Guided Setup for AWA

</td><td>

Goes to the Advanced Work Assignment \(AWA\) setup tasks in Agent Workspace Guided Setup.

</td></tr><tr><td>

Launch Guided Setup for Agent Workspace

</td><td>

Goes to the Agent Workspace for CSM setup tasks in Customer Service Management Guided Setup.

</td></tr></tbody>
</table>## Case Type form related lists

The Case Type form related lists display items configured for the case type table. Use the related lists to create additional configurations.

-   Record Producers
-   State Flows
-   Special Handling Notes
-   SLAs
-   Email Templates
-   Quick Messages
-   Reports
-   Case Type Selections

## Select a category and subtype for a case type

The system administrator can assign an optional category and a subtype to a case type. When creating a case, agents can filter the available case types by category and subtype in the [case type selector](csm-case-type-select-modals.md). If an agent selects a category, the list of case types displayed is filtered by that category. If an agent selects a subtype, the list is further filtered by that subtype.

The Customer Service Case Types plugin includes several categories that the system administrator can select for a case type. These categories include:

-   Onboarding
-   Complaint
-   Orders
-   General

The **Subtype** field displays fields from the Case Type table that are of the following type:

-   Choice list
-   Reference

To select a category and a subtype for a case type:

1.  Navigate to **Customer Service** &gt; **Case Types** &gt; **Manage Case Types** and select a case type.
2.  Select a category in the **Category** field.
3.  Select a field in the **Subtype** field.
4.  Select **Update**.

## Case types and major cases

The system administrator can enable the **Propose Major Case** UI action for different case types. If this UI action is available, an agent can propose a major case from the selected case type record. If the major case candidate is accepted, a major case is created and the case type record is added as a child case on the major case.

The major case is created on the base Case table. Updates to the major case are synchronized to the child case types. Multiple case type records can be added to the same major case.

