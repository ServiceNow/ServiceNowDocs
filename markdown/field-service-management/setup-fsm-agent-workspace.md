---
title: Setting up Field Service in CSM Agent Workspace
description: Activate Field Service in CSM Agent Workspace and set up roles for performing the tasks.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Setting up CSM/FSM Configurable Workspace, Configuring Field Service Management, Field Service Management]
---

# Setting up Field Service in CSM Agent Workspace

Activate Field Service in CSM Agent Workspace and set up roles for performing the tasks.

**Important:** Starting with the Vancouver release, Legacy FSM Agent Workspace is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. The Field Service Management Configurable Workspace \[com.snc.uib.fsm\_agent\_workspace\] provides the latest experience for this functionality. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activating Agent Workspace

Activate the following plugins:

-   Customer Service with Field Service Management plugin \[com.snc.csm\_fsm\_integration\] to enable account, contact, partner, partner contact, consumer information from Customer Service to Field Service Management.
-   Field Service Management plugin \(com.snc.work\_management\) to provide support for scheduling and managing on-location work tasks.
-   FSM Agent Workspace plugin \(com.snc.agent\_workspace.fsm\) is activated when you enable the Field Service Management plugin \(com.snc.work\_management\) or the Customer Service with Field Service Management plugin \[com.snc.csm\_fsm\_integration\].

## Roles used in Agent Workspace for FSM

<table id="table_xkh_hcp_n3b"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains Roles

</th></tr></thead><tbody><tr><td>

Administrator \[admin\]

</td><td>

Update Field Service Management roles for Agent Workspace.

</td><td>

 

</td></tr><tr><td>

Customer Service Agent \[sn\_customerservice\_agent, sn\_customerservice.consumer\_agent\]

</td><td>

-   Create work orders from case.
-   View and apply template on a work order.
-   Move a work order from **Draft** state to **Ready for Approval**, **Ready for Qualification**, and **Ready for Dispatch** based on existing state flow and sm\_config rules.
-   Book an appointment on a work order.

</td><td>

-   knowledge
-   sn\_fsm\_servicedesk\_agent
-   template\_editor
-   chat\_admin
-   sn\_customerservice.deescalation\_requester for only \[sn\_customerservice\_agent\]
-   sn\_templated\_snip.template\_snippet\_reader
-   sn\_shn.editor
-   timecard\_user for \[sn\_customerservice\_agent\]
-   sn\_esm\_agent

</td></tr><tr><td>

Location agent\[sn\_customerservice.svc\_location\_agent\]

</td><td>

Create and manage work orders created from cases for contacts and consumers in their service organization. In integration with Field Service Management:-   View and apply template on a work order.
-   Move a work order from **Draft** state to **Ready for Approval**, **Ready for Qualification**, and **Ready for Dispatch** based on existing state flow and sm\_config rules.
-   Book an appointment on a work order.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_esm\_location\_agent

</td></tr><tr><td>

Location consumer agent\[sn\_customerservice.svc\_location\_consumer\_agent\]

</td><td>

Create and manage work orders created from cases for contacts and consumers in their service organization. In integration with Field Service Management:-   View and apply template on a work order.
-   Move a work order from **Draft** state to **Ready for Approval**, **Ready for Qualification**, and **Ready for Dispatch** based on existing state flow and sm\_config rules.
-   Book an appointment on a work order.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_esm\_location\_agent

</td></tr><tr><td>

Location manager\[sn\_customerservice.svc\_location\_manager\]

</td><td>

Create and manage work orders created from cases for contacts and consumers that belong to the service organizations within their hierarchy. In integration with Field Service Management:-   View and apply template on a work order.
-   Move a work order from **Draft** state to **Ready for Approval**, **Ready for Qualification**, and **Ready for Dispatch** based on existing state flow and sm\_config rules.
-   Book an appointment on a work order.

</td><td>

-   sn\_fsm\_servicedesk\_agent
-   sn\_customerservice.svc\_location\_agent
-   email\_client\_quick\_message\_author
-   sn\_templated\_snip.template\_snippet\_writer
-   sn\_shn.admin
-   approver\_user
-   sn\_publications.approver
-   sn\_customerservice.svc\_location\_consumer\_agent

</td></tr><tr><td>

Relationship agent\[sn\_customerservice.relationship\_agent\]

</td><td>

Restricts an agent's access to cases for the accounts, contacts, consumers, and households that they have a relationship with Relationship Manager and Account Manager.In integration with Field Service Management:

-   View and apply template on a work order.
-   Move a work order from **Draft** state to **Ready for Approval**, **Ready for Qualification**, and **Ready for Dispatch** based on existing state flow and sm\_config rules.
-   Book an appointment on a work order.

</td><td>

-   agent\_workspace\_user
-   sn\_fsm\_servicedesk\_agent
-   snc\_internal
-   sn\_shn.editor
-   email\_composer

</td></tr></tbody>
</table>Notes:

-   When a case is created, the service organization on the case is the service organization of the user who creates the case.
-   When a case is assigned to an agent, the service organization on the case is updated to the service organization of the assigned agent.

