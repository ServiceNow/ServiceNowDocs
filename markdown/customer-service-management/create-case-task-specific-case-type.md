---
title: Create a case task of a specific type for a customer service case
description: Customer service agents can create different types of case tasks by making selections from the case task type selector screen.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-04"
reading_time_minutes: 2
breadcrumb: [Manage cases, Use, Customer Service Management]
---

# Create a case task of a specific type for a customer service case

Customer service agents can create different types of case tasks by making selections from the case task type selector screen.

## Before you begin

Role required:

-   sn\_customerservice\_agent
-   sn\_customerservice.consumer\_agent
-   sn\_customerservice\_manager
-   sn\_customerservice.svc\_location\_agent
-   sn\_customerservice.case\_task\_agent

## About this task

The types of case tasks that agents can create depends on the configuration of the [customer service case types](../concept/customer-service-case-types.md) and [service definitions](../concept/csm-service-definitions.md) features. For more information, see the following topics:

-   [Configure customer service case types](configure-csm-case-types.md)
-   [Manage customer service case types](../concept/manage-csm-case-types.md)
-   [Configuring service definitions](../concept/csm-service-definitions-configure.md)

In CSM Configurable Workspace, agents use the [Case type selector screen](../concept/csm-case-type-select-modals.md) to make selections and create cases.

## Procedure

1.  Create a case task.

    -   Select **New** from a case task list.
    -   Select **New** from the Tasks related list tab on a case record.
    -   Select the **+** icon on the related records task list in the Dynamic Related Records component.
    -   Select the Task declarative action on the activity viewer.
    -   Select **Create Task** in a case playbook stage.
2.  Make a selection in the case task type selector.

    -   If you create the case task from a case task list, the **Service task** field on the case task type selector shows all of the related services where the target table is Case Task \[sn\_customerservice\_task\] and extensions of Case Task.
    -   If you create the case task from a case record, the **Case task service** field lists the task services related to the case service. If the case has no service, the **Service task** field shows all of the related services where the target table is Case Task \[sn\_customerservice\_task\] and extensions of Case Task.
3.  Select **Create task**

    The case task is created with the selected task service definition. If any default values have been defined in the case task service definition, these values are populated on the case task record.


