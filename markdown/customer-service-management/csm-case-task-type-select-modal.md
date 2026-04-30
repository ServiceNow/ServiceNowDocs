---
title: Case task type selector
description: The case task type selector is a component that provides customer service agents with a way to create the right types of tasks while working on cases.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Customer service case types, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Case task type selector

The case task type selector is a component that provides customer service agents with a way to create the right types of tasks while working on cases.

Using the case task type selector, agents can select services and create case tasks specifically for those services. The selections that an agent can make within the case task type selector depends on where they create a case task from.

<table id="table_phq_hrq_yxb"><tbody><tr><td>

When an agent creates a case task from a case task list, they can select a service in the case task type selector.

</td><td>

![Case task type selector with a Service task field that you can use to select a case task service](../image/case-task-type-selector-list.png "Case task type selector (case task list view)")

</td></tr><tr><td>

When an agent creates a case task from a case record, the case task type selector shows related services based on the case type.

</td><td>

![Case task type selector with fields that display the service from the case and a dropdown list of selectable case task services](../image/case-task-type-selector-record.png "Case task type selector (case record view)")

</td></tr></tbody>
</table>An agent working on a case or a case type can create case tasks in the following ways.

<table id="table_csb_f5b_yxb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Select **New** from a case task list

</td><td>

The **Service task** field on the case task type selector shows all of the related services where the target table is Case Task \[sn\_customerservice\_task\] and extensions of Case Task.

</td></tr><tr><td>

Select **New** from the Tasks related list tab on a case record

</td><td>

The **Service** field is auto-filled with the case service. The **Case task service** field lists the task services related to the case service.

 If the case has no service, the **Service task** field shows all of the related services where the target table is Case Task \[sn\_customerservice\_task\] and extensions of Case Task.

</td></tr><tr><td>

Select the **+** icon on the related records task list in the Dynamic Related Records component

</td><td>

The **Case task service** field on the case task type selector shows the following services:-   The task services related to the case service.
-   The related services where the service target table is Case Task and extensions of Case Task.

</td></tr><tr><td>

Select **Create Task** in a case playbook stage

</td><td>

The **Service** field is auto-filled with the case service. The **Case task service** field lists the task services related to the case service.

</td></tr><tr><td>

Select **Create Task** in the activity viewer

</td><td>

The **Service** field is auto-filled with the case service. The **Case task service** field lists the task services related to the case service.

</td></tr></tbody>
</table>Some declarative actions available with the Customer Service Case Types plugin are disabled by default. For more information, see [Configure case type and case task type declarative actions](../task/config-case-type-declarative-action.md).

## Configuring service definitions for cases and case tasks

The system administrator creates the [service definitions](csm-service-definitions.md) for cases and case tasks, along with their relationships. The service definition manager and service definition admin can also create these service definitions and relationships.

For case task service definitions, the system administrator can include logic and default field values that the system uses when creating the case tasks. For more information, see [Configuring service definitions](csm-service-definitions-configure.md).

