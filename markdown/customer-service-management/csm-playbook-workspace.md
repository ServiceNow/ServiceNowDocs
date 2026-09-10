---
title: Workspace
description: In CRM Workspace, a playbook appears on a record page that is built from components. These components can be customized to fit how agents work through and resolve cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-playbook-workspace.html
release: australia
topic_type: concept
last_updated: "2026-07-21"
reading_time_minutes: 2
breadcrumb: [Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Workspace

In CRM Workspace, a playbook appears on a record page that is built from components. These components can be customized to fit how agents work through and resolve cases.

The playbook components and configuration options work together within CRM Workspace to shape the agent's experience:

-   The components provide the parts an agent uses to resolve a case, such as the stage picker, activity viewer, and contextual side panel.
-   Customization controls which of those components appear, how they are arranged, and how they behave, so a page can be tailored to a specific case type or team.

Starting from the same set of components, an administrator can build a focused page for a complaint case or a more detailed one for a product support case, without changing what the components do.

## Role of CSM Workspace

-   **In an agent's workflow**: Configurable Workspace is where an agent resolves a case. A case can reach an agent from different channels, such as a phone call, an email, or a request submitted from a portal. When the agent opens the case, the playbook guides them through the steps to resolve it, while the side panel, lookup, and case summarization tools keep the information they need in the same place. This lets an agent move from reviewing a case to resolving it without switching to another tool.
-   **In a playbook**: The workspace is the agent-facing side of a playbook. A playbook is created once in Workflow Studio, where its trigger, stages, and activities are defined. That same playbook can then appear in more than one place, such as in Configurable Workspace for agents or on a portal for customers. The workspace presents the playbook as an agent experience, so the steps an agent follows and the steps a customer sees on a portal come from the same playbook.

## Page components

A playbook record page is made up of components such as the stage picker, activity picker, activity viewer, contact or consumer lookup, case summarization, and contextual side panel. Each component has a specific role in helping an agent move through the stages and activities of a case and find the information needed to resolve it. For the full list of components and what each one does, see [Page components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-templates.md).

## Configure pages

A playbook record page can be customized to match how a team works. An administrator can activate a page or page variant, change what appears in the page header, adjust the actions in the action bar, and set what shows in the left and contextual side panels. For the customization tasks available on a playbook page, see [Configure templates and pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-pages.md).

