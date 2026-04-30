---
title: Extract Transform Load \(ETL\) definition overview
description: ETL definitions extract data from a source table, transform the data as desired, and load the data into one or more target tables. ETL definitions also support nested data structures.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Robust Import Set Transformers, Import sets, Imports, Creating integrations with applications]
---

# Extract Transform Load \(ETL\) definition overview

ETL definitions extract data from a source table, transform the data as desired, and load the data into one or more target tables. ETL definitions also support nested data structures.

## ETL definitions specify how to map data

Importing data starts with a [data source](c_DataSources.md). A data source specifies the type of data that you want to extract and its location. After the data is extracted, it's loaded into a staging, or import set, table. Then an ETL definition specifies how to map the data into one or more target tables in ServiceNow. You can create ETL definitions that map data to ServiceNow tables while still maintaining the foreign key and unique key constraints. ![Overview of the import process using an ETL definition.](../image/etl-definition-overview.png)

## ETL entities represent input data and target tables

ETL definitions are based on entities. Every ETL definition that you create must have entities associated with it. Entities represent input data and target tables.

-   Input data is the data that has been loaded into the staging table.
-   Target tables are the ServiceNow tables where you want your data to end up.

Mappings and operations are also based on entities, so it's helpful to create entities early, when you create the definition.

The following image shows an example of an ETL definition for Computer. This definition has three entities associated with it. The Import Set entity represents the input data, the data loaded from an Excel file into a staging table. The table for the Import Set entity is set to **None**. Computer and Disk are the target entities. They represent two ServiceNow tables named Computers \[sn\_etl\_demo\_computer\] and Disk \[sn\_etl\_demo\_disk\]. The data from the staging table will be loaded into the two target tables. ![An ETL definition for Computer showing three ETL entities for Computer, Disk, and Import Set.](../image/ETL-definition.png)

## Input entities

Input entities represent the extracted data that was loaded into the staging table. Input entities have ETL entity fields to represent the import set table columns or, for a single column mode, JSON keys. You can create entity fields by selecting **New** on the ETL Entity fields tab.

The following image shows the Import Set entity from the Computer ETL definition. The Import Set entity represents the input data loaded from an Excel file into the Computers \[sn\_elt\_demo\_computers\_stage\] staging table. The Import Set entity has an entity field for each column in the staging table. ![The Import Set entity has an entity field for each column in the staging table.](../image/input-entity-example.png)

## Target entities

Target Entities represent the target tables in ServiceNow. The following image shows the Disk target entity from the Computer ETL definition. Disk represents the sn\_etl\_demo\_disk target table. It has entity fields to represent table columns and temporary values to apply operations.![The Computer and Disk target entities have entity fields to represent table columns and temp values for operations.](../image/target-entity-example.png)

Each entity field has a name, a reference or path field, a coalesce field, and a coercion action.

-   **Reference field**

    Special field where a row in one table refers to a row in a second table by storing the sys\_id of the second table's row as a column value in the first table's row. Though the reference is stored as a sys\_id, when the data is imported, it's imported as values. So for reference fields, you map the values of the unique fields of the referred table to the imported data. Ultimately, the system will use the values to find the associated record, retrieve the sys\_id, and store it in the appropriate column.

    For example, in the Disk entity mentioned previously, the sn\_etl\_demo\_disk table has a reference to the computer using the reference field **computer**. However, the imported data only contains the computer ID, which can be used to uniquely identify the computer. So in the Disk entity, the referenced field path \(computer.id\) specifies the column of the Computer table as well.

    If there's more than one field for a unique key, all the field values should be given by adding multiple fields. For example, in the following image, the sn\_etl\_demo\_worker table has a reference to the sn\_etl\_demo\_address table. The sn\_etl\_demo\_address table has three columns \(number, street, and postal code\) as unique keys. Therefore, the Worker entity has three fields for unique key columns. Reference fields can be used as coalesce fields as well. ![The Worker entity has three fields for unique key columns.](../image/target-entity-reference-fields.png)

-   **Coalesce field**

    Specifies the unique key for a target entity. The system uses the coalesce field to determine whether to update an existing record or insert a new one. If the Coalesce field is true, and the system finds an existing record with the same coalesce field value, it updates the existing record. For the sn\_etl\_demo\_disk table shown previously, in the Disk entity, the Serial No column is unique for all the disk entries, so it is specified as a coalesce field.

-   **Coercion action**

    For reference fields, specifies what to do when a row with the unique key value doesn't exist in the referred table. The Coercion action has the following options.

    -   **Create** a new row in the referred table and assign it to the target row.
    -   **Ignore** the reference field value. The reference column is saved as empty.
    -   **Reject** the reference field value. It is not inserted into or updated in the target table.

## Robust Transform Engine \(RTE\) entity operations modify data

Entity operations modify input data before storing it in a target table. The following image shows an example of a concatenation operation. In the ETL definition for Computer, the imported data contains both a type and a version. However, the target table requires a value that is a combination of the type and version. So the Computer entity uses a concatenation operation to concatenate type and version. Entity operations can only be performed on entity fields, so in this example, two temp fields are created to copy the import set values. ![An RTE Entity Concatenation Operation for the Computer entity.](../image/entity-operations-example.png)

## RTE entity mappings specify field mappings

After creating the input and target entities with their entity fields and operations, create an RTE entity mapping for each target entity. RTE entity mappings specify how fields in the input entity are mapped to fields in the target entities. In the ETL definition for Computer, there are two RTE entity mappings. One, shown in the following image, maps input data to the Computer entity fields. The other maps input data to the Disk entity fields. ![RTE Entity Mapping specifying how to map data from the Import Set to the Computer entity.](../image/RTE-entity-mapping-example.png)

## Nested data in ETL definitions

With JSON data imports, you might need to import records with JSON arrays, or records that import more than one row for the same table. ETL definitions support these payloads with a small change to the paths. The following JSON data has an array for email information. You can import this data by modifying the path or paths in the input or target entities as shown in the next two images.

```
{
      "id": "123",
      "name": "Jhon",
      "emails": [
        {
          "address": "jhon@servicenow.com",
          "type": "work"
        },
        {
          "address": "jhon@gmail.com",
          "type": "personal"
        }
      ]
    }

```

-   **Input entities with nested data**

    Input entities for nested data also represent the input JSON data. Like imports without nested data, they have entity fields to represent the values. The only difference is that paths with arrays are specified with an asterisk \(\*\). The following image shows how the paths to address and type are specified as emails\[\*\].address and emails\[\*\].type.![ETL entity for nested input data showing the use of an asterisk to specify a value within an array.](../image/input-entity-nested-data.png)

-   **Target entities with nested data**

    Target entities with nested data are also like the target entities in a normal import except that the path ends with an asterisk \(\*\). The asterisk tells the system to process the entity as an array. In the Email entity, the target path is specified as email\[\*\]. Coalesce fields, reference fields, and coercion actions work the same as with normal imports.![ETL entity for nested input data showing the use of an asterisk to specify an array.](../image/target-entity-nested-data.png)

-   **RTE entity mappings with nested data**

    RTE entity mappings for nested data are like normal mappings. Any field from the hierarchy can be assigned to the entity.


