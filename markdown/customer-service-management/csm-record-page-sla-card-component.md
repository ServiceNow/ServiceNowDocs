---
title: Task SLA cards component
description: The Task SLA cards component displays the status of one or more Service Level Agreements \(SLAs\) for the current record in card format.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-12-01"
reading_time_minutes: 1
breadcrumb: [Front-line case page, CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Task SLA cards component

The Task SLA cards component displays the status of one or more Service Level Agreements \(SLAs\) for the current record in card format.

The Task SLA cards component can display multiple SLAs. The cards are displayed in a carousel with horizontal navigation. If more than one SLA card is present, agents can use arrows to scroll through the cards. Within the Task SLA cards component, the case SLA card appears first followed by case task SLA cards.

**Note:** When there are no active SLAs, the Task SLA cards component isn't shown.

![SLA card component with three SLA cards displayed in a carousel. Cards include the SLA name, time remaining and current status.](../image/component-sla-card.png "Task SLA cards component")

The Task SLA cards component is available on the Front-line case page. Previously, the SLA information appeared in the Record Information tab in the contextual side panel. Agents can find SLA information in the left column above the contact and consumer lookup components.

The SLA cards display a visual presentation of SLA information that agents can use to check quickly where they are in the life cycle of the SLA.

-   The SLA card header appears at the top of the card and includes a counter with the number of active SLAs for the case.
-   The SLA name is displayed below the SLA card header.
-   The remaining time is displayed below the SLA name.
-   Agents can expand and collapse the Task SLA cards component by selecting the chevron icon in the SLA card header.
-   Tags on the SLA card indicate the SLA status and either the time remaining or the time elapsed since reaching the Breached state:
    -   **Ongoing**: Is displayed when an SLA starts \(green background\).
    -   **At risk**: Is displayed when 25% of the SLA time is remaining \(yellow background\).
    -   **Breached**: Is displayed when an SLA is violated \(red background\). This tag is displayed in both the SLA card expanded and collapsed states.

