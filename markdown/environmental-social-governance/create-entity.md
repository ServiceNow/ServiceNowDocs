---
title: Create an entity
description: Create an entity and measure its performance against the goals. Defining an entity ensures that the entity owners are also identified. After an entity is defined, ESG Management goals are applied to the entity.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage entities in ESG Management, Configuring ESG Management, Environmental, Social, and Governance Management]
---

# Create an entity

Create an entity and measure its performance against the goals. Defining an entity ensures that the entity owners are also identified. After an entity is defined, ESG Management goals are applied to the entity.

## Before you begin

Role required: \(per product\)

-   In Environmental, Social, and Governance Management: sn\_esg.program\_manager
-   In GRC: Metrics: sn\_grc\_metric.manager
-   In Risk Management: sn\_risk\_workspace.IT\_risk\_manager and sn\_risk\_workspace.operational\_risk\_manager

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **ESG Workspace** &gt; **Scoping** &gt; **All entities**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_l2g_jzy_vqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Entity

</td></tr><tr><td>

Refers to existing record

</td><td>

Option that refers the new entity to an existing record.

</td></tr><tr><td>

Table

</td><td>

Table to be queried to create an entity.

</td></tr><tr><td>

Applies to record

</td><td>

Records that are associated with the selected table.

</td></tr><tr><td>

Name

</td><td>

Name of the entity.

</td></tr><tr><td>

Owned by

</td><td>

Details of the owner of the entity such as system administrator.

</td></tr><tr><td>

Active

</td><td>

Option that indicates whether the entity is active.

</td></tr><tr><td>

Class

</td><td>

Name of the class that is associated with the entity such as Application or Business Entity.

</td></tr><tr><td>

Location

</td><td>

Location record of the entity with details such as address, city, state, and country.

</td></tr><tr><td>

Description

</td><td>

Description of the entity.

</td></tr><tr><td class="sub-head" colspan="2">

Compliance

</td></tr><tr><td>

Attestation frequency

</td><td>

Frequency of attestations for the controls that are attached to an entity. The choices are as follows:-   **Daily**
-   **Weekly**
-   **Monthly**
-   **Quarterly**
-   **Semi-annually**
-   **Annually**


</td></tr></tbody>
</table>4.  To save the entity, click **Save**.

    **Note:** On the New Entity form, only the **Details** tab is displayed. After a new entity is created, the **Overview** tab, the **Details** tab, and other related lists are displayed on the form.


## Result

The entity is created. The New Entity form is displayed with the **Overview** tab, **Hierarchy** tab, and the related lists:

-   Entity types
-   Downstream risks
-   Downstream controls
-   Downstream engagements
-   Downstream issues
-   Downstream tasks
-   Policy exceptions
-   Content References
-   Goals

**Note:** Some related lists appear in the entity form only when certain applications are installed. For example, the Downstream risks related list appears only when the Risk Management application is installed. The Downstream engagements related list appears only when the Audit Management application is installed. The Downstream controls, Downstream issues, and Policy exceptions related lists appear only if you have the IRM license.

## What to do next

[Update an entity](update-an-entity.md)

**Parent Topic:**[Manage entities in ESG Management](../concept/entities-in-esg.md)

