---
title: Change the actions that a user can take
description: Configure which actions a user can perform on behalf of a technician they manage.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/change-proxy-action.html
release: brazil
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring proxy actions, Work order tasks, Set up work orders and tasks, Configure, Field Service Management]
---

# Change the actions that a user can take

Configure which actions a user can perform on behalf of a technician they manage.

## Before you begin

Role required: sn\_fsm\_proxy\_actn.proxy\_admin

## About this task

By default, when proxy actions are enabled, managers can take the actions below on behalf of a technician they manage.

You can configure the specific actions that managers can take on behalf of agents. For example, you can limit managers to only closing work order tasks.

Actions that managers can take by default:

-   Accept
-   Reject
-   Start travel
-   Start work
-   Close complete
-   Close incomplete

## Procedure

1.  Select **All** &gt; **Field Service** &gt; **Proxy Configuration** &gt; **Policy**.

2.  Select the policy called **Proxy actions for Managers on behalf of their agents**.

3.  Clear **Enable All Actions**.

4.  Select **Unlock Enabled Actions** \[Omitted image "lock-proxy.png"\] Alt text: lock icon.

5.  Select **lookup using list** \[Omitted image "lookup-list.png"\] Alt text: lookup icon and select the action that others can take on behalf of technicians.

    **Note:** Repeat this step if there is more than one action you want to configure.

6.  Select **Lock enabled actions** \[Omitted image "lock-actions.png"\] Alt text: lock actions.


