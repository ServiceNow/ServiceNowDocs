---
title: Configure Service Model Foundation
description: Configure the Service Model Foundation feature to enable a foundational data model framework. You can use this framework to create structured and flexible data models that represent your business needs.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data models, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure Service Model Foundation

Configure the Service Model Foundation feature to enable a foundational data model framework. You can use this framework to create structured and flexible data models that represent your business needs.

## Before you begin

Role required: admin

## About this task

Service Model Foundation provides the core framework and guidance for building and modeling the entities that are involved in the customer service value chain. This framework introduces new entities, such as service organizations, internal and external business locations, and households. It also introduces roles and relationships that provide both flexibility and control in granting access to customer cases and information.

With the Service Model Foundation plugins, you can support:

-   Internal business locations and staff members
-   External business locations and staff members
-   Households and household members

For more information about this feature, see [Service Model Foundation overview](../concept/csm-industry-data-model.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup**.

2.  On the Getting Started page of the guided setup, click **Get Started**.

3.  In the Service Model Foundation category, view the list of tasks to configure the feature.

<table id="table_pz1_qqv_llb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate plugins

</td><td>

Activate the plugins:-   Business Location \(com.snc.business\_location\)
-   Customer Service Household \(com.snc.household\)


</td></tr><tr><td>

Activate query rules

</td><td>

Activate the query rules by setting the system property \[sn\_cs\_queryrules.use\_query\_rules\] value to **true**.

</td></tr><tr><td>

Configure forms and lists

</td><td>

Configure forms to add the fields and related lists that support the business location and household models.

</td></tr><tr><td>

Assign responsibilities

</td><td>

Assign responsibilities to the service organization \(SO\) member using the responsibility data model.

</td></tr><tr><td>

Assign roles

</td><td>

Roles control access to features, capabilities, and data. The Service Model Foundation plugins add roles that you can assign to internal and external users in your organization.

</td></tr><tr><td>

Create relationships

</td><td>

Use relationships to provide internal and external users with additional access to customer data. Relationships are based on responsibility definitions. When you create a relationship, you select the users involved in the relationship and the responsibility that one user performs on behalf of another.

 The Service Model Foundation plugins provide both relationships and responsibility definitions that you can use to create relationships between users.

</td></tr></tbody>
</table>4.  To perform a task, click **Configure**.

    This button opens the page in your instance where the configuration is completed.


