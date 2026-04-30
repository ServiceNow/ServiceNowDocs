---
title: An entity in the workspace view
description: The Entity form in the workspace provides a complete view of an entity across your organization. The Entity form is listed under the Library menu of the List view in the workspace. Select an entity in the list view so that you can display its overview, details, hierarchy, entity types, or downstream risks.
locale: en-US
release: xanadu
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Explore entities, Common GRC features, Governance, Risk, and Compliance]
---

# An entity in the workspace view

The Entity form in the workspace provides a complete view of an entity across your organization. The Entity form is listed under the Library menu of the List view in the workspace. Select an entity in the list view so that you can display its overview, details, hierarchy, entity types, or downstream risks.

## Overview details on the Entity form

The Entity form displays the details on the entity such as Compliance status, Risk status, and Tracking. The information about an entity is organized in different tabs such as Overview, Details, and Hierarchy as shown in the following example.

![Entities overview page](../image/entities-overview-final.png "Overview tab on the Entity form")

The related lists on the Entity form display the dependencies that are related to the entities as explained in the following table:

<table id="table_j15_drs_45b"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details tab

</td><td>

Information about the entity such as Name, Active condition that shows whether the entity is active, Owned by, Class, Description, and Location information in the Entity section. The Compliance section displays the Attestation frequency such as Annually.The Cybersecurity Risk Profile \(CRI\) displays the following fields:

-   **Tier**

Tier levels such as Tier 1, Tier 2, Tier 3, and Tier 4.

Controls are generated based on the change of the tier. If you change the tier value, then save the record.

-   **Tiering assessment**

Assessment method based on the new smart control assessment engine, which has the tiering assessment templates as the CRI templates.

-   **Tiering assessor**

User who can perform the tiering assessment.


</td></tr><tr><td>

Hierarchy tab

</td><td>

Information about the upstream entities and downstream entities, entity class, owner information.

</td></tr><tr><td>

Highlighted details

</td><td>

Downstream hierarchy for the selected entity, related entity types, regulatory bodies applicable to the entity, and related policies.

</td></tr></tbody>
</table>The Entities section displays the following related lists:

<table id="table_gs4_j3v_lqb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity types

</td><td>

Details of the entity type, description, condition if the entity type was created manually and the Compliance score in percentage.

</td></tr><tr><td>

Risks

</td><td>

The Risks tab on the entity record page displays the following:-   **Directly related risks**: List all risks that are directly associated with the entity.
-   **Suggested risks**: List all risks suggested by the Risk Suggestion AI Agent.
-   **All risks**: List all directly related risks and downstream risks.

</td></tr><tr><td>

Downstream controls

</td><td>

Details of the downstream controls such as Name, Number, Entity, Control objective, State, Status, Exempt, Owner, and Description.

</td></tr><tr><td>

Downstream inherited controls

</td><td>

Details of downstream inherited controls such as Control, Number, Entity, Reliant entity, Function, State, Status, Exempt, Owner, Description, and Control objective.

</td></tr><tr><td>

Downstream engagements

</td><td>

Details of the downstream engagements such as Name, Number, Type, Parent plan, State, Engagement lead, Remaining expense budget \(%\), Remaining resource budget \(%\), and engagement planned start.

</td></tr><tr><td>

Downstream issues

</td><td>

Details of the downstream issues such as Issue, Number, Entity, Priority, Assigned to, and Issue manager. You can add existing Issues, create new issue, or remove an existing issue.

</td></tr><tr><td>

Downstream tasks

</td><td>

Details of the downstream tasks such as Name, Number, Parent, State, Assigned to, and Planned end date.

</td></tr><tr><td>

Policy exceptions

</td><td>

Details of the policy exceptions such as Name, Number, State, Substate, Policy, Control objective, Issue, Reason, Requester, Valid from, Valid to, and Risk rating.

</td></tr><tr><td>

Risk events

</td><td>

Details of the risk events such as Risk event, Primary entity, Event type, Sub type, State, Date of discovery, Net loss, Expected loss, and Non-financial impact.

</td></tr><tr><td>

Content references

</td><td>

Details of the content reference such as Content reference, Description, and version. You can click **Add** to add the content references.

</td></tr><tr><td>

Risk assessments

</td><td>

Details of the risk assessments such as Number, Risk assessment methodology, Assessable entity, Risk, Applies to record, Inherent risk, Control effectiveness, Residual risk, Response, Assessor, and End date.

</td></tr><tr><td>

Aggregated risks

</td><td>

Details of the aggregated risks such as Risk assessment methodology, Residual rating, Inherent rating, Control effectiveness, Residual ALE, Inherent ALE, Contributing risk assessments, and Risk rollup status.

</td></tr><tr><td>

Privacy assessments

</td><td>

Details of the Privacy assessments such as Number, Metric type, Classification, Due date, State, and Assigned to.

</td></tr><tr><td>

CRI Tiering assessments

</td><td>

Details of tiering assessment of an entity such as the Assessment template, State, Users, and Due date.

</td></tr><tr><td>

CRI assessments

</td><td>

Details of control assessment such as the Assessment template, State, Users, and Due date.

</td></tr><tr><td>

Stakeholders

</td><td>

Stakeholders with customizable roles relevant to single and composite entities, enabling effective team involvement in risk assessments and projects. You can add persona, group, and users in the stakeholder list.

</td></tr></tbody>
</table>The 360° view displays an entire relationship view for the selected entity the upstream entities, downstream entities, entity class and entity type associated with the entity, and the relationships that the entity includes.

![360 degree view of the entity](../image/360-degree-view-of-the-entity.png "360 degree view of the entity")

-   **[Create an entity](../task/create-new-entity-ws.md)**  
Create an entity for your enterprise. In Governance, Risk, and Compliance, entities can be people, processes, departments, applications, or objects. These entities have controls that are defined to mitigate their exposure, and their audits must be completed.

**Parent Topic:**[Exploring the entities](../../grc-common/concept/exploring-the-entities.md)

