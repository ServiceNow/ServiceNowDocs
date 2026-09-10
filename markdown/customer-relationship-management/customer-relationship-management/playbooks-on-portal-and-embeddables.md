---
title: Portal and Embeddables
description: Playbooks can be surfaced on a portal or embedded in a custom page, giving users outside the agent workspace access to a guided, step-by-step process.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-07-07"
reading_time_minutes: 3
---

# Portal and Embeddables

Playbooks can be surfaced on a portal or embedded in a custom page, giving users outside the agent workspace access to a guided, step-by-step process.

The same playbook that agents work through in Configurable Workspace can be made available to customers, constituents, or requesters on a portal — or embedded in a third-party site entirely.

A playbook on a portal or embeddable is organized into stages and activities, just like in Configurable Workspace. Users can see where they are in the process, complete the required tasks at each step, save progress and return later, and track status throughout. The experience is self-guided — users do not need an agent to walk them through it.

Common uses for playbooks on portals or embeddables across CRM products include:

-   A custom intake form embedded on a company website for prospective clients to start an application
-   A requester tracking the progress of an open case or work order through a self-service portal
-   A patient or caregiver completing an enrollment or intake process through a healthcare portal
-   A constituent submitting a benefits request or license renewal through a government service portal
-   A customer completing a multi-step onboarding application on a bank or financial services portal

## Portal playbooks

A portal playbook is an existing playbook that's configured in Workflow Studio and surfaced on a ServiceNow portal page \(such as Customer Service Portal or Consumer Service Portal\). External users — customers, constituents, or requesters — access the playbook directly on the portal. Unlike agents who work through playbooks in Configurable Workspace, portal users see a tailored interface designed for external access. This can be the same playbook that agents use internally, with activity overrides controlling which activities each persona sees — or a separate playbook built for external users, such as an intake-only playbook that hands off to the agent's playbook for the rest of the case.

## Embeddable playbooks

An embeddable playbook is selected in the embeddable Admin app and embedded in an external site, such as a third-party application or website. Users see the playbook interface integrated within that environment.

Examples of embeddable playbook use cases include:

-   A custom intake form embedded on a company website for prospective clients to start an application
-   A playbook embedded in a partner portal to guide partners through a process without leaving their environment
-   A workflow embedded in a mobile app to enable users to complete tasks on-the-go
-   A guided process embedded in a third-party ticketing system for integrated workflow management

## Portal vs embeddable playbooks

Both surface the same playbook to external users. The difference is how the playbook is configured and deployed.

A portal playbook relies on the portal to manage deployment. The playbook logic is built in Workflow Studio, and the setup work happens at the configuration layer — the draft state, record generator, Playbook content item, and Process tab — which is what exposes the playbook to external users. To see how to set this up, see.

An embeddable playbook takes more configuration, because it's embedded in an external environment rather than a standard portal. The playbook page is built in UI Builder, selected in the embeddable Admin app, and then embedded in the external site. It gives greater control over the experience and lets a playbook be integrated into a custom application.

## Guest and public playbooks

Guest and public playbooks allow users who are not logged in or authenticated to access and work through a playbook on a portal or embeddable. This enables a playbook experience for members of the public, prospective customers, or anyone who doesn't have a valid login.

Previously, surfacing a playbook on a portal required the user to be authenticated. Guest/public playbooks remove that requirement, enabling scenarios like:

-   A prospective customer starting a loan application without creating an account first
-   A member of the public submitting a service inquiry anonymously

The playbook itself is the same. The difference is in how the session is managed and how the record is created and associated once the user submits or authenticates later in the flow.

