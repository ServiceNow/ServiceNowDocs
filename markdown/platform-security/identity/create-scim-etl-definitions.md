---
title: Create a SCIM ETL definition
description: Use the SCIM ETL definitions to map the custom attributes with the sys\_user or sys\_user\_group tables.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [SCIM customization, SCIM Provider, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Create a SCIM ETL definition

Use the SCIM ETL definitions to map the custom attributes with the sys\_user or sys\_user\_group tables.

## Before you begin

Role required: scim\_config\_admin

**Warning:** Grant this role carefully. The scim\_config\_admin role is equivalent to giving the user the admin role, where the scim\_config\_admin role can insert new records into the tables that can bypass business logic or ACL protection.

**Note:**

-   SCIM Group and SCIM User ETL definitions are part of the base system for resource mapping. You can use the same resource mappings and change the criteria as required, or you can create new resource mappings.
-   There is no support for \[\*\] fields through RTE in SCIM mapping.

## Procedure

1.  Follow the instructions in Create Extract Transform Load \(ETL\) definitions.

2.  Open the newly created record and view the details.

3.  In the ETL Entities section, create an entity by clicking **New**.

    You have to create entities for the following users:

    -   scim-user: For the fields that are from SCIM.
    -   user \(sys\_user\) or group \(sys\_user\_group\) table: For the fields that you want to map from the database table with SCIM. For example, for customization of user details through SCIM, you can use the sys\_user table.
    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the ETL entity.|
        |Application|Application scope for this record.|
        |Table|Target table for the ETL entity.|
        |Definition|Selected ETL entity.|
        |Path|Unique path for this entity. Do not specify any path for the entity representing the import set table. When an entity represents a collection, the path must end with an asterisk \[\*\]. This requirement applies to intermediate entries and the target table entity.|
        |Synchronize Inserts|Option to guarantee only one record with unique coalesced field values by synchronizing record inserts.|
        |Run business rules|Option to run business rules.|

    2.  Click **Submit**.

        The ETL entities are created for scim-user and user tables. You have to create ETL entity fields within these ETL entities, and map both entities by creating an RTE Entity Mapping.

        ![ETL Entity](../images/etl-entity.png)

4.  Create the entities and map them.

    1.  Open the submitted record \(scim-user and user\).

    2.  In the ETL Entity fields, add the fields by clicking **New**.

    3.  On the form, fill in the fields.

<table id="table_rth_cjq_2tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the ETL Entity field definition.

</td></tr><tr><td>

Application

</td><td>

Selected ETL entity that this field definition belongs to.

</td></tr><tr><td>

Field/Path

</td><td>

This field is either a column or path.-   The field is a column name when the entity is the Import or Target table.
-   The field is a path when the field has nested structures.


</td></tr><tr><td>

Entity

</td><td>

Entity that this operation applies to. Choose the entity using the look-up icon.

</td></tr><tr><td>

Coercion action

</td><td>

What the system should do if a reference or choice could not be found. Options are as follows:-   **Create**: Create a new reference or choice. Assign the reference or choice to the current record.
-   **Reject**: Do not save the whole record to the database.
-   **Ignore**: Set the current value as empty.


</td></tr><tr><td>

Definition

</td><td>

Selected ETL entity that this field definition belongs to.

</td></tr><tr><td>

Coalesce

</td><td>

Option to query the existing records.

</td></tr></tbody>
</table>        ![ETL Entity field](../images/etl-entity-field.png)

    4.  Submit the entries by clicking **Submit**.

        You can add multiple entries as your ETL Entity field based on your requirement.

        The scim-user ETL entity can have entities with the core extension \(user\), the ServiceNow extension, or custom extension.

        ![Scim-user entities](../images/scim-user-etl-definitions.png)

        The user ETL entity can have entities from the database table. For example, sys\_user table.

        ![User entities](../images/user-etl-definitions.png)

        **Note:** To add a filter in the incoming SCIM fields, use an underscore \(`_`\). This underscore translates to an EQ filter. For example, the attribute **email.type\_work.value** applies the SCIM filter of email **\[type eq “work”\].value**.

        After the fields are created in both the scim-user and user ETL Entity records, you have to create an RTE Entity mapping record. You must then specify the source and target definition to map both the fields.

5.  In the RTE Entity Mappings section, create an entity mapping by clicking **New**

6.  On the form, fill the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the mapping.|
    |Source Entity|Source entity for the mapping.|
    |Target Entity|Target entity for the mapping.|
    |Order|Order in which the mapping should be processed.|
    |Is Conditional|Option to designate the mapping as conditional.|
    |Condition Script|Script that defines the conditions that must be met for the mapping.|
    |Application|Application scope for this record.|
    |Definition|Selected ETL entity that this mapping belongs to.|
    |Ignore|Option to designate if this ETL entity mapping should be ignored when performing data integrations using Robust Import Set Transformation \(RTE\).|

    ![RTE Entity Mapping](../images/etl-definitions-rte.png)

7.  Click **Submit**.

    The following example shows a record created for mapping both the scim-user and user ETL Entity records.

    ![scim-user-mappings](../images/scim-user-mappings.png)

8.  Open the submitted record \(scim-user-mappings\) and create a mapping between the scim-user and user ETL Entity records.

    1.  In the RTE Field Mappings section, click **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Source Field|Application scope for this record.|
        |Application|Selected ETL entity that this field definition belongs to.|
        |Target Field|Output ETL field for the operation if the operation takes a single output.|
        |Entity Mapping|Entity mapping that this operation applies to.|
        |Referenced Entity|Entity that is referenced and the operation that it applies to.|
        |Definition|Selected ETL entity that this field definition belongs to.|
        |Order|Order in which the operation runs on the entity.|

        ![RTE Field Mapping](../images/rte-etl-field-mapping.png)

        The source field **Home Address - Country** \(scim-user ETL Entity\) maps the target field as **Country** \(user ETL Entity\).

    3.  Submit the entries by clicking **Submit**.

        You can add multiple entries as your RTE Entity mappings based on your requirement.

        ![RTE Entity Mappings](../images/rte-mappings.png)

        The source fields and targets fields are mapped as configured. When you perform CRUD operations using SCIM, the customized values are updated in the respective table.


## Result

These ETL definitions and mappings enable you to extract data from a source table, transform the data as desired, and load the data into a target table.

**Related topics**  


[bundle-crint.create-etl-definitions]

