---
title: Granular Delegation
description: Granular delegation allows employees to delegate their tasks to other employees for specific date and time ranges based on delegation rules.
locale: en-US
release: xanadu
product: Granular Delegation
classification: granular-delegation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Employee Service Management]
---

# Granular Delegation

Granular delegation allows employees to delegate their tasks to other employees for specific date and time ranges based on delegation rules.

Granular delegation provides the ability to delegate specific records by table and condition. It also allows admins to delegate approvals and/or task assignments for task tables they administer.

A task is delegated when it matches the delegation rules specified for a delegation. For example, William can assign Jane as a delegate for approvals or tasks when the priority is set to High.

Service delegation options are available, like limiting a delegation to specific record types. For example:

-   Limiting records that match a filter condition.
-   Limiting records to only approvals.
-   Limiting records to only task assignments.

**Note:** Granular Delegation is intended for employee users, not fulfiller or agent users, such as in ITSM. Depending on your use cases, fulfiller and agent delegation is better managed via [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-application-landing-page&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Terms

The following terms are applicable:

-   Delegate Admin: An employee that defines the tables used for delegation rules, defines delegation rules, and can assign delegates for employees.
-   Delegator: An employee who delegates their tasks to another employee through a delegation record, specifying the delegate user, time frame, and delegation rules.
-   Delegate: An employee who is delegated tasks that are assigned to another employee. The delegate also receives tasks assigned from the delegator. The delegate also receives notifications of these assignments and the time frame the delegation covers.

## Granular Delegation with HR Service Delivery

Granular Delegation with the HR Service Delivery base system supports the HR task \(sn\_hr\_core\_task\) table. Along with filter conditions, you can filter delegations for delegators and delegates.

For more information on how user criteria filters delegations for delegators and delegates, see [Create delegation rules](../task/create-delegation-rules.md).

For information on HR criteria and user criteria, see:

-   [HR criteria](../../../human-resources/concept/hr-criteria.md#)
-   [User criteria for Service Portal](https://www.servicenow.com/docs/access?context=user-criteria&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

-   **Access control rules \(ACLs\)**

    Access control rules \(ACLs\) in HR Service Delivery were modified to look for the Assigned to person on an HR task. Other domains that want to use Granular Delegation must modify their ACLs to use this feature. For more information about ACLs, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

-   **Rule-based and ad-hoc delegations**

    -   Rule-based: The delegation\_admin configures delegation rules, which automatically reassign tasks to specific employees.
    -   Ad-hoc: An employee who is defined as a delegator can delegate their tasks from the **My Delegates** widget in the Employee Center.
    **Note:** The delegation\_admin must define a delegation rule table, delegation rules, and delegates. For more information on defining a delegation rule table see [Add delegation rule tables](../task/add-delegation-rules-tables.md). For more information on defining a delegation rule, see [Create delegation rules](../task/create-delegation-rules.md). For more information on defining delegators and delegates, see [Create a delegate](../task/create-delegation-admin.md).


