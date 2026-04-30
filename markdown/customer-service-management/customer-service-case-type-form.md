---
title: Case Type form
description: Use the Case Type form to manage the settings for a case type.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Customer Service forms, Customer Service Management reference, Customer Service Management]
---

# Case Type form

Use the Case Type form to manage the settings for a case type.

To access a Case Type form, navigate to **Customer Service** &gt; **Case Types** &gt; **Manage Case Types** and select a case type from the list.

<table id="table_fyv_dtr_bs"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Table

</td><td>

The table for the case type that extends the Case table \(sn\_customerservice\_case\).

</td></tr><tr><td>

Category

</td><td>

An optional category for a case type. When creating cases, customer service agents can filter the available case types by category in the Select Case Type popup window. The Customer Service Case Types plugin \(com.snc.csm\_case\_types\) includes the following categories:

-   Onboarding
-   Complaint
-   Orders
-   General

</td></tr><tr><td>

Subtype

</td><td>

An optional sub-category for a case type. When creating cases, customer service agents can filter the available case types by category and then by subtype in the Select Case Type popup window. The **Subtype** field displays fields from the selected **Table** that are of the following type:

-   Choice list
-   Reference

</td></tr><tr><td>

Short description

</td><td>

A brief description of the case type.

</td></tr></tbody>
</table>## Related links

The Case Type form includes the following related links:

-   **View Case Type Configuration**: View the current configuration for this case type table.
-   **Launch Guided Setup for Case Types**: Go to the Case Types setup tasks in Customer Service Guided Setup.
-   **Launch Guided Setup for AWA**: Go to the Advanced Work Assignment \(AWA\) setup tasks in Agent Workspace Guided Setup.
-   **Launch Guided Setup for Agent Workspace**: Go to the Agent Workspace for CSM setup tasks in CSM Guided Setup.

## Related lists

The Case Type form related lists display items configured for the case type table. Use the related lists to create additional configurations.

-   Record Producers
-   State Flows
-   Special Handling Notes
-   Notification Triggers
-   SLAs
-   Email Templates
-   Quick Messages
-   Reports

