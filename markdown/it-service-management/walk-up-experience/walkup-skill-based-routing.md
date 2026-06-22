---
title: Configure skill-based routing in Walk-up Experience
description: Route work items to assigned groups. Use skill-based routing to ensure that the right work goes to the right agent depending on the walk-up reasons.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/walk-up-experience/walkup-skill-based-routing.html
release: zurich
product: Walk-Up Experience
classification: walk-up-experience
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Walk-up Experience, IT Service Management]
---

# Configure skill-based routing in Walk-up Experience

Route work items to assigned groups. Use skill-based routing to ensure that the right work goes to the right agent depending on the walk-up reasons.

Identify skills for a specific set of conditions defined for walk-up reasons. Use business rules to automatically add the skills to those types of work items. In the Walk-up Experience application, the work items get automatically assigned to the right agents based on the skills.

-   When a new walk-up interaction is opened trough the check-in portal or booking an appointment, Advanced Work Assignment routes the interactions to agents who have the skill set required to address the reason for interaction.
-   The administrators must activate **Skill determination for interaction** BR on interaction table for Advanced Work Assignment to route interactions based on the agent's skills.
-   New interactions opened after the set up are routed to the available agent with the respective skills.
-   If an agent is unavailable and the interaction does not need any mandatory skills, the walk-up task is routed based on the assignment rule associated with the location.

For more information, see [Skills Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/skills-management/skills-management.md)

-   **[Route walk-up tasks to skilled agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/walk-up-experience/walkup-routing-tasks-to-skilled-agents.md)**  
Use business rules to automatically route walk-up tasks to the agents based on their skill set.

**Parent Topic:**[Configuring Walk-up Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/walk-up-experience/walkup-experience-configuration.md)

