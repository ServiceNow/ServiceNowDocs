---
title: Components installed with PSEW
description: Components installed with PSEW.
locale: en-US
release: yokohama
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: reference
last_updated: "2025-03-24"
reading_time_minutes: 3
breadcrumb: [Proactive Service Experience Workflows reference, Proactive Service Experience Workflows]
---

# Components installed with PSEW

Components installed with PSEW.

The main components are as follows:

-   Flows and subflows
-   Escalation stages
-   Decision tables
-   Messages
-   Business rule
-   Client scripts
-   System properties
-   Roles
-   Assignment groups
-   Service Operations Workspace

## Flows and subflows

A workflow is triggered when an incident is created with the SD-WAN category and one of these five subcategories:

-   Link Failure
-   Device Failure
-   Protocol Failure
-   Soft-WAN Link Failure
-   Software Failure

Each category has subflows for each assignment group and a level of escalation for a total of 27 subflows. These subflows are a starting point created primarily for network operations outages, but can be reused and extended for other use cases.

## Escalation stages

The five stages of escalation are as follows:

-   Triage
-   L1 investigation
-   L2 investigation
-   L3 investigation
-   Resolution

Proactive Service Experience Workflows uses these stage values to trigger the appropriate decision in the Incident Escalation Policy \[sys\_hub\_flow\] decision table. This table triggers the correct subflow during incident escalation. During each stage of escalation, an incident task is created and maintained for that assignment group. The incident information synchronizes to the incident task from a business rule and includes the following:

-   Short description
-   Priority
-   State
-   Work notes that the assigned person in the assignment group adds to the incident
-   Message content that is embedded in the incident by the workflow

## Decision tables

Based on the defined condition, Workflow Studio works with the Incident Escalation Policy \[sys\_hub\_flow\] decision table to determine which subflow to generate at certain escalation points.

## Messages

Each subflow in Proactive Service Experience Workflows is associated with a message file that provides instructions for agents to use to troubleshoot, escalate, and resolve network-initiated incidents. For more information about how to customize the default instructions for your internal troubleshooting processes, see [Customize message files](../task/configure-msg-file-taw.md).

## Business rules

The `Sync to tsm incident task` business rule determines the information that synchronizes from the incident to the incident task, including:

-   Short description
-   Priority
-   State
-   Assignment group
-   Assignee
-   Work notes that the assigned person in the assignment group adds to the incident

## Roles

The `sn_ind_tsm_core.noc_agent` role is available with the Proactive Service Experience Workflows application. This role when added, ensures that the technical support agent can see the relevant information between ITSM and CSM applications. This role includes the following:

-   itil
-   wm\_initiator
-   wm\_read
-   sn\_customerservice.case\_viewer
-   sn\_customerservice.customer\_data\_viewer

Several assignment groups are included with this role and other groups can also have the admin role. The `sn_ind_tsm_sdwan.ticket_integrator` role can be used for trouble tickets created from the TMF 621 Open API use cases.

## Assignment groups

Workflows involve network-related personnel, including network coordinators and engineers. All assignment groups have the base `sn_ind_tsm_sdwan.PSEW_USER` system role.

**Note:** These assignment groups are a starting point, created primarily for network operation support.

-   **Network coordinator**

    The network coordinator's tasks and responsibilities are as follows:

    -   Manage and triage incidents from the network management systems
    -   Assess the impact and define the incident priority
    -   Refresh the impacted services and create cases for the affected customers
    -   Correlate incidents with the open incidents or change requests using Agent assist
    -   Assign incidents and coordinate with network engineering
-   **L1- Network engineer**

    The L1 - network engineer's tasks and responsibilities are as follows:

    -   Troubleshoot network incidents
    -   Engage Field Service agents, third-party vendors, and OEMs to resume normal service operation
    -   Trigger the Change Management and Problem Management processes
-   **L2 - Network engineer**

    The L2 - network engineer's tasks and responsibilities are as follows:

    -   Troubleshoot network incidents
    -   Engage Field Service agents, third-party vendors, and OEMs to restore normal service operation
    -   Trigger the Change Management and Problem Management processes to introduce beneficial change or perform root cause analysis
-   **L3 - Network engineer**

    The L3 - engineer's tasks and responsibilities are as follows:

    -   Troubleshoot network incidents
    -   Engage Field Service agents, third-party vendors, and OEMs to restore normal service operation
    -   Trigger the Change Management and Problem Management processes to introduce beneficial changes or perform root cause analysis

**Parent Topic:**[Proactive Service Experience Workflows reference](assurance-workflows-reference.md)

