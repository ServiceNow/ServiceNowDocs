---
title: Fundamentals
description: Playbooks are built from a set of core components that work together to guide users through a business process.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-07-06"
reading_time_minutes: 2
keywords: [Playbooks basics, understanding playbooks, playbook fundamentals]
---

# Fundamentals

Playbooks are built from a set of core components that work together to guide users through a business process.

## Stages and activities

A playbook is organized into stages and activities. Each stage contains a group of activities to complete before the process moves forward. Activities can be manual tasks or form entries, automated system actions that run without agent input, or guided decisions that present structured questions to a recommended next action.

A playbook also includes a trigger, which determines when the playbook starts running. Each trigger has conditions that, when met, start the playbook — for example, when a record is created or updated.

## Where playbooks are used

Playbooks can be surfaced in several environments depending on who needs to interact with the process.

-   **Playbook on Configurable Workspace:** The workspace experience is built from pages, templates, and components that control what users see and how they interact with a playbook. Administrators configure this in UI Builder — selecting a page template, activating it, and customizing its components. For more information, see.
-   **Playbook on Portal:** Guide customers through a self-service intake process on your company's service portal. Customers see the playbook stages and save their progress in Draft state until they submit. Configured by creating playbook content items. For more information, see.
-   **Playbook Embeddables:** Embed a playbook component inside a custom UI Builder page, a third-party application, or an external website. Configured by mapping the playbook page into the target page collection within UI Builder. For more information, see.

## How playbooks are built

Building and configuring playbooks requires three main tools, each serving a different part of the process.

-   **Workflow Studio** is where the playbook logic is defined — the stages, activities, branching logic, and conditions that drive the process forward. This is the backbone of any playbook.
-   **UI Builder** is where how the playbook looks and feels in the workspace is designed. Select a page template, activate it, and then customize the layout and components to match your organizational needs. The UI layer is separate from the playbook logic so the visual experience can be changed without touching the underlying workflow.
-   **Platform** is where underlying activity definitions, UI layouts, and configuration records that power playbook automations and custom activities are managed.

This three-tool approach means playbook logic, presentation, and configuration can each be managed independently, making it easier to update processes and maintain consistency across records.

**Related topics**  


[Playbooks for Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/playbooks.md)

[Playbooks for Financial Services Operations applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/playbooks-fso-apps.md)

[Playbooks for Public Sector Digital Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/playbooks-psds-exploring.md)

[Configuring playbooks for Patient Support Services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/pss-config-playbook.md)

[Customer Engagement Sequences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-customer-engagement-sequences.md)

