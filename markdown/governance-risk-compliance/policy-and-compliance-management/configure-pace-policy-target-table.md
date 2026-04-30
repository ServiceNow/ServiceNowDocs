---
title: Configure compliance data source registry
description: Set up the Compliance Data Source Registry \(CDSR\) that provides the ability to associate policies in other ServiceNow products with control objectives in Policy and Compliance to inform an organization’s overall compliance stand, and to perform policy exceptions when required.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Preventive compliance with Policy as Code Engine, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Configure compliance data source registry

Set up the Compliance Data Source Registry \(CDSR\) that provides the ability to associate policies in other ServiceNow products with control objectives in Policy and Compliance to inform an organization’s overall compliance stand, and to perform policy exceptions when required.

## Before you begin

Role required: sn\_compliance.admin

## About this task

Based on the association, entities are generated for the associated assessed objects from the target application table and controls are generated automatically. CDSR facilitates easy integrations between GRC and other ServiceNow products such as DevOps, HR, SecOps, and others to meet the customers’ compliance validation and management needs across the enterprise.

Select the application table that is linked to the assessed object table. Establish a relationship between an item in the application table and a control objective in a target table. To do this, the items must first be configured and mapped to the control objective. Secondly, establish a relationship between the target table and the entities in the entity table.

Incidentally, entities are people, processes, departments, applications, or objects that must be measured for compliance against control objectives.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Compliance data source registry**.

2.  Click **New**.

3.  On the form, fill in the fields.

<table id="table_bdh_qhy_qsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the item registry.

</td></tr><tr><td>

Application table

</td><td>

Table of records associated to control objective.

</td></tr><tr><td class="sub-head" colspan="2">

Related entity identification

</td></tr><tr><td>

Assessed object table

</td><td>

Table in which controls are created.

</td></tr><tr><td>

Relationship to application table

</td><td>

Relationship between the item table and the target table. The choices are:-   One to many: One record in the application table is linked to multiple records in the assessed object table, and one record in the assessed object table is linked to only one record in the application table.
-   Many to many: One record in the application table is linked to multiple records in the assessed object table, and one record in the assessed object table is linked to multiple records in the application table.


</td></tr><tr><td>

Application field on assessed object table

</td><td>

Field name that points to the target table.

</td></tr><tr><td>

Application field on m2m table

</td><td>

Field name in the mapping table that points to the item table.

</td></tr><tr><td>

Assessed object field on m2m table

</td><td>

Field name in the mapping table that points to the target table.

</td></tr><tr><td>

Is the assessed object table equivalent to entities?

</td><td>

Flag to create an entity in the target table.

</td></tr><tr><td>

Entity relationship to assessed object table

</td><td>

Relationship between the item table and the entity table. The choices are:-   One to one: When one record in the assessed object table is linked to only one record in the entity table.
-   Many to many: When one record in the entity table is linked to multiple records in the assessed object table, and when one record in the assessed object table is linked to multiple records in the entity table.


</td></tr><tr><td>

Many to many table

</td><td>

Table that establishes the relationship between the item table and the target table.

</td></tr><tr><td>

Entity field on assessed object table

</td><td>

Name of the field that points to the entity table.

</td></tr><tr><td>

Entity field on m2m table

</td><td>

Name of the field in the mapping table that points to an entity table.

</td></tr><tr><td>

Entity owner field

</td><td>

Owner of the entity in the entity table.

</td></tr></tbody>
</table>    For more detailed information on the set up of generic framework compliance data source registry, see the [Set up of generic framework compliance data source registry \[KB1112478\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1112478) article in the Now Support Knowledge Base.

    **Note:** You must log in to Now Support to view the articles.

4.  Click **Submit**.


