---
title: Playbooks on Configurable Workspace
description: Configurable Workspace is the main environment where users work through a playbook. When a user opens a record that has a playbook attached, the playbook loads automatically; displaying the stages, the activities within each stage, and the current activity to complete.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-07-07"
reading_time_minutes: 2
keywords: [Playbooks on Configurable Workspace]
---

# Playbooks on Configurable Workspace

Configurable Workspace is the main environment where users work through a playbook. When a user opens a record that has a playbook attached, the playbook loads automatically; displaying the stages, the activities within each stage, and the current activity to complete.

Configurable Workspace itself is customizable — administrators control the layout, which components appear, what shows in the header, and how the contextual side panel is configured. The playbook within that workspace is also customizable through the record page configuration in UI Builder. Together, these customizations allow each organization to tailor the full experience to match how their users work.

## Who uses it

**For agents, fulfillers, and technicians:** These are the end users who work through playbooks at runtime in Configurable Workspace. They see the stages and activities that administrators configured, and they complete the work step-by-step. They can access information from the contextual side panel without leaving the workspace.

-   A customer service agent uses a complaint case playbook to investigate and resolve a customer issue, working through triage, investigation, and resolution stages.
-   A field service technician uses a work order playbook to complete equipment maintenance tasks and access related equipment records and service history.

**Administrators and implementation partners:** These roles design and customize Configurable Workspace to meet organizational needs. They work in UI Builder to select page templates, configure which components appear on the page, choose the stage layout \(horizontal or vertical\), and manage the contextual side panel display. They also set rules in the playbook experience configuration for stage and activity visibility based on user roles or record state.

-   An administrator selects the Focused page template for a complaint case playbook, then configures visibility rules so supervisors see additional escalation activities that agents cannot access.
-   An implementation partner customizes the contextual side panel for a work order playbook to display related equipment records and service history.

## How to use it

A typical workflow looks like this:

-   A user opens a record, such as a case, work order, or request. The playbook loads based on the record type.
-   The stage picker shows where the record is in the process. The user selects a stage to see its activities.
-   The user works through each activity, filling in a form, reviewing information, or completing a checklist, and marks it complete before moving on.
-   The contextual side panel is available throughout, giving access to the activity stream, related records, attachments, and other tools without leaving the page.
-   When all activities in a stage are done, the playbook advances to the next stage.

