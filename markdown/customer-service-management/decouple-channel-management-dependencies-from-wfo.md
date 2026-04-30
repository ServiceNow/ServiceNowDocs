---
title: Decouple Channel Management Dependencies from WFO
description: Decouple Channel Management from core Workforce Optimization \(WFO\) modules to support modular deployment, enabling independent updates or scaling of Channel Management without impacting other workforce engagement.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-28"
reading_time_minutes: 2
breadcrumb: [Agent management, Use, Customer Service Management]
---

# Decouple Channel Management Dependencies from WFO

Decouple Channel Management from core Workforce Optimization \(WFO\) modules to support modular deployment, enabling independent updates or scaling of Channel Management without impacting other workforce engagement.

## Overview of decoupling channel management

Channel Management is a crucial tool that allows users to monitor ongoing work and track agents' performance. Decoupling Channel Management from the core Workforce Optimization \(WFO\) modules supports modular deployment, enabling independent updates or scaling of Channel Management without impacting other workforce engagement.

**Note:** Channel Management when installed as a standalone module along with the agent workspace, the other modules are disabled.

Key Benefits:

-   Independent Deployment: Channel Management can now be deployed independently, allowing for greater flexibility and control.
-   Reduced Inter-Module Dependencies: The decoupling reduces dependencies between modules, enhancing system stability.
-   Enhanced Scalability and Maintainability: The new architecture improves scalability and maintainability, making it easier to manage and expand.
-   Streamlined Future Upgrades: Future upgrades for individual modules can be streamlined, ensuring smoother and more efficient updates.

## Roles and Responsibilities

<table id="table_e33_dp5_chc"><thead><tr><th>

Role Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_channel\_mgmt.admin \(for group manager\)

</td><td>

The System Administrator creates a customer care assignment group and manage channel configurations and assignments.

</td></tr><tr><td>

sn\_channel\_mgmt.user \(for the additional manager\)

</td><td>

The Manager can log into Agent Workspace and access the channel management module through role-based visibility, such as the sn\_channel\_mgmt.user role. The Manager can utilize Channel Management in Agent Workspace independently of the full WFO suite.For more details see [Configuring groups in Workforce Optimization for ITSM](https://www.servicenow.com/docs/access?context=configuring-groups-wfo-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)

</td></tr></tbody>
</table>## Channel Management \(New Menu in Agent Workspace\)

Role: canvas\_user and sn\_channel\_mgmt.user.

Agent Workspace is updated with a new menu icon ChannelManagement. Admin or user can see and access channel icon on the left pane for channel management in the Agent Workspace. On selecting the new channel menu icon, you can view the service channels. Admins can allocate the work items under Queued Work table, to respective group members.

## Channel Management Capabilities for Supervisor Persona

Role: sn\_csm.manager.

Enabling the channel management capabilities for the supervisor persona in Agent Workspace allows access to channel management without the need for the full WFO suite. The Manager can log into Agent Workspace and access the channel management module through role-based visibility, such as the sn\_channel\_mgmt.user role. This ensures that the Manager can use Channel Management in Agent Workspace independently of the full WFO suite.

## Demo Data for Channel Management in Agent Workspace

Role: sn\_channel\_mgmt.admin.

Setting up demo data in Agent Workspace to showcase Channel Management features. The personas involved are an Agent and a Supervisor. The Supervisor creates a customer care assignment group and manage channel configurations and assignments. This group is associated with the customer care chats queue to manage inbound communication effectively. The demo data is provided within Agent Workspace, allowing users to view and interact with it to explore Channel Management functionalities. The validation process includes checking the addition of the new customer care group, populating group members, assigning roles, and ensuring all sections function properly.

For more information on channel management for customer service in workforce optimization, see: [Channel Management in Workforce Optimization for Customer Service](../../workforce-optimization-for-customer-service-configurable/concept/explore-channels-configurable-wfo-cs.md)

