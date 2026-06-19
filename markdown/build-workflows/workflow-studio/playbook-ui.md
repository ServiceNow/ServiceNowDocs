---
title: About Playbook Experience
description: Interact with a business workflow in real time from within Workspace. Agents can use Playbook Experience to update records, upload attachments, and complete tasks across multiple workflow activities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/playbook-ui.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Running Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# About Playbook Experience

Interact with a business workflow in real time from within Workspace. Agents can use Playbook Experience to update records, upload attachments, and complete tasks across multiple workflow activities.

## Playbook Experience overview

Playbook are built by admins in Workflow Studio, customized by admins in UI Builder and more, and embedded in Workspace, Configurable Workspace, Service Portal and more. The Playbook Experience for fulfillers during runtime provides visibility into cross-business workflows and the actionable tasks used to complete these business workflows.

-   Playbook may appear in the side panel or in the related items of records configured with playbook.
-   Activities that you must perform to complete the business workflow are displayed. You're able to see what you've done and what you must do to complete the playbook. You can collapse activities to display relevant activities, and expand them again.
-   Activities are typically performed sequentially. You can go back to those activities to complete them later. Complete an activity and go to the next activity, or complete the playbook.

Playbook Experience automatically updates playbook tasks if completed outside of a playbook.

\[Omitted image "playbook-flow.gif"\] Alt text: Playbook flow.

## Playbook UI

Playbook contain helpful UI features.

-   **Header**

    Shows the title of a playbook. A header exists for each playbook attached to a record. Selecting a playbook header expands the stages nested under it. \[Omitted image "playbook-header.png"\] Alt text: Playbook header

-   **Stages**

    Click a stage title to view its activities. By default, all activity cards are collapsed except for the first card in a stage.

    \[Omitted image "playbook-stage-title.png"\] Alt text: Stage title

    The stage progress updates as activities are completed. A checkmark inside the playbook header indicates that the stage is complete.

    \[Omitted image "playbook-stage-progress.png"\] Alt text: Stage status complete and in progress

    Use the stage filter \(\[Omitted image "playbook-hr-filter-icon.png"\] Alt text: Playbook filter icon\) to filter a playbook.

    \[Omitted image "playbook-stage-filter.png"\] Alt text: stage filter selections

    Use the ellipses action menu icon \(\[Omitted image "playbook-ellipses.png"\] Alt text: Playbook action menu icon\) to perform select actions at the playbook and stage level.

    \[Omitted image "playbook-ellipses-menu.png"\] Alt text: Playbook action menu at playbook level

-   **Activity cards**

    Playbook activity cards display details about an activity, which may include the status, SLA timer, form data, and attachments. Use playbook activity cards to complete tasks by filling in forms, completing checklists, and adding attachments.\[Omitted image "playbook-activity-cards.png"\] Alt text: Playbook activity cards


**Parent Topic:**[Running Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-agents-and-fulfillers.md)

