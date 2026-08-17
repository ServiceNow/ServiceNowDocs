---
title: Configure a playbook recommendation in Recommended Actions
description: Add a playbook as a recommended action type, then select and configure the playbook with its required inputs in the Recommendation form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/ra-configure-playbooks.html
release: australia
topic_type: task
last_updated: "2026-07-06"
reading_time_minutes: 1
keywords: [Configure playbook in Recommended Actions]
breadcrumb: [Configuring the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Configure a playbook recommendation in Recommended Actions

Add a playbook as a recommended action type, then select and configure the playbook with its required inputs in the Recommendation form.

## Before you begin

-   One or more playbooks must already be published and active in your instance.
-   Role required: sn\_nb\_action.next\_best\_action\_author or admin

## About this task

Playbooks deliver step-by-step guidance directly within the Recommended Actions panel. As an author, you can select any published playbook and add it as a recommended action type. You can then configure the playbook's required inputs so that it has the correct context when an agent launches it.

## Procedure

1.  Navigate to **All** &gt; **RecommendedActions** &gt; **Contexts**.

2.  Open a context from the list and then open a rule in the context.

3.  Select or create a recommendation within a rule.

    You can add a playbook to a new or existing rule configuration.

4.  In the Action type drop-down, select `Playbook`.

    The system displays a new section for playbook configuration.

5.  Select a playbook from the available list.

    Only active and published playbooks appear in this list.

    **Note:** If you don't see a playbook you expect, verify it is published and active in the Playbook application.

6.  Configure the playbook's required inputs.

    Each playbook may have required input fields. Fill in or map values for these inputs so the playbook has the correct context when launched.

7.  In the Launch mode field, select how to launch a playbook in the Agent workspace when an agent selects the action.

    -   **Launch in expanded view**: The playbook opens in the configured location such as a related tab.
    -   **Launch in side panel**: The playbook opens in the Suggested Actions tab of the Recommended Actions Contextual Side Panel.
    **Note:** This field appears when you select the `Playbooks` option in the Action type field.

8.  Save the recommended action configuration.

    The system validates and saves your playbook action configuration. The playbook is now available as a recommended action to users who match the rule criteria.


## Result

The playbook is successfully added as a recommendation and configured with its required inputs. Agents now see the playbook as an action card in the Recommended Actions panel when the rule matches their record context.

