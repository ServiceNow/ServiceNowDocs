---
title: Create Extract Transform Load \(ETL\) definitions
description: Create ETL definitions to extract data from a source table, transform the data as desired, and load the data into multiple target tables. ETL definitions also support nested data structures.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Robust Import Set Transformers, Import sets, Imports, Workflow Data Fabric]
---

# Create Extract Transform Load \(ETL\) definitions

Create ETL definitions to extract data from a source table, transform the data as desired, and load the data into multiple target tables. ETL definitions also support nested data structures.

## Before you begin

Role required: import\_transformer

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **ETL Definitions**.

2.  Click **New**.

3.  Complete the form.

<table id="table_fnb_s3p_3jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the ETL definition.

</td></tr><tr><td>

Description

</td><td>

Description of the ETL definition.

</td></tr><tr><td>

Copy empty fields

</td><td>

Option to copy empty field values. If the incoming data has a field with an empty value, you can either copy the empty value or ignore it and keep the existing value.

</td></tr><tr><td>

Execute onBefore script

</td><td>

Option to run a script before inserting or updating data.The onBefore script has three parameters.

-   **source**: The source data from the import record.
-   **target**: The transformed data from the import record. In the onBefore script, this parameter accesses transformed data before it's inserted into the target table.
-   **importLog**: The log that records information about data import activity.
The onBefore script has two variables.

-   **ignore**. Type: Boolean. When **true**, the specified import set row is ignored.
-   **ignore\_reason**. Type: String. Message describing why the import set row was ignored.


</td></tr><tr><td>

Execute onAfter script

</td><td>

Option to run a script after inserting or updating data.The onAfter script has three parameters.

-   **source**: The source data from the import record.
-   **target**: The transformed data from the import record. In the onAfter script, this parameter accesses transformed data after it's inserted into the target table. Once a record is inserted or updated, it has a sys\_id.
-   **importLog**: The log that records information about data import activity.


</td></tr><tr><td>

Application

</td><td>

Application scope for this record.

</td></tr><tr><td>

Active

</td><td>

Selected if the ETL definition is active. Unselected if the ETL definition isn't active.

</td></tr></tbody>
</table>4.  Click **Submit**.


## Example

In this example, the ETL Definition for Worker has both an onBefore and onAfter script. In the onBefore script, the source record with an id of 124 is ignored because that worker has already resigned. The source data and target data are both written to the import log. Finally, the script iterates through the transformed values of the sn\_etl\_demo\_worker table to get each worker's ID and name and record them in the import log.

In the onAfter script, the source and target data are both written to the import log. The script again iterates through the transformed values of the sn\_etl\_demo\_worker table. Now that the data has been inserted into the target table, each record has a sys\_id. The script records each worker's Sys ID, ID, and name in the import log.

![ETL Definition example with onBefore and onAfter scripts.](../image/etl-definition-example.png)

**Note:**

-   For creating these definitions and mapping using a guided or step-by-step experience, refer to [Integration Hub - Import](../../integrationhub/concept/integrationhub-imports.md).
-   If your target table or application is related to CMDB, use the IntegrationHub ETL guided experience.

**Related topics**  


[Define ETL entities](define-etl-entities.md)

[Define ETL entity mappings](define-etl-mappings.md)

[Create ETL entity field definitions](create-etl-field-definitions.md)

[Define Robust Transform Engine operations](define-rte-operations.md)

