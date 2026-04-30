---
title: Blocking tasks
description: Certain agent actions trigger case flows which create and resolve blocking tasks for customer service cases. These tasks determine the case action status.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Case action status overview, Administer Customer Service Management, Customer Service Management]
---

# Blocking tasks

Certain agent actions trigger case flows which create and resolve blocking tasks for customer service cases. These tasks determine the case action status.

When an agent performs certain actions, such as asking a customer for more information or associating a problem with a case, the system:

-   Adds a blocking task to the case. This task appears on the Case form in the **Blocked by** form section.
-   Updates the **Action Status** field on the Case form and Case list.

**Note:** A blocking task is something that prevents an agent from making progress toward case resolution. For example, a case might have one or more open related task records or be waiting for customer feedback.

Additionally, there are actions that resolve these blocking tasks, such as the customer responding to an agent’s question or an internal user resolving a problem task. When one of these actions occur, the system:

-   Updates the status of the blocking task on the Case form.
-   Updates the **Action Status** field on the Case form and Case list.
-   Enables the **Needs Attention** field on the Case form.

## Actions that create blocking tasks

The following actions create blocking task for customer service cases:

-   The agent sets the state of the case to **Needs More Information**.
-   The agent associates one of the following to the case:
    -   Problem
    -   Request
    -   Change
    -   Incident
    -   Case task
    -   Work order

## Actions that resolve blocking tasks

The following actions resolve blocking tasks for customer service cases:

-   A customer provides the requested information.
-   A fix or a workaround is associated with a related problem record.
-   A related problem, request, change, or incident record is resolved.
-   A related case task or work order is closed or canceled.

## Needs attention field

When the **Needs attention** field on the Case form is enabled, the **Action Status** column on the Case list displays a blue indicator.

The **Needs attention** field is enabled automatically when:

-   A blocking task for a case is resolved.
-   A customer or someone other than the case owner comments on a case.
-   A work note is added to a case that is a child of a major case.

Customer service agents and managers can manually enable the **Needs attention** field if information is required from customers or internal users. This field can be deactivated only by the agent assigned to the case or by the customer service manager or admin.

## Requesting additional information from a customer

When an agent requests additional information from a customer, the system enables the **Needs attention** field and sets the **Action status** field to Needs attention.

If an agent must request additional information from a customer for a second time on the same case, be sure to clear the **Needs attention** field on the Case form before requesting the information. This ensures that the status updates correctly.

## Case action status and major issue management

When using the case action status feature with major issue management, the following actions enable the **Needs attention** field for a major case:

-   A customer provides comments for a case that is a child of a major case.
-   An agent adds a work note to a case that is a child of a major case.

## Blocked by related list

Blocking tasks that are created for a case are added to the **Blocked by** related list. Each blocking task is assigned one of the following blocking reasons:

-   Need information from the customer
-   Need task resolution
-   Need PRB workaround
-   Other

**Note:** When a problem is associated with a case and a blocking task is created, the blocking reason is set to **Need task resolution**. If necessary, the agent can change this reason to **Need PRB workaround**.

When a blocking task is resolved:

-   The **Unblocked By** field displays the user who performed the unblocking action.
-   The **Unblocked On** field displays the date that the blocking task was resolved.

## Blocking Tasks table

Records that have blocking tasks are stored in the Blocked By table \[sn\_action\_status\_blocked\_by\]. Records are periodically removed from this table. Six months after a blocked record is closed, the entries in the Blocked By table related to the blocked record are removed.

**Parent Topic:**[Case action status overview](../concept/customer-service-case-action-status.md)

