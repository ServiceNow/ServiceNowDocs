---
title: HR Playbook Experience
description: Use Playbook Experiences to select the playbook your company uses.
locale: en-US
release: zurich
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Setting up HR Service Delivery Playbook, Playbook, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# HR Playbook Experience

Use Playbook Experiences to select the playbook your company uses.

The base HR Service Delivery Playbook contains a pre-configured playbook experience.

A Playbook experience is tied to Playbook Configurations and Playbook Activity Overrides.

-   **Playbook Configuration**
    -   Decide if you want the activity state icon on the card.
    -   Determine what fields to use in the Playbook filter.
    -   Determine the maximum number of form fields allowed on a card before a model is used.
    -   Define the conditions to display on the card for the SLA time icon.
-   **Playbook Experiences**

    Controls the playbook user experience.

    -   Sets up display and activity filters.
    -   Provides SLA integration.
    -   Provides access control.
-   **Activity Overrides**

    The base system uses activity overrides to show the list card for requests and the default record card for collapsing and expanding tasks. Activity overrides are also for expanding cards assigned to the user, overdue, SLA breached, and so on that agents see by default.

    Activity overrides control the logic and conditions for cards that are expanded and cards that are collapsed.

    Enables you to override three \(3\) defaults for each card \(from the **What to override** tab\):

    -   The type of card used \(default card, list card, create record card, knowledge card, and so on\).
    -   Expand state \(should this card open by default when playbook loads\).
    -   Roles Required \(should you limit this card to specific roles\).
-   **Activity Actions**

    Defines playbook actions like add using forms, conditions, and scripts, and what buttons appear on a card. You can configure these buttons:

    -   Location, where the buttons appear.
    -   Button type and color.
    -   How the button is implemented \(server script, client action, or a UI component modal\).
    Activity actions also work with displaying buttons and icons that can:

    -   Render a component \(Add Approvers or Close Complete\).
    -   Update the record \(change its state\).

To make changes to the default configurations, see Update playbook experience configurations.

