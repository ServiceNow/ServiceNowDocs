---
title: Playbooks in Recommended Actions
description: Playbooks are interactive, step-by-step guided workflows that help agents make decisions and resolve issues faster. Configure playbooks as recommended actions to deliver contextual guidance directly in the Recommended Actions Contextual Side Panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ra-playbooks.html
release: australia
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 1
keywords: [Playbooks in Recommended Actions, Recommended Actions, Playbooks action type, Create playbooks action type in Recommended Actions]
breadcrumb: [Recommended Actions, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Playbooks in Recommended Actions

Playbooks are interactive, step-by-step guided workflows that help agents make decisions and resolve issues faster. Configure playbooks as recommended actions to deliver contextual guidance directly in the Recommended Actions Contextual Side Panel.

For more information on playbooks, see [Playbooks in Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setting-up-csm-playbooks.md).

## Key concepts

-   **Playbook action type**

    The Playbooks action type that enables authors and admins to add and configure playbooks as recommended actions. Admins configure and publish playbooks, and set launch behavior. Agents see playbooks as cards in the Suggested Actions tab of the RA panel in the Agent Workspace and can execute them inline with minimal tab switching.

-   **Launch mode**

    The behavior that determines how a playbook opens when an agent selects the **Launch** button on the Playbook card in the Recommended Actions panel in the Agent Workspace. Options include Launch in side panel \(opens playbook in the side panel\) and Launch in expanded view \(opens playbook in a related tab\).

-   **Playbook execution state**

    The shared execution context of a playbook across users and sessions. When a playbook completes, the system automatically marks the related recommended action as completed. Multiple agents viewing the same recommended action see a synchronized playbook state.

-   **Execution history**

    A record of past playbook executions, including outputs and timestamps. Agents can review execution history under Recommended Actions history to understand prior resolutions.


## What you can do with playbooks in Recommended Actions

As an admin, you can perform the following on the playbooks in Recommended Actions:

-   Add playbooks as a new action type when authoring recommended actions.
-   Execute playbooks directly from the Recommended Actions panel without switching between the tabs.
-   Monitor playbook completion and synchronize state across team members.
-   Review execution history for audit and training purposes.

