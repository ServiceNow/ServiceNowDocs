---
title: Create a table transform map from an extraction table
description: In Zero Copy Connector for ERP, create a table transform map from an extraction table and map the source fields with target fields.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erpc-create-table-transform-map-from-extraction-table.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Extracting and transforming data in Zero Copy Connector for ERP, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Create a table transform map from an extraction table

In Zero Copy Connector for ERP, create a table transform map from an extraction table and map the source fields with target fields.

## Before you begin

Role required: admin

Confirm that you have an extraction table associated with a model containing output parameters. For more information, see [Add a new ERP extraction table in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-add-new-extraction-table.md) and [Choose output parameters for an ERP model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-manage-outputs.md).

**Note:** The following procedure always generates a new transform map and new staging table. To modify an existing transform map or an existing staging table, navigate to the record and update manually. Transform maps are in **System Import Sets** &gt; **Administration** &gt; **Transform Maps** and staging tables are in **System Definition** &gt; **Tables**.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP extraction tables page by selecting the ERP extraction tables icon \(\[Omitted image "erpc-extraction-table-icon.png"\] Alt text: ERP extraction tables navigation icon\) in the side panel.

3.  Select an extraction table to work with by selecting the **Name**.

    The table should have an ERP model that contains some output parameters.

4.  Select **Generate mapping**.

5.  In **Select mapping table**, specify the destination table for the data obtained from an external source.

    \[Omitted image "erpc-transform-map-extraction-table1.png"\] Alt text: Generate mapping overlay with select mapping table field highlighted.

6.  Create the mappings by selecting an output in the **Available model outputs** column and then selecting a column in **Available columns**.

    As you work, the mappings are saved in the **Field Mapping** section to create the import map staging table and the transform map. For general information, see [Import sets key concepts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/system-import-sets/c_ImportSetsKeyConcepts.md) and [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md).

    \[Omitted image "erpc-transform-map-extraction-table2.png"\] Alt text: Generate mapping overlay with select mapping table field highlighted.

    To change a mapping, you can drag the items within the **Selected model outputs** column or the **Selected columns** column. As you make changes, the **Field Mapping** section updates automatically.

7.  In the **Field Mapping** section, select the **Coalesce** option for each mapping.

    For more information, see [Updating records using coalesce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/integrate-applications/system-import-sets/c_ImportSetCoalesce.md).

8.  Select **Save**.

    The import set staging table and a transform map that can be used by Zero Copy Connector for ERP to push the data into the destination table are generated. The extraction table record opens. A confirmation message is displayed stating that the staging table was generated and there’s a link to the transform map.

9.  Select the link at the top to open the transform map.

    \[Omitted image "erpc-transform-map-extraction-table3.png"\] Alt text: Extraction table record with transform map link highlighted.

    In **Source table**, the staging table is listed with its auto-generated name. The **Field Maps** related list contains the fields you mapped.

10. Return to the extraction table record \(it might be open in a different browser tab\).

11. To view the transform map at any time, select the link in **Table transform map link**.


**Parent Topic:**[Extracting and transforming data in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-extraction-tables.md)

