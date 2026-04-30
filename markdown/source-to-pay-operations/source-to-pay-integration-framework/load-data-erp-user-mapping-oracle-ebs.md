---
title: Load data to ERP user-mapping table for Oracle EBS
description: Set up Oracle EBS and ERP User ID mapping for the integration to work. The mapping is maintained for all active users who have the procurement buyer role in ERP. These users should be used in the requisition assignment rule.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Load data to ERP user-mapping table for Oracle EBS

Set up Oracle EBS and ERP User ID mapping for the integration to work. The mapping is maintained for all active users who have the procurement buyer role in ERP. These users should be used in the requisition assignment rule.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Select **Create table** and enter a label for the new table in the **Label** field.

3.  In the **Source of the import** field, select the **File** option.

4.  Select **Choose File** to import the source Excel spreadsheet.

    ![Load data to ERP user mapping table for Oracle EBS](../image/oracle-ebs-load-data.png "Load data to ERP user-mapping table for Oracle EBS")

5.  If appropriate, specify the Work sheet and Header row number.

6.  Select **Submit**.

    The imported data is now available in the new Import Set table.

7.  [Create a transform map](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) to define the field mapping between columns of the import set and columns of the target ERP User Mapping \[sn\_fcms\_intg\_erp\_user\_map\] table.

    The ERP User Mapping table maintains mapping between ERP user IDs and ServiceNow user IDs.

8.  Transform the data from the import set table to the target table.

    For more information, see [Run an import](https://www.servicenow.com/docs/access?context=t_RunImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

    The data is imported into the Oracle EBS ERP User Mapping `(sn_fcms_intg_erp_user_map)` table.


## What to do next

Verify that the data records are imported into the target table. You can view the Oracle EBS ERP user mappings by navigating to **Finance - ERP Integration** &gt; **ERP Users**.

**Note:** If an ERP user mapping isn’t required, you can deactivate it. To deactivate a mapping, in the ERP User Mapping form, select the **Inactive** check box.

**Parent Topic:**[Configure the Source-to-Pay integration with Oracle EBS](../concept/configuring-source-to-pay-oracle-ebs-integration.md)

**Related topics**  


[ERP source configuration for Oracle EBS](../concept/erp-source-configuration-oracle.md)

[Define ERP source configuration for Oracle EBS](define-erp-source-oracle.md)

[Configure integration services for Oracle EBS](configure-service-maps-oracle-ebs.md)

[Look up primary data in Oracle EBS](../concept/look-up-primary-data-oracle-ebs.md)

[Scheduled jobs to look up primary data in Oracle EBS](../concept/scheduled-jobs-to-primary-data-oracle-ebs.md)

