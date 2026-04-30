---
title: Configure access through the responsibility access configuration
description: Streamline how you create and update your responsibility definitions and access configurations by using the declarative responsibility framework in the Customer Service Management \(CSM\) application. This framework enables you to select the level of access for each responsibility by leveraging low-code or no-code capabilities, which reduces the time required for scripting.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure customer access management, User management, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure access through the responsibility access configuration

Streamline how you create and update your responsibility definitions and access configurations by using the declarative responsibility framework in the Customer Service Management \(CSM\) application. This framework enables you to select the level of access for each responsibility by leveraging low-code or no-code capabilities, which reduces the time required for scripting.

## Before you begin

Role required: admin

## About this task

The Responsibility Access Configuration \[sn\_customerservice\_responsibility\_access\_config\] table is used to store the metadata of the responsibility access configuration. This configuration specifies the level of access and the entities that can be accessed by a particular responsibility. For more information about creating a responsibility definition, see [Create a responsibility definition](t_CreateAResponsibilityDefinition.md).

**Note:** The need for domain separation in configuring access records is determined by the domain of the referenced responsibility.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Responsibility Definitions**.

2.  Select a responsibility definition record.

3.  From the Responsibility Access Configuration related list, select **New**.

4.  On the form, fill in the fields.

<table id="table_xqp_24b_1yb"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accessible entities

</td><td>

List

</td><td>

Entities accessible through this configuration.

</td></tr><tr><td>

Access levels

</td><td>

List

</td><td>

Operations enabled on the accessible entities. The list shows the access levels, including read, write, and full.

**Note:** Full represents a special access level that is equivalent to read, write, and create.

</td></tr><tr><td>

Active

</td><td>

True/False

</td><td>

Status of the configuration. By using this functionality, you can enable or disable a responsibility access configuration.

 The default value is **True**.

</td></tr><tr><td>

Applies to relationship

</td><td>

Table name

</td><td>

Relationship table to establish connections between a user, an accessible entity, and the respective responsibilities.

</td></tr><tr><td>

Responsibility

</td><td>

Reference

</td><td>

Responsibility applicable to this configuration.

</td></tr><tr><td>

Restrict access to

</td><td>

List

</td><td>

Access that is restricted to a set of records of the accessible entities.

</td></tr><tr><td>

Roles

</td><td>

User roles

</td><td>

Roles required in addition to responsibilities to get the access.

</td></tr></tbody>
</table>    **Note:** To create new entries to the **Applies to Relationship**, **Access Levels**, or **Accessible Entities** fields in the Responsibility Access Configuration table, you must migrate all existing configurations for these fields in the global.CSMRelationshipConstantsSNC script include.

5.  Select **Submit**.


