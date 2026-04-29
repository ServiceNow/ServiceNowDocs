---
title: Components installed with Guided Decisions Experience
description: Several types of components are installed with the Guided Decisions Experience application, including tables, roles, and guidances.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Install the Guided Decisions Experience application, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Components installed with Guided Decisions Experience

Several types of components are installed with the Guided Decisions Experience application, including tables, roles, and guidances.

## Tables

The following tables are added to your instance with the activation of Guided Decisions Experience.

<table id="table_efw_1rd_ywb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Decision Tree\[ga\_decision\_tree\]

</td><td>

Stores details of all decision trees.

</td></tr><tr><td>

Decision Tree Node\[ga\_decision\_tree\_node\]

</td><td>

Stores details of all decision tree nodes in each decision tree.

</td></tr><tr><td>

Decision Input Mapping\[ga\_decision\_input\_mapping\]

</td><td>

Stores input-mapping details such as source node, source input, destination node, and destination input.

</td></tr><tr><td>

Decision Tree Version\[ga\_decision\_tree\_version\]

</td><td>

Stores decision tree versions with states.

</td></tr></tbody>
</table>## Roles

The following roles are added to your instance with the activation of the Guided Decisions, Guided Decisions Experience, and Recommended Actions plugins.

<table id="table_zn2_xrd_ywb"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Decision tree author\[decision\_tree\_author\]

\[sn\_gd\_core.decision\_tree\_author\]

</td><td>

Creates, views, updates, and deletes decision trees.**Note:** This role is automatically given to customer service managers.

</td><td>

-   decision\_table\_admin
-   sn\_gd\_guidance.guidance\_manager
-   decision\_tree\_user

 **Note:** Included with the Guided Decisions plugin.

</td></tr><tr><td>

Decision tree user\[decision\_tree\_user\]

</td><td>

Views decision trees.**Note:** This role is automatically given to customer service agents.

</td><td>

-   decision\_table\_reader
-   sn\_gd\_guidance.guidance\_user

 **Note:** Included with the Guided Decisions plugin.

</td></tr><tr><td>

Guidance manager\[sn\_gd\_guidance.guidance\_manager\]

</td><td>

Creates, views, updates, and deletes guidances, which are outcome of a decision tree.**Note:** This role is automatically given to customer service managers.

</td><td>

-   sn\_gd\_guidance.guidance\_user

**Note:** Included with the Guided Decisions - Guidance plugin.

-   metadata\_scope\_viewer: Grants read-only access to the Application field on metadata records within scoped applications.

**Note:** Included in the Global application scope.


</td></tr><tr><td>

Guidance user\[sn\_gd\_guidance.guidance\_user\]

</td><td>

Views guidances. **Note:** This role is automatically given to customer service agents.

</td><td>

uxframework\_user**Note:** Included with the Guided Decisions - Guidance plugin.

</td></tr><tr><td>

Playbook author\[pd\_content\_author\]

</td><td>

Adds decision trees and guidances to a new or existing playbook for service agents to access on their workspace.

</td><td>

-   sn\_gd\_core.decision\_tree\_user
-   pd\_shared.user
-   pd\_trigger\_author

</td></tr><tr><td>

Resource Generator author\[sn\_nb\_action.resource\_generator\_author\]

</td><td>

Configures resource generators.

</td><td>

-   flow\_operator
-   decision\_table\_reader
-   platform\_ml\_read
-   sn\_nb\_action.trend\_definition\_author

 **Note:** Included with the Recommended Actions plugin.

</td></tr><tr><td>

Trend Definition author\[sn\_nb\_action.trend\_definition\_author\]

</td><td>

Configures trend definitions.

</td><td>

**Note:** Included with the Recommended Actions plugin.

</td></tr></tbody>
</table>Granular admin users can be granted delegated developer privileges and other required roles to manage and configure metadata in scoped applications instead of assigning high-privileged admin roles. By granting granular admin users with the Manage Update Set permission, you can allow them to create and manage records within a specific application scope and track those changes in the appropriate update set. The metadata\_scope\_viewer role allows these granular admins to view the Application field on metadata records within scoped applications.. For more information on the delegated development, see [Delegated Development](https://www.servicenow.com/docs/access?context=delegated-development-landing&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Guidances

The Guided Decisions Experience application includes the guidances described in the following table.

<table id="table_e4p_rjl_d5b"><thead><tr><th>

Guidance

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Apply resolution from a solved case

</td><td>

Enables agents apply a resolution from recommended solved cases by clicking the **Resolve case** button on a card. The action copies the resolution notes and a resolution code from the solved case into the Closure Information section of the current case. The state of the current case changes to resolved.

</td></tr><tr><td>

Communicate Workaround

</td><td>

Enables agents to communicate a workaround from a recommended problem record by clicking a **Communicate workaround** button on a card. The action opens the guidance in the side panel.

 The guidance shows the workaround from the problem record and provides a note field for the agent to add additional notes. The workaround and notes are added in the work notes and the problem record is linked to the current case.

</td></tr><tr><td>

Create case task

</td><td>

Enables agents to create a case task for the current case by clicking a **Create** button on a card, which opens the guidance in the side panel where the agent can enter a subject for a new case task and submit it.

</td></tr><tr><td>

Create Work Order

</td><td>

Enables agents to create a work order for a case by clicking a **Create** button on a card. Creates a work order task and opens the task in a subtab.

</td></tr><tr><td>

Link to existing defect

</td><td>

Enables agents to link an existing defect to the current case by clicking a **Link to defect** button on a card, which links the defect to the case and updates the work notes.

</td></tr><tr><td>

Link to existing open case

</td><td>

Enables agents to link the current case to an existing open case by clicking the **Link to this case** button on a card. The action sets the open case as the parent of the current case.

</td></tr><tr><td>

Offer Recommendation

</td><td>

Enables agents to recommend upgrade of a product to provided product model.

</td></tr><tr><td>

Propose Resolution

</td><td>

Enables agents to enter resolution notes and a resolution code for a case by clicking a **Propose Solution** button on a card.

</td></tr><tr><td>

Read message to customer

</td><td>

Enables an agent to indicate that a message was read to the customer during a call by clicking the **Mark as read** button on a card, and adding the message to the work notes.

</td></tr><tr><td>

Reassign case

</td><td>

Enables agents to reassign the current case to a recommended assignment group by clicking a **Reassign** button on a card, which opens the guidance in a side panel where the agent can enter notes. The current case is reassigned to a different assignment group and the work notes are updated.

</td></tr><tr><td>

Review and attach article

</td><td>

Enables agents to review a recommended knowledge article in the contextual side panel. They can do this by clicking the **Review and attach article** button on a card, which opens the article in the side panel.

 In the side panel, agents can do the following:

-   Review the article.
-   Attach the article to the case.
-   Mark the article as helpful.
-   Open the article in a subtab.

</td></tr></tbody>
</table>