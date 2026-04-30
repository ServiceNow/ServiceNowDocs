---
title: Components installed with Recommended Actions
description: Several types of components are installed with the Recommended Actions application, including tables, roles, guidances, resource generators, and scheduled jobs.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Install the Recommended Actions application, Recommended Actions configuration, Implement Intelligence, Configure, Customer Service Management]
---

# Components installed with Recommended Actions

Several types of components are installed with the Recommended Actions application, including tables, roles, guidances, resource generators, and scheduled jobs.

## Tables

The Recommended Actions application adds the metadata tables described in the following table.

<table id="table_brq_nnw_15b"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Context\[sn\_nb\_action\_rule\_context\]

</td><td>

Stores contexts for tables such as case, incident, and problem for which recommendations are generated.

</td></tr><tr><td>

Recommendation\[sn\_nb\_action\_recommended\_action\]

</td><td>

Stores recommendations, which include action type, action, and resource generator information.

</td></tr><tr><td>

Action Type Definition\[sn\_nb\_action\_type\_definition\]

</td><td>

Stores action type definitions such as guidances, guided decision trees, and field recommendations.

</td></tr><tr><td>

Field Recommendation\[sn\_nb\_action\_field\_recommendation\]

</td><td>

Stores field recommendations.

</td></tr><tr><td>

Field Recommendation Definition\[sn\_nb\_action\_field\_recommendation\_definition\]

</td><td>

Stores field recommendation definitions.

</td></tr><tr><td>

Field Recommendation Input\[sn\_nb\_action\_field\_recommendation\_input\]

</td><td>

Stores inputs for field recommendations.

</td></tr><tr><td>

Resource Generator\[sn\_nb\_action\_resource\_generator\]

</td><td>

Stores resource generators.

</td></tr><tr><td>

Resource Generator Type\[sn\_nb\_action\_resource\_generator\_type\]

</td><td>

Stores resource generator types such as flow, decision table, scripting, similarity, similarity with trend, and classification.

</td></tr><tr><td>

Resource Generator Type Input\[sn\_nb\_action\_generator\_type\_input\]

</td><td>

Stores inputs for resource generators types.

</td></tr><tr><td>

Trend Definition\[sn\_nb\_action\_trend\_definition\]

</td><td>

Stores trend definitions.

</td></tr><tr><td>

Rule\[sn\_nb\_action\_condition\_based\_rule\]

</td><td>

Stores rules, which include a condition and roles for the context.

</td></tr><tr><td>

Recommended Action Rule\[sn\_nb\_action\_rule\_base\]

</td><td>

Stores recommended action rules records.

</td></tr><tr><td>

Conditional Rule\[sn\_nb\_action\_conditional\_rule\]

</td><td>

Stores conditional rules. This table is no longer supported.

</td></tr><tr><td>

Decision Table Rule\[sn\_nb\_action\_decision\_table\_rule\]

</td><td>

Stores decision table rules. This table is no longer supported.

</td></tr><tr><td>

Recommended Action Input Generator\[sn\_nb\_action\_input\_generator\]

</td><td>

Stores input generator records. This table is no longer supported.

</td></tr><tr><td>

Search result recommended action mapping \[sn\_nb\_action\_search\_result\_ra\_mapping\]

</td><td>

Stores mapping between search result outputs and action inputs.

</td></tr></tbody>
</table>## Roles

The Recommended Actions application includes the roles described in the following table.

<table id="table_vgb_b2v_15b"><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Recommended Actions admin\[sn\_nb\_action.next\_best\_action\_admin\]

</td><td>

Grants administrator access to the Recommended Actions application.

</td><td>

sn\_nb\_action.next\_best\_action\_author

</td></tr><tr><td>

Recommended Actions author\[sn\_nb\_action.next\_best\_action\_author\]

</td><td>

Can create recommended actions.

</td><td>

-   sn\_nb\_action.resource\_generator\_author
-   sn\_gd\_guidance.guidance\_manager
-   sn\_nb\_action.next\_best\_action\_user
-   sn\_gd\_core.decision\_tree\_author

</td></tr><tr><td>

Recommended Actions user\[sn\_nb\_action.next\_best\_action\_user\]

</td><td>

Can use recommended actions.

</td><td>

sn\_gd\_core.decision\_tree\_author

</td></tr><tr><td>

Resource Generator author\[sn\_nb\_action.resource\_generator\_author\]

</td><td>

Grants access to configure resource generators.

</td><td>

-   flow\_operator
-   decision\_table\_reader
-   platform\_ml\_read
-   sn\_nb\_action.trend\_definition\_author
-   sn\_ti\_admin.tia\_user

</td></tr><tr><td>

Trend Definition author\[sn\_nb\_action.trend\_definition\_author\]

</td><td>

Grants access to configure trend definitions.

</td><td>

None

</td></tr></tbody>
</table>Other than the roles in the preceding table, you can delegate deployment tasks to developers or non-admin users. For more information on the delegated development, see [Delegated Development](https://www.servicenow.com/docs/access?context=delegated-development-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

## Guidances

The Recommended Actions application includes the guidances described in the following table.

<table id="table_e4p_rjl_d5b"><thead><tr><th>

Guidance

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Apply resolution from a solved case

</td><td>

Enables agents to apply a resolution from a recommended solved case by clicking **Resolve case** button on a card, which copies the resolution notes and a resolution code from the solved case into the Closure Information section of the current case. The state of the current case changes to resolved.

</td></tr><tr><td>

Communicate Workaround

</td><td>

Enables agents to communicate a workaround from a recommended problem record by clicking a **Communicate workaround** button on a card, which opens the guidance in the side panel.

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

Enables agents to link the current case to an existing open case by clicking a **Link to this case** button on a card, which sets the open case as the parent of the current case.

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

Enables an agent to indicate that a message was read to a customer during a call by clicking the **Mark as read** button on a card, and adding the message to the work notes.

</td></tr><tr><td>

Reassign case

</td><td>

Enables agents to reassign the current case to a recommended assignment group by clicking the **Reassign** button on a card, which opens the guidance in a side panel where the agent can enter notes. The current case is reassigned to a different assignment group and the work notes are updated.

</td></tr><tr><td>

Review and attach article

</td><td>

Enables agents to review a recommended knowledge article in the contextual side panel by clicking a **Review and attach article** button on a card, which opens the article in the side panel.

 In the side panel, agents can do the following:

-   Review the article.
-   Attach the article to the case.
-   Mark the article as helpful.
-   Open the article in a subtab.

</td></tr></tbody>
</table>## Resource generators

The Recommended Actions application includes the resource generators described in the following table.

|Resource generator|Description|
|------------------|-----------|
|Find most read KB Article for Product|Finds the most read KB article for the selected product. You can use this KB article to attach to a case as a recommended action.|
|Find Matching PRB with workaround|Finds a matching problem record that has a workaround. You can propose to share the workaround from this case as a recommended action.|
|Find Matching PRB without workaround|Finds a matching problem record without a workaround. You can propose to link to this problem record as a recommended action.|

