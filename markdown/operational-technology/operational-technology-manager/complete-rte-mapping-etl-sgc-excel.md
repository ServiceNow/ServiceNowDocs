---
title: Complete the RTE mapping for ETL
description: Complete the Robust Transform Engine \(RTE\) mapping for the Extract Transform Load \(ETL\) so that the ETL process knows how to transform the custom column records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/operational-technology-manager/complete-rte-mapping-etl-sgc-excel.html
release: brazil
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-09-09"
reading_time_minutes: 2
breadcrumb: [Add a custom column to the staging table, Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Complete the RTE mapping for ETL

Complete the Robust Transform Engine \(RTE\) mapping for the Extract Transform Load \(ETL\) so that the ETL process knows how to transform the custom column records.

## Before you begin

Role required: admin

## About this task

To populate the custom column data in the Configuration Management Database \(CMDB\), the **Trigger CMDB Import** process is executred. In order for this to work correctly, you must set up the proper mappings so the ETL process can transform the custom column records.

For more information about the **Trigger CMDB Import** process, see [Trigger a CMDB import for valid staging records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/trigger-cmdb-import.md)

## Procedure

1.  Create a field for the Import entity.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_rte_eb_field.do` to open a new record form in the RTE Entity Field \(sys\_rte\_eb\_field\) table.

    3.  In the **Name** and **Field/Path** fields, enter the name of your custom column.

    4.  Set the **Entity** field to **Import**.

    5.  Set the **Definition** field to SG-OT Asset Excel Import.

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

    4.  Set the **Target Field** field to the to the custom column from the temp entity.

    5.  In the **Order** field, enter any value.

        For example, `100`.

    6.  Set the **Entity Mapping** field to `impTotemp`.

    7.  Set the **Definition** field to **SG-OT Asset Excel Import**.

    8.  Select **Submit**.

5.  Create a mapping from temp to the CMDB class stub.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_rte_eb_field_mapping.do` to open a new record form in the RTE Entity Field Mapping \(sys\_rte\_eb\_field\_mapping\) table.

    3.  Set the **Source** to the custom column from the temp entity.

    4.  Set the **Target Field** field to the to the matching column from the target CMDB class entity stub.

    5.  In the **Order** field, enter any value.

        For example, `100`.

    6.  Set the **Entity Mapping** field to `tempTo` followed by the CMDB class you're targeting.

    7.  Set the **Definition** field to **SG-OT Asset Excel Import**.

    8.  Select **Submit**.


## Result

Once you configure these mappings, the custom column data populates correctly in the CMDB when you select the **Trigger CMDB Import** UI action.

**Parent Topic:**[Add a custom column to the staging table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/operational-technology/operational-technology-manager/add-custom-column-staging-table.md)

