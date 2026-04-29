---
title: Components installed with CSM workspaces
description: Several types of components are installed with CSM workspaces.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Customer Service Management]
---

# Components installed with CSM workspaces

Several types of components are installed with CSM workspaces.

## Roles

The agent workspace user role \(agent\_workspace\_user\) is added to the Service Management agent \(sn\_esm\_agent\) role. The role is required to access Agent Workspace for CSM.

## Form views

Customer service agents see forms in the CSM Workspace form view \(workspace\_csm\), if they exist for certain record types. Otherwise, agents see forms in the Workspace form view.

## Tables

In CSM workspaces, a number of Customer Service Management tables are provided with the Workspace and CSM Workspace view layouts.

-   **Tables in Workspace view**

    The Workspace view is provided for the following tables:

    -   Case \(sn\_customerservice\_case\)
    -   Consumer \(csm\_consumer\)
    -   Account \(customer\_account\)
    -   Contact \(customer\_contact\)
    -   Account Relationship \(account\_relationship\)
    -   Asset \(alm\_asset\)
    -   Contract \(ast\_contract\)
    -   Product Model \(cmdb\_model\)
    -   Entitlement \(service\_entitlement\)
    -   Task \(sn\_customerservice\_task\)
    -   Appointments \(sn\_customerservice\_appointment\)
    -   Contact Relationship \(sn\_customerservice\_contact\_relationship\)
    -   Escalation \(sn\_customerservice\_escalation\)
    -   Order \(csm\_order\)
    -   Order Case \(csm\_order\_case\)
    -   Special Handling Notes \(sn\_shn\_notes\)
    -   Order Line Item \(csm\_order\_line\_item\)
    -   Asset Contact \(sn\_customerservice\_m2m\_asset\_contact\)
    -   Account Team Member \(sn\_customerservice\_team\_member\)
    -   Social Profiles table \(sn\_app\_cs\_social\_social\_profile\)
    -   Social Logs table \(sn\_app\_cs\_social\_social\_log\)
    -   Knowledge Applied to Tasks table \(m2m\_kb\_task\)
-   **Tables in CSM Workspace view**

    The CSM Workspace view \(workspace\_csm\) is provided for the following tables:

    -   Interaction \(interaction\)
    -   Location \(cmn\_location\)
    The CSM Workspace view for these tables is similar to the respective default platform interface view.


## Lists

The list categories and filtered lists that have been configured for customer service agents in CSM workspaces.

<table id="table_kbv_c1t_rdb"><thead><tr><th>

List Category

</th><th>

Filtered Lists

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cases

</td><td>

My Cases

</td><td>

Cases assigned to the customer service agent.

</td></tr><tr><td>

 

</td><td>

My Open

</td><td>

Open cases assigned to the customer service agent.

</td></tr><tr><td>

 

</td><td>

Unassigned for my groups

</td><td>

Cases that belong to any of the customer service agent's groups but have not been assigned to an agent.

</td></tr><tr><td>

 

</td><td>

All

</td><td>

All customer service cases.

</td></tr><tr><td>

Major Issue Management

</td><td>

Major Cases

</td><td>

Major cases that have been accepted.

</td></tr><tr><td>

Customer

</td><td>

Accounts

</td><td>

A list of customer accounts.

</td></tr><tr><td>

 

</td><td>

Partners

</td><td>

A list of partner accounts.

</td></tr><tr><td>

 

</td><td>

Contacts

</td><td>

A list of customer contacts.

</td></tr><tr><td>

 

</td><td>

Consumers

</td><td>

A list of consumers.

</td></tr><tr><td>

Interactions

</td><td>

My Interactions

</td><td>

Interactions that are assigned to the customer service agent \(agent's name appears in the **Assigned to** field on the interaction record\).

</td></tr><tr><td>

Knowledge

</td><td>

My Knowledge Articles

</td><td>

Knowledge articles authored by the customer service agent \(agent's name appears in the **Author** field\).**Note:** This list appears in the list panel when the Knowledge Management Advanced Installer plugin \(com.snc.knowledge\_advanced.installer\) is activated.

</td></tr><tr><td>

Catalog Tasks

</td><td>

Assigned to my groups

</td><td>

Catalog tasks assigned to the current agent's groups.

</td></tr></tbody>
</table>**Note:** Additional filtered lists appear in the list panel when a customer service agent also has the itil role.

