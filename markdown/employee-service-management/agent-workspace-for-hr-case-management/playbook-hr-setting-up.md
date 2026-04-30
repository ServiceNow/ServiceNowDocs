---
title: Setting up HR Service Delivery Playbook
description: Set up HR Service Delivery Playbook so that your agents can easily manage, track, and lifecycle event cases.
locale: en-US
release: zurich
product: Agent Workspace for HR Case Management
classification: agent-workspace-for-hr-case-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Playbook, Agent Workspace, HR Service Delivery, Employee Service Management]
---

# Setting up HR Service Delivery Playbook

Set up HR Service Delivery Playbook so that your agents can easily manage, track, and lifecycle event cases.

-   **Activation**

    To activate Playbook for HR, you must go to the ServiceNow Store to make it available on your instance.

    Activate the following plugins:

    Playbook Experience Core \[com.glide.playbook\_experience.config\].

    The next two \(2\) applications are obtained from the store:

    -   Playbook Experience \[sn\_playbook\_exp\]
    -   Playbook Experience Components \[now\_playbook\_exp\]
    For more information, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   **HR cards**

    The Playbook tab under HR Service Delivery Agent Workspace has HR cards.

    HR cards represent each activity in the activity set which could represent various records such as HR tasks, HR cases, requests, incidents, approvals, and more.

    Below is an example of an HR card showing an HR task record.

    -   The Verify Work Authorization card has an HR task type = Mark When Complete condition.
    -   Each activity shows an HR task, case, request, and others. The activities look at the HR Playbook Card Configuration table to match the lowest order record.
    -   The HR Playbook Card Configuration can have filters to determine what values to render.
    -   Use HR Playbook Card Configuration to configure cards.
    -   For more information, see [Configure HR Service Delivery playbook card](../task/playbook-hr-card-configuration.md).

As an HR administrator, use this to configure how each playbook looks in HR Service Delivery Playbook for different types of records \(HR case, task, and others\). Different record types have different relevant information to show.

The base system provides 19 records.

**Note:** For more information on playbook configuration, see Set up a playbook.

