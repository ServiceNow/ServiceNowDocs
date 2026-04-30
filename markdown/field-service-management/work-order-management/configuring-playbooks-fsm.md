---
title: Configuring Playbooks for Field Service Management
description: Playbooks provide step-by-step guidance for your field service teams to complete tasks. Use the playbooks feature to create processes to manage the life cycle of field service tasks.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work orders and tasks, Configure, Field Service Management]
---

# Configuring Playbooks for Field Service Management

Playbooks provide step-by-step guidance for your field service teams to complete tasks. Use the playbooks feature to create processes to manage the life cycle of field service tasks.

A playbook breaks a workflow into multiple stages. Each stage includes the following:

-   A list of activities or steps that the agent must perform.
-   Status indicators that display the current state of each activity or step.
-   Check boxes and counters that indicate where an agent is in the workflow.

Playbooks are created using the [Process Automation Designer](https://www.servicenow.com/docs/access?context=process-automation-designer&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US) platform feature.

## Playbooks for the ServiceNow Agent

Playbooks for the ServiceNow Agent application include stages for completing a work order task. Playbooks can be viewed under a selected work order task on the **My work** page. Tasks that have an active playbook associated with it display a **View Playbooks** button.

Playbooks are organized in stages to provide a guided experience. They direct you to new or existing features of the mobile application and maintain a checklist of completed stages on that work order task. Stages can be marked complete or skipped at your discretion. The stages progress as follows:

1.  Troubleshoot
2.  Parts
3.  Record time
4.  Log incidentals
5.  Verify work completion
6.  Close work order task

For more information, see [Playbooks on ServiceNow Agent](playbooks-now-mobile-agent-app.md).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Configuration Overview

The steps for setting up Playbooks for Field Service Management are:

1.  [Install Playbooks for Field Service Management](../task/activate-fsm-playbook.md)

    Install the Playbooks for Field Service Management application \(sn\_fsm\_playbook\) if you have the admin role.

2.  [Activate Playbooks for Field Service Management](../../../administer/process-automation-designer/task/activate-process-automation-designer-for-fsm.md)

    Activate Workflow Studio Playbooks on your instance so that you can create Playbooks triggered by tables.


