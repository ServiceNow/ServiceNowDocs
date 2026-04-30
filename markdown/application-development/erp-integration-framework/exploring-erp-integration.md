---
title: Exploring Zero Copy Connector for ERP
description: Zero Copy Connector for ERP enables you to connect to the ERP \(Enterprise Resource Planning\) system to send updates and extract data to remote tables and extraction tables for use on the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Exploring Zero Copy Connector for ERP

Zero Copy Connector for ERP enables you to connect to the ERP \(Enterprise Resource Planning\) system to send updates and extract data to remote tables and extraction tables for use on the ServiceNow AI Platform.

## Overview of Zero Copy Connector for ERP

Zero Copy Connector for ERP functions as a platform within ServiceNow, offering a unified data model for ERP systems. Zero Copy Connector for ERP enables you to manage tables that contain both standard and custom fields grouped within ERP models. You can send updates to and extract data from ERP tables on the system of record and store it in a remote table or an extraction table, depending on the size of data sets and refresh needs.

-   Remote tables get their records from running an associated script against an external data source.
-   Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.

In addition to retrieving data, Zero Copy Connector for ERP can also update the ERP system using a BAPI \(Business Application Programming Interface\) or OData and an HTTP connection.

The unified data model of the ServiceNow AI Platform ensures seamless integration of ERP data into the ServiceNow AI Platform. Zero Copy Connector for ERP streamlines ERP data management, making it accessible and actionable within the ServiceNow AI Platform and ServiceNow instances.

**Note:** Zero Copy Connector for ERP doesn't replicate data into the ServiceNow AI Platform. It mirrors data that lives in the ERP system of record, and remains protected there.

## Zero Copy Connector for ERP workflow

1.  Have your administrator use the Connections and Credentials app to configure credentials to connect to the ERP system of record. For more information, see [Configure the Zero Copy Connector for ERP credentials and connection](../task/set-up-erp-integration-connection.md).
2.  Create an ERP system in Zero Copy Connector for ERP using the connection and credentials alias that you configured. For more information, see [Create an ERP system in Zero Copy Connector for ERP](../task/create-an-erp-system.md).

    **Note:** The rest of the workflow steps are in Zero Copy Connector for ERP. Build your ERP systems, ERP models, and tables in a development instance, and then promote them to a production instance when you're ready. For more information, see [Managing app deployments using Pipelines and Deployments](../../app-engine-studio/concept/aes-review-apps-p-and-d.md).

3.  Clone or create an ERP model that scans the specified ERP module in the system of record for available tables and fields. Note the tables and fields in the ERP model for use in extraction and remote tables, as well as for mapping parameters to read and update the system of record.For more information, see [Clone an ERP model in Zero Copy Connector for ERP](../task/erp-canvas-clone-data-model.md).
4.  Create read and update operations to connect to the ERP system by adding tables, mapping fields, and building table joins to include additional data in the ERP model. For more information, see the following topics:
    -   [Managing how models read and update the ERP system](erpc-managing-models-read.md)
    -   [Add joins between ERP tables](../task/erp-canvas-add-join-data-model.md)
5.  Work with remote tables to make them available for use as a data source, such as when building apps in App Engine Studio. Remote tables get their records from running an associated script against an external data source. For more information, see the following topics:
    -   [View and edit ERP remote table details with Zero Copy Connector for ERP](../task/erpi-find-tables.md)
    -   [Customize fields for an ERP remote table in Zero Copy Connector for ERP](../task/erp-canvas-build-remote-table.md)
    -   [Query a remote table using Zero Copy Connector for ERP](../task/erp-canvas-query-remote-table.md)
6.  Work with ETL extraction tables to regularly scan the system of record and extract data to a staging table. Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.
    -   Create as many separate extraction tables as needed, such as one for each supported country. For more information, see [Extracting and transforming data in Zero Copy Connector for ERP](erp-canvas-extraction-tables.md).
    -   You must first create the table transform map that connects the source table \(on the system of record\) to a Glide table on the ServiceNow AI Platform. For more information on creating table transform maps, see [Create a transform map](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).
    -   Extraction processes are configured in the ServiceNow app that uses them, for example, Workflow Studio.
    -   After the extraction process is run, use import sets to map imported data into ServiceNow AI Platform tables. For more information, see [Import sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).
7.  Build flows in Workflow Studio to specify details for when you query or update the ERP \(Enterprise Resource Planning\) system. For more information, see [Building flows to read or update the ERP system](erp-canvas-build-flow-operation.md).
8.  Move the ERP systems, ERP models, tables, operations, and flows to a production environment when they're ready. For more information, see [Managing ERP development pipelines in Zero Copy Connector for ERP](manage-erp-tables-pipelines.md).
9.  Use the ERP data as the data source when building apps on the ServiceNow AI Platform using:
    -   App Engine Studio: For more information, see [Create a data model for your application](../../app-engine-studio/concept/add-data.md).
    -   Flows in Workflow Studio: For more information, see [Configuring flows](https://www.servicenow.com/docs/access?context=configuring-flow-designer&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).
    -   Playbooks in Workflow Studio: For more information, see [Getting started with Process Automation](https://www.servicenow.com/docs/access?context=getting-started-process-automation&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).
    -   Table Builder: For more information, see [Data in Table Builder](../../../administer/form-builder/concept/table-builder.md).
    -   UI Builder: For more information, see [Dynamically expose data in UI Builder pages \(advanced feature\)](../../../administer/ui-builder/concept/data-resources.md).
    -   Workspace Builder: For more information, see [Configure a record page for a workspace in Workspace Builder](../../app-engine-studio/task/configure-record-page-workspace.md).

## Benefits of Zero Copy Connector for ERP

<table id="table_cjc_j1y_mwb"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Role

</th></tr></thead><tbody><tr><td>

Configure connections to the system of record

</td><td>

[Working with ERP systems in Zero Copy Connector for ERP](erp-canvas-work-with-systems.md)

</td><td>

sn\_erp\_integration.erp\_admin

</td></tr><tr><td>

Build ERP models to create read and update operations and organize mirrored ERP data

</td><td>

[Building and managing ERP models to work with ERP data](work-with-erp-data-models.md)

</td><td>

sn\_erp\_integration.erp\_admin

</td></tr><tr><td>

Work with and query remote tables to view ERP data on the system of record

</td><td>

[Using ERP remote tables in Zero Copy Connector for ERP](erp-canvas-work-with-remote-tables.md)

</td><td>

-   To modify remote tables: sn\_erp\_integration.erp\_admin
-   To read remote tables: sn\_erp\_integration.erp\_user

</td></tr><tr><td>

Access standard remote tables

</td><td>

[Standard remote tables for Zero Copy Connector for ERP](../reference/erpi-standard-remote-tables.md)

</td><td>

-   sn\_erp\_integration.erp\_user
-   Additional, table-specific roles are required. For more information, see [Zero Copy Connector for ERP roles](../reference/erp-canvas-roles.md).

</td></tr><tr><td>

Configure extraction tables to regularly pull custom data from the ERP system

</td><td>

[Extracting and transforming data in Zero Copy Connector for ERP](erp-canvas-extraction-tables.md)

</td><td>

sn\_erp\_integration.erp\_admin

</td></tr></tbody>
</table>## Additional resources for Zero Copy Connector for ERP

<table id="table_flh_vjt_gtb"><thead><tr><th>

Learn more about Zero Copy Connector for ERP

</th><th>

ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="3">

Zero Copy Connector for ERP is a ServiceNow app that enables you to simplify the use of ERP data from the system of record, such as SAP.

</td><td>

![](../../../reuse/icons/brand-icons/bus-whitepaper.svg) [App Engine for ERP Overview on ServiceNow University](https://learning.servicenow.com/lxp/en/app-engine/enterprise-resource-planning-clean-core-with-app-engine-overview?id=learning_course_prev&course_id=ee84d77293bc35903cc0322d6cba10eb)

 **Note:** You must log in to ServiceNow University to access this resource.

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-3-person.svg) [ServiceNow Community site](https://www.servicenow.com/community/?id=community_search&q=erp%20canvas&spa=1)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-application-developer.svg) [Video: Unlock the full potential of your ERP system](https://www.youtube.com/watch?v=R66HqYLfEc8)

</td></tr></tbody>
</table>-   **[Identifying ERP candidates to replatform with Zero Copy Connector for ERP and ERP-CM](erpi-and-ecm-together.md)**  
Zero Copy Connector for ERP enables you to connect to your ERP \(Enterprise Resource Planning\) system of record, and to organize its data.
-   **[Zero Copy Connector for ERP custom field example](ecm-example-case.md)**  
Zero Copy Connector for ERP helps you identify custom ERP \(Enterprise Resource Planning\) apps and fields in the system of record to access their data on the ServiceNow AI Platform. The ERP system can have both standard and custom fields that are accessed by Zero Copy Connector for ERP.
-   **[Zero Copy Connector for ERP and security](erp-canvas-and-security.md)**  
In addition to role-based security and access control, Zero Copy Connector for ERP protects personally identifiable data in other ways.
-   **[Guided tours in ERP Canvas](guided-tours-in-erp-canvas.md)**  
Learn about Zero Copy Connector for ERP guided tours, including how to access and take them to build your knowledge of Zero Copy Connector for ERP.
-   **[Get help with Zero Copy Connector for ERP](erp-canvas-get-help-now.md)**  
To get help with Zero Copy Connector for ERP, your ServiceNow instance, plugins, permissions, and more, watch a short video to contact the ServiceNow admin who works in your company.

**Parent Topic:**[Zero Copy Connector for ERP](erp-integration-overview.md)

