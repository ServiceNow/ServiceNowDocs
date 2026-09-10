---
title: Playbooks patterns
description: Build a working playbook by combining Workflow Studio, the Playbook canvas, and UI Builder to produce a specific runtime experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/playbook-patterns.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-08-31"
reading_time_minutes: 2
breadcrumb: [Playbooks, Workflow Studio, Build workflows]
---

# Playbooks patterns

Build a working playbook by combining Workflow Studio, the Playbook canvas, and UI Builder to produce a specific runtime experience.

Most playbook configuration is documented by tool: you configure prerequisites, build a process definition on the canvas, then design how the process appears at runtime. Some playbooks require a specific sequence of choices across all three tools, where a decision made in Workflow Studio determines the options available later in UI Builder. These playbooks are documented as patterns.

The following patterns are available:

-   **[Guided Decision playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/configure-a-guided-decision-playbook.md)**

    Configure a Guided Decision Playbook to walk users through decision-driven questions and actions toward a recommended outcome, delivered as a seamless runtime experience running standalone or inside another playbook. The Guided Layout removes the activity and stage pickers and consolidates previous responses into an accordion.

-   **[Nested playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/nested-playbooks.md)**

    Embed or "nest" a child playbook within a parent playbook to organize your processes and then present the appropriate sequence of steps in the runtime experience. Creating child playbooks that can be used in other parent playbooks enables you to define sets of activities that can be re-used across multiple playbooks to avoid duplication.

-   **[Wizard layout playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/configure-wizard-layout-playbook.md)**

    Build a wizard-driven Playbook to present a playbook as a guided, step-by-step experience that walks end users through a process one activity at a time. The Wizard layout adds numbered step navigation and forward and back controls to a standard playbook.

-   **[Guest user access playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/configure-guest-user-access.md)**

    Set up a playbook, public audience record, and UI experience so that guest users can run playbooks without a ServiceNow login through a public URL.


Each pattern topic describes the intended use of the pattern, its prerequisites, its constraints, and the configuration sequence across Workflow Studio, the canvas, and UI Builder. Constraints that limit functionality available to standard playbooks are stated at the point of configuration.

**Related topics**  


[Building Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/building-a-process.md)

[Designing Playbook Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-experience-admins.md)

