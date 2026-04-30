---
title: Configure access through the responsibility access configuration
description: Streamline how you create and update your responsibility definitions and access configurations by using the declarative responsibility framework in the Customer Service Management \(CSM\) application. This framework enables you to select the level of access for each responsibility by leveraging low-code or no-code capabilities, which reduces the time required for scripting.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring customer access management, User management, Set up your environment, Configure, Customer Service Management]
---

# Configure access through the responsibility access configuration

Streamline how you create and update your responsibility definitions and access configurations by using the declarative responsibility framework in the Customer Service Management \(CSM\) application. This framework enables you to select the level of access for each responsibility by leveraging low-code or no-code capabilities, which reduces the time required for scripting.

## Before you begin

Role required: admin

## About this task

The Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table is used to store the metadata of the responsibility access configuration. With this configuration, you can enable different levels of access for related party users across different records of the same entity. For example, a user with a location manager role might serve as a fulfiller at one business location and as an agent at another.

For more information about creating a responsibility definition, see [Create a responsibility definition](t_CreateAResponsibilityDefinition.md). The need for domain separation in configuring access records is determined by the domain of the referenced responsibility.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Responsibility Definitions**.

2.  Select a responsibility definition record.

3.  From the Responsibility Access Configuration related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_xqp_24b_1yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Responsibility

</td><td>

Responsibility applicable to this configuration, for example, account manager or authorized representative.

</td></tr><tr><td>

Active

</td><td>

Status of the configuration. By using this functionality, you can enable or disable a responsibility access configuration.The default value is **True**.

</td></tr><tr><td>

Roles required

</td><td>

Roles required in addition to responsibilities to get the access.

</td></tr><tr><td>

Access levels

</td><td>

Levels of access for the accessible entities. The list shows the access levels, including read, write, and full. **Note:** Full represents a special access level that is equivalent to read, write, and create.

</td></tr><tr><td>

Accessible table

</td><td>

Entities or records accessible through this configuration, like cases or sold products.

</td></tr><tr><td>

Accessible table filter

</td><td>

Additional conditions to filter the accessible table.

</td></tr><tr><td>

Relationship table

</td><td>

Relationship table where this configuration is applied, for example account team member \[sn\_customerservice\_team\_member\] table.

</td></tr><tr><td>

Relationship filter

</td><td>

Additional conditions to filter the relationship records applicable to the user.

</td></tr><tr><td>

Type

</td><td>

Type of association between the accessible and relationship table. Listed are three types of association:

-   Simple
-   Dependent
-   Advanced


</td></tr><tr><td>

Relationship field

</td><td>

Field on the relationship table to be used for association.

</td></tr><tr><td>

Accessible table field

</td><td>

Field on the accessible table to be used for association.

</td></tr><tr><td>

Dependent table

</td><td>

Table that contains the mapping between the relationship field and accessible table field.

</td></tr><tr><td>

Dependent relationship field

</td><td>

Field on the dependent table that maps to the selected relationship field.

</td></tr><tr><td>

Dependent accessible table field

</td><td>

Field on the dependent table that maps to the selected accessible table field.

</td></tr><tr><td>

Field values script

</td><td>

Script that returns the valid association values for advanced association logic.

</td></tr></tbody>
</table>    **Note:** To create new entries to the **Applies to Relationship**, **Access Levels**, or **Accessible Entities** fields in the Responsibility Access Configuration table, you must migrate all existing configurations for these fields in the global.CSMRelationshipConstantsSNC script include.

5.  Select **Submit**.


