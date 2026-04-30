---
title: Load data to ERP user-mapping table for Oracle Financial Cloud
description: Set up Oracle Financial Cloud and ERP User ID mapping for the integration to work. The mapping is maintained for all active users who have the procurement buyer role in ERP. These users should be used in the requisition assignment rule.
locale: en-US
release: zurich
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Load data to ERP user-mapping table for Oracle Financial Cloud

Set up Oracle Financial Cloud and ERP User ID mapping for the integration to work. The mapping is maintained for all active users who have the procurement buyer role in ERP. These users should be used in the requisition assignment rule.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Select **Create table** and enter a label for the new table in the **Label** field.

3.  In the **Source of the import** field, select the **File** option.

4.  Select **Choose File** to import the source Excel spreadsheet.

    ![Load data to ERP user-mapping table for Oracle Financial Cloud](../image/oracle-fin-load-data-erp.png "Load data to ERP user-mapping table for Oracle Financial Cloud")

5.  If appropriate, specify the Work sheet and Header row number.

6.  Select **Submit**.

    The imported data is now available in the new Import Set table.

7.  [Create a transform map](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) to define the field mapping between columns of the import set and columns of the target ERP User Mapping \[sn\_fcms\_intg\_erp\_user\_map\] table.

    The ERP User Mapping table maintains mapping between ERP user IDs and ServiceNow user IDs.

8.  Transform the data from the import set table to the target table.

    For more information, see [Run an import](https://www.servicenow.com/docs/access?context=t_RunImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

    The data is imported into the Oracle Financial Cloud ERP User Mapping `(sn_fcms_intg_erp_user_map)` table.


## What to do next

Verify that the data records are imported into the target table. You can view the Oracle Financial Cloud ERP user mappings by navigating to **Finance - ERP Integration** &gt; **ERP Users**.

**Note:** If an ERP user mapping isn’t required, you can deactivate it. To deactivate a mapping, in the ERP User Mapping form, select the **Inactive** check box.

