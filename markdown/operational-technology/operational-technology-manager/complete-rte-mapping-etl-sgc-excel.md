---
title: Configure the RTE mapping for ETL
description: Configure the Robust Transform Engine \(RTE\) mapping for the Extract Transform Load \(ETL\). The ETL process transfers custom column data from the import set to the target Configuration Management Database \(CMDB\) class.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/operational-technology/operational-technology-manager/complete-rte-mapping-etl-sgc-excel.html
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 3
breadcrumb: [Add a custom column to the staging table, Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Configure the RTE mapping for ETL

Configure the Robust Transform Engine \(RTE\) mapping for the Extract Transform Load \(ETL\). The ETL process transfers custom column data from the import set to the target Configuration Management Database \(CMDB\) class.

## Before you begin

-   Complete the update for the column mapping script. The custom column must be included in the JSON file exported to the import set before the RTE can map it. For more information, see [Update the column mapping script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/operational-technology/operational-technology-manager/update-column-mapping-script-sgc-excel.md).
-   Role required: admin

## About this task

When you select the **Trigger CMDB Import** UI action, the exported staging records are loaded into the SG-OT Asset Excel Import set and processed through the following RTE entities:

-   **Import**

    The raw field on the import set record \(the JSON key produced by importSetColumnsVsStagingColumnsMap\).

-   **temp**

    An intermediate staging entity used to hold the value during transformation.

-   **CI class stub**

    The target field on the CMDB CI class that stores the value.


The data is processed from the Import to the temp to the CI class stub. You must define a field for each entity the data passes through and map each pair of entities.

**Warning:** Use the same column name in the RTE entity fields as the key you used in the **importSetColumnsVsStagingColumnsMap** object. Using different names results in the RTE not finding the data to transform.

For more information about triggering the CMDB import process, see [Trigger a CMDB import for valid staging records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/operational-technology/operational-technology-manager/trigger-cmdb-import.md).

## Procedure

1.  Create a field for the Import entity.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_rte_eb_field.do` to open a new record form in the RTE Entity Field \(sys\_rte\_eb\_field\) table.

    3.  In the **Name** and **Field/Path** fields, enter the name of your custom column.

    4.  Set the **Entity** field to **Import**.

    5.  Set the **Definition** field to **SG-OT Asset Excel Import**.

    6.  Select **Submit**.

2.  Create a field for the temp entity.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_rte_eb_field.do` to open a new record form in the RTE Entity Field \(sys\_rte\_eb\_field\) table.

    3.  In the **Name** and **Field/Path** fields, enter the name of your custom column.

    4.  Set the **Entity** field to **temp**.

    5.  Set the **Definition** field to **SG-OT Asset Excel Import**.

    6.  Select **Submit**.

3.  Create a field for the configuration item \(CI\) class entity.

    **Note:** Only complete this step if the custom field is being added to the target CMDB CI class.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_rte_eb_field.do` to open a new record form in the RTE Entity Field \(sys\_rte\_eb\_field\) table.

    3.  In the **Name** and **Field/Path** fields, enter the name of your custom column.

    4.  Set the **Entity** field to the CMDB class stub you want to target.

    5.  Set the **Definition** field to **SG-OT Asset Excel Import**.

    6.  Select **Submit**.

4.  Create a mapping from Import to temp.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_rte_eb_field_mapping.do` to open a new record form in the RTE Entity Field Mapping \(sys\_rte\_eb\_field\_mapping\) table.

    3.  Set the **Source** to the custom column from the Import entity.

    4.  Set the **Target Field** field to the custom column from the temp entity.

    5.  In the **Order** field, enter any value.

        For example, `100`.

    6.  Set the **Entity Mapping** field to `impTotemp`.

    7.  Set the **Definition** field to **SG-OT Asset Excel Import**.

    8.  Select **Submit**.

5.  Create a mapping from temp to the CMDB class stub.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_rte_eb_field_mapping.do` to open a new record form in the RTE Entity Field Mapping \(sys\_rte\_eb\_field\_mapping\) table.

    3.  Set the **Source** to the custom column from the temp entity.

    4.  Set the **Target Field** field to the matching column from the target CMDB class entity stub.

    5.  In the **Order** field, enter any value.

        For example, `100`.

    6.  Set the **Entity Mapping** field to `tempTo` followed by the CMDB class you're targeting.

    7.  Set the **Definition** field to **SG-OT Asset Excel Import**.

    8.  Select **Submit**.


## Result

After you configure these mappings, the custom column data populates correctly in the CMDB when you select the **Trigger CMDB Import** UI action.

**Parent Topic:**[Add a custom column to the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/operational-technology/operational-technology-manager/add-custom-column-staging-table.md)

