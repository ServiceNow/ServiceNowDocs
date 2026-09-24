---
title: Configure proxy actions
description: Proxy actions let authorized users perform work order task actions on behalf of a technician who can't act themselves. Configuration controls who can act, on whose behalf, and which actions are allowed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/configure-proxy-fsm.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Configure proxy actions

Proxy actions let authorized users perform work order task actions on behalf of a technician who can't act themselves. Configuration controls who can act, on whose behalf, and which actions are allowed.

## How proxy actions works

Proxy actions builds on two plugins. Granular Delegation is a platform plugin that provides the underlying policy mechanism, and you might already have it installed for other purposes. Proxy Actions for Field Service Management adds work order task actions, roles, and a dedicated policy screen on top of Granular Delegation.

Installing Proxy Actions for Field Service Management doesn't affect any existing Granular Delegation policies you might have configured for other features.

## Default policy

Proxy Actions for Field Service Management ships with one policy already configured. This default policy covers work order tasks assigned to a manager's managed agents, and is assigned to the wm\_manager role. It enables six proxy actions: accept, reject, start travel, start work, close complete, and close incomplete.

No additional policy configuration is required, but each manager still needs the proxy\_agent role assigned to perform a proxy action.

## Roles

Two kinds of roles apply to proxy actions.

A policy's **Assigned to** role determines which users the policy covers, such as wm\_manager. An administrator can assign a policy to any role, like wm\_dispatcher, or to an individual user.

Two dedicated security roles also control access to the feature:

-   **sn\_fsm\_proxy\_actn.proxy\_admin**

    Required to create or edit a proxy policy.

-   **sn\_fsm\_proxy\_actn.proxy\_agent**

    Required to perform a proxy action. Every user who performs a proxy action needs this role, even a manager covered by the default policy.


## Configure proxy actions

Configuring proxy actions involves the following steps.

1.  Activate the Granular Delegation plugin.

    [Activate Granular Delegation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/activate-granular-delegation.md)

2.  Activate the Field Service Management proxy actions plugin. Activating Field Service Management proxy actions auto-installs the Granular Delegation plugin if it's not already installed.

    [Activate Proxy Actions for Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/fsm-proxy-action.md)

3.  Add the sn\_fsm\_proxy\_actn.proxy\_agent or sn\_fsm\_proxy\_actn.proxy\_admin roles to users.

    [Assign a role to a user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AssignARoleToAUser.md)

4.  \(Optional\) Add more resources that can take proxy actions.

    [Add resources to take proxy actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/add-resources-proxy.md)

5.  \(Optional\) Change the actions a user can take.

    [Change the actions that a user can take](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/change-proxy-action.md)


**Related topics**  


[Proxy actions in Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/proxy-actions-fsm.md)

[Complete a proxy action in Dispatcher Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-scheduling/proxy-action-dispatcher.md)

[Complete proxy actions on Field Service Manager Mobile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/proxy-action-manager.md)

[Complete a proxy action in Workforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/field-service-manager-workforce/proxy-action-workforce.md)

