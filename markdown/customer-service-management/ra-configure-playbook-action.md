---
title: Configure a playbook as a Recommended Actions
description: Add a playbook as a recommended action type in the authoring interface, then select and configure the playbook with its required inputs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ra-configure-playbook-action.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [playbooks, recommended actions, authoring, configure]
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Configure a playbook as a Recommended Actions

Add a playbook as a recommended action type in the authoring interface, then select and configure the playbook with its required inputs.

## Before you begin

One or more playbooks must already be published and active in your instance.

Role required: RA author

## About this task

Playbooks deliver step-by-step guidance directly within the Recommended Actions panel. As an author, you can select any published playbook and add it as a recommended action type. You can then configure the playbook's required inputs so that it has the correct context when an agent launches it.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**

2.  Open a context from the list and then open a rule in the context.

3.  Select or create a recommended action rule.

    You can add a playbook to a new or existing rule configuration.

4.  In the Action type drop-down, select **Playbook**.

    The system displays a new section for playbook configuration.

5.  Select a playbook from the available list.

    Only active and published playbooks appear in this list.

    **Note:** If you don't see a playbook you expect, verify it is published and active in the Playbook application.

6.  Configure the playbook's required inputs.

    Each playbook may have required input fields. Fill in or map values for these inputs so the playbook has the correct context when launched.

7.  Configure the playbook launch mode \(optional\).

    Choose how the playbook should launch when an agent clicks the action:

    -   **Launch and Show** — Opens the playbook in a side panel or new tab
    -   **Launch Only** — Emits an event without rendering the playbook UI
    Default is **Launch and Show**.

8.  Save the recommended action configuration.

    The system validates and saves your playbook action configuration. The playbook is now available as a recommended action to users who match the rule criteria.


## Result

The playbook is successfully added as a recommended action type and configured with its required inputs. Agents now see the playbook as an action card in the Recommended Actions panel when the rule matches their context.

## What to do next

Monitor how agents interact with the recommended playbook action. You can review execution history to see which playbooks are most frequently used and which might need adjustment.

