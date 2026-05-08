---
title: CMDB CI Lifecycle Management \(legacy\)
description: From the time of its creation until it's no longer needed, a CMDB CI would typically transition through several operational states. CI LIfecycle Management provides the mechanism to define states and actions for a CI and lets you apply appropriate actions based on a CI's state to tailor the management of CI lifecycle to business needs.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB CI Lifecycle Management \(legacy\)

From the time of its creation until it's no longer needed, a CMDB CI would typically transition through several operational states. CI LIfecycle Management provides the mechanism to define states and actions for a CI and lets you apply appropriate actions based on a CI's state to tailor the management of CI lifecycle to business needs.

The CMDB Data Manager is now a more comprehensive and integrated solution for managing CI life cycle operations such as deletion and archival, in bulk. For information about the CMDB Data Manager, see [Working with CMDB Data Manager](cmdb-data-management.md).

Terms associated with CI Lifecycle Management:

-   **Operational states**

    A set of states that a CI can be at such as 'Operational' or 'Repair in Progress'. A CI can be associated with only a single operational state at any given time. The choices for operational states are based on the **operational\_status** field in the \[cmdb\_ci\] table. There are several operational states that are defined in the base system such as 'Retired' and 'Repair in Progress'. You can modify this list to reflect operational states that are relevant in your business.

    **Note:** By default, Service Mapping is configured to ignore all host CIs for which the value of Operational status **\[operational\_status\]** is not **1** \(Operational\) or the value of status **\[install\_status\]** is **100** \(absent\). For additional information about this behavior, see [Preparing customized ServiceNow deployments to work with Service Mapping](https://support.servicenow.com/kb_view.do?sysparm_article=KB0647574) \[KB0647574\] in the HI Knowledge Base.

    CI Lifecycle Management allows multiple operators and automations to simultaneously set different operational states of a CI. Since a CI cannot be associated with multiple operational states, it is important to configure each operational state with a priority. These priorities are then used in such situation to determine which of the operational states is the cumulative operational state.

-   **CI actions**

    A set of actions that can be applied to a CI during its lifetime. You can define CI actions that are relevant in your business.

-   **Compatible CI Actions**

    CI Lifecycle Management allows a CI to have multiple active CI actions simultaneously, however they must be specifically defined as compatible. By default, there are no two actions for a CI that are compatible with each other. You can change this behavior by specifying pairs of actions that are compatible and thus allowed to be applied simultaneously to a CI. For example, you can specify that the ‘Patching’ and the ‘Provisioning’ CI actions are compatible making it possible to apply both simultaneously to a CI.

-   **Not Allowed CI Actions**

    By default, any CI action can be applied to any CI. You can restrict this behavior by defining a rule that an action is not allowed for a CI when it is in a specific operational state. For example, you can define a Not Allowed CI Action in which it is not allowed to apply the 'Provisioning' action to a Linux Server that is in a 'Non-Operational' state.

-   **Not Allowed Operational Transitions**

    By default, transitions are allowed from any operational state to another. You can restrict this behavior by defining a rule that for a specified CI, a transition from a certain operational state to another operational state is not allowed. For example, you can define that for a Linux Server it is not allowed to transition from 'Repair in progress' to 'Non-Operational'.

-   **Requestor**

    A requestor can be a workflow or a non-workflow operator that is trying to set operational states and apply CI actions. Each requestor has an associated requestor ID that is a GUID and that can be an active workflow context or a non-workflow registered operator ID.

-   **Lease time**

    A time period that each requestor \(especially non-workflow operators\) can provide, during which a specified CI action is allowed to be active for a specified CI.


CMDB CI Lifecycle Management provides a set of APIs to manage CI operational states and CI actions. And the UI where you define a set of rules to restrict certain operational state transitions and to restrict actions based on operational states. It also provides a mechanism to audit CI operational state and CI actions during the entire CI lifecycle.

Providers such as automation, workflows, or Change Management can use CI Lifecycle Management as a mechanism to manage CI operational states and apply CI actions. By default, the behavior of CI Lifecycle Management has no restrictions on some operations, and full restrictions on other operations. The CI Lifecycle Management UI lets you modify this default behavior by specifying Not Allowed CI Actions, Compatible CI Actions, and Not Allowed Operational Transitions that restricts some operations and enables for others.

With CI Lifecycle Management you can:

-   Manage CI operational states and CI actions throughout the entire CI lifecycle.
-   Manage CI operational state transitions.
-   Restrict certain operational state transitions.
-   Associate certain actions for certain CI types that are in specific operational state.
-   Restrict IT Service Management applications based on CI operational state.
-   Audit CI operational states and CI actions during the entire CI lifecycle.

## Lifecycle management APIs

CI Lifecycle Management provides a set of APIs to manage CI operational state and CI actions during the entire CI lifecycle. All restrictions and allowances specified by rules in the UI are enforced when state management APIs run, and if an API attempts to perform a restricted operation, the operation is blocked and an error is logged.

## Registering requestors

When using the lifecycle management APIs to apply CI actions, requestors are required to be registered and to obtain a requestor ID which is unique within the lifecycle management tables. To register and to obtain a requestor ID, non-workflow users should call the **registerOperator** API. Workflow users can use the active Workflow context as the requestor ID, and they do not need to explicitly call registerOperator.

After completing the CI lifecycle operations, the requestor should call the unregisterOperator API to unregister. All the state management records associated with that specific requestor ID are then marked as inactive or they are removed by the **CI Lifecycle Management — Restore Internal State Management Tables** scheduled job.

## Integration with Incident Management and Problem Management

A base instance includes the pre-defined CI action **CreateTask** used for creating a task for a CI. New instances have a pre-defined Not Allowed CI Action, specifying that the 'CreateTask' action is not allowed for any CI with a **Retired** operational state. This restriction is integrated with Incident Management and with Problem Management to prevent the creation of incident or problem tasks for retired CIs. The 'CreateTask' CI action is used as a reference qualifier to the **Configuration Item** field of the Incident/Problem tables. In a new incident or problem, CIs in which **Operational Status** is 'Retired' — are filtered out from the **Configuration Item** list on the form. For more information about reference qualifiers, see Reference qualifiers .

## Integration with Asset Management

In a base system, a CI's **Operational Status** field and the **Status**/**Hardware Status** \(if its hardware\) fields are kept synchronized if one of the two fields' values is **Retired**. When **Operational Status** of a CI is set to **Retired**, then the **Status**/**Hardware Status** field is automatically set to **Retired**. In the opposite direction, when the **Status**/**Hardware Status** field of a CI is set to **Retired**, **Operational Status** is automatically set to **Retired** too.

-   When an **Operational Status** field changes from **Retired** to another status, the CI’s **Status**/**Hardware Status** field is set to **Installed**.
-   When a CI’s **Status**/**Hardware Status** field changes from **Retired** to another status, the **Operational Status** field is automatically set to **Non-Operational**.

    The change of state from 'Retired' to another state is seldom, and by default, the state is changed to 'Non-Operational'. However, this might not be the intended state for the record. Therefore, it important that administrators review and manage the state appropriately in this case.


Whenever CI’s **Status**/**Hardware Status** changes, it is synchronized to the CI’s corresponding **Asset State** field, and vice versa — keeping the CI’s **Operational Status** and the CI’s corresponding **Asset State** synchronized.

For more information about mapping **Asset State** and **Substate** fields to a CI's **Status**/**Hardware Status** \(if its hardware\) field, see Map asset state and CI hardware status. And for more information about retiring assets, see Retire assets.

-   **[Get started with CI Lifecycle Management](../task/get-started-cilifecyclemgmt.md)**  
Follow these high level steps to get started and to track activities of the CI Lifecycle Management module of the CMDB application.
-   **[Lifecycle management APIs](state_mgmt-api.md)**  
CI Lifecycle Management provides a set of state management APIs for manipulating CI operational states, and applying CI actions.
-   **[Components installed by CI Lifecycle Management](../reference/tbls-instld-ci-lifecycle-mgmt.md)**  
Several types of components are installed by CI Lifecycle Management \(included in the com.snc.cmdb plugin\), including tables, scheduled jobs, and properties.
-   **[Activate the CI Lifecycle Management scheduled job](../task/enable-cilifecyclemgmt-job.md)**  
When starting to use the CI Lifecycle Management module, ensure to activate the **CI Lifecycle Management - Restore Internal State Management Tables** scheduled job which is disabled by default. This scheduled job continuously checks and maintains the data integrity of all internal CI Lifecycle Management tables.
-   **[Define a CI action](../task/define-cmdb-ci-action.md)**  
Define a CI Lifecycle Management CI action that can be later applied to CIs.
-   **[Define compatible CI actions](../task/dfn-cmptbl-cmdb-ci-action.md)**  
Allow a CMDB CI Lifecycle Management operation in which two specified CI actions can be applied simultaneously to a CI.
-   **[Define a not-allowed CI action](../task/non-allowed-cmdb-ci-action.md)**  
Define a restriction for CI Lifecycle Management in which a specified action is not allowed for a CI that is in a specified operational state.
-   **[Set priority for an operational state](../task/set-priority-operational-state.md)**  
CI Lifecycle Management allows multiple operators or automations to simultaneously set different operational states for a CI. A CI can have only a single operational state, so in this case, the cumulative operational state of the CI is set to the one with the highest priority. It is recommended that you specify a priority for each operational state that you define so that a cumulative state can be correctly calculated.
-   **[Define a non-allowed operational transition](../task/not-allowed-oprtionl-trnston.md)**  
Define a restriction for CI Lifecycle Management in which a specified CI cannot transition from one operational state to another.

**Parent Topic:**[Configuration Management Database \(CMDB\)](c_ITILConfigurationManagement.md)

