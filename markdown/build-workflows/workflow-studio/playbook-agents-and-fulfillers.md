---
title: Running Playbook Experience
description: Interact with a business workflow in real-time from within Workspace. Agents can use Playbook Experience to update records, upload attachments, and complete tasks across multiple workflow activities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/playbook-agents-and-fulfillers.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Playbooks, Workflow Studio, Build workflows]
---

# Running Playbook Experience

Interact with a business workflow in real-time from within Workspace. Agents can use Playbook Experience to update records, upload attachments, and complete tasks across multiple workflow activities.

## Playbook Experience overview

Playbooks are built by admins in Workflow Studio, customized by admins in UI Builder and more, and embedded in Workspace, Configurable Workspace, Service Portal and more. Playbook Experience provides visibility for fulfillers into cross-business workflows and the actionable tasks used to complete these business workflows.

-   Playbooks may appear in the side panel or in the related items of records configured with playbook.
-   Activities that you must perform to complete the business workflow are displayed. Some activities may be performed by an AI Agent instead. You're able to see what you of an AI Agent has done and what still must be done to complete the playbook. You can collapse activities to display relevant activities, and expand them again.
-   Activities are typically performed sequentially. You can go back to those activities to complete them later. \[Omitted image "playbook-flow.gif"\] Alt text: Screenshot showing Playbook flow example.

## Playbook UI

Playbooks contain helpful UI features.

-   **Header**

    Shows the title of a Playbook. A header exists for each playbook attached to a record. Selecting a Playbook header expands the stages nested under it.

    \[Omitted image "playbook-header.png"\] Alt text: Screenshot showing Playbook header example.

-   **Stages**

    Select a stage title to view its activities. By default, all activity cards are collapsed except for the first card in a stage.

    The stage progress updates as activities are completed. A check mark inside the playbook header indicates that the stage is complete.

    \[Omitted image "playbook-stage-progress.png"\] Alt text: Screenshot showing stage status complete and in progress.

    Use the stage filter \[Omitted image "playbook-hr-filter-icon.png"\] Alt text: Playbook filter icon to filter a playbook.

    \[Omitted image "playbook-stage-filter.png"\] Alt text: Screenshot showing stage filter selections.

    Use the ellipses action menu icon \[Omitted image "playbook-ellipses.png"\] Alt text: Playbook action menu icon to perform select actions at the playbook and stage level.

    \[Omitted image "playbook-ellipses-menu.png"\] Alt text: Screenshot showing Playbook action menu at playbook level.

-   **Activity cards**

    Playbook activity cards display details about an activity, which may include the status, SLA timer, form data, and attachments. Use playbook activity cards to complete tasks by filling in forms, completing checklists, and adding attachments.

    \[Omitted image "playbook-activity-cards.png"\] Alt text: Screenshot showing Playbook activity cards.


-   **[Add an activity to a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-add-optional-activity.md)**  
Add preselected optional activities to a Playbook Experience if available.
-   **[Testing support for playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/testing-support-playbooks.md)**  
The Automated Test Framework \(ATF\) can be used to create automated tests to confirm your playbooks run as planned.
-   **[Restart a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/restart-a-playbook.md)**  
Restart a playbook from the beginning, an activity, or a stage.
-   **[Cancel a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/cancel-playbook.md)**  
Cancel a playbook to stop a business workflow when no longer valid.
-   **[Open full lists within playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/full-list-playbook.md)**  
Open a full list within playbook cards to view and update list items.
-   **[Using activity stream within a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/activity-stream-in-playbook.md)**  
Use activity stream within a playbook to add comments or notes, and view communication and task history for the parent or associated record.

**Parent Topic:**[Workflow Studio Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/workflow-studio-playbooks-landing.md)

