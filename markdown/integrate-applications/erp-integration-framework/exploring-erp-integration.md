---
title: Exploring Zero Copy Connector for ERP
description: Zero Copy Connector for ERP enables you to connect to the ERP \(Enterprise Resource Planning\) system to send updates and extract data to remote tables and extraction tables for use on the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/exploring-erp-integration.html
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Exploring Zero Copy Connector for ERP

Zero Copy Connector for ERP enables you to connect to the ERP \(Enterprise Resource Planning\) system to send updates and extract data to remote tables and extraction tables for use on the ServiceNow AI Platform.

## Overview of Zero Copy Connector for ERP

Zero Copy Connector for ERP functions as a platform within ServiceNow, offering a unified data model for ERP systems. Zero Copy Connector for ERP enables you to manage tables that contain both standard and custom fields grouped within ERP models. You can send updates to and extract data from ERP tables on the system of record. Store extracted data in a remote table or an extraction table, depending on the size of datasets and refresh needs.

-   Remote tables get their records from running an associated script against an external data source.
-   Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.

In addition to retrieving data, Zero Copy Connector for ERP can also update the ERP system using a BAPI \(Business Application Programming Interface\) or OData and an HTTP connection.

The unified data model of the ServiceNow AI Platform helps with the seamless integration of ERP data into the ServiceNow AI Platform. Zero Copy Connector for ERP streamlines ERP data management, making it accessible and actionable within the ServiceNow AI Platform and ServiceNow instances.

**Note:** Zero Copy Connector for ERP doesn't replicate data into the ServiceNow AI Platform. It mirrors data that lives in the ERP system of record, and remains protected there.

## Zero Copy Connector for ERP workflow

1.  Have your administrator use the Connections and Credentials app to configure credentials to connect to the ERP system of record. For more information, see [Connect to a system of record from Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/set-up-erp-integration-connection.md).
2.  Create an ERP system in Zero Copy Connector for ERP using the connection and credentials alias that you configured. For more information, see [Create an ERP system in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/create-an-erp-system.md).

    **Note:** The rest of the workflow steps are in Zero Copy Connector for ERP. Build your ERP systems, ERP models, and tables in a development instance, and then promote them to a production instance when you're ready. For more information, see .

3.  Clone or create an ERP model that scans the specified ERP module in the system of record for available tables and fields. Note the tables and fields in the ERP model for use in extraction and remote tables, as well as for mapping parameters to create records on, read, and update the system of record.For more information, see [Clone an ERP model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-clone-data-model.md).

    \[Omitted image "erp-explore-1.png"\] Alt text: Zero copy connector for ERP models tab displaying a list of several models.

4.  Add create, read, and update operations to connect to the ERP system by adding tables, mapping fields, and building table joins to include additional data in the ERP model. For more information, see the following topics:
    -   [Managing how models read and update the ERP system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erpc-managing-models-read.md)
    -   [Add joins between ERP tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-add-join-data-model.md)
5.  Work with remote tables to make them available for use as a data source, such as when building apps in App Engine Studio. Remote tables get their records from running an associated script against an external data source. For more information, see the following topics:
    -   [View and edit ERP remote table details with Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erpi-find-tables.md)
    -   [Customize fields for an ERP remote table in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-build-remote-table.md)
    -   [Query a remote table using Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-query-remote-table.md)
6.  Work with ETL extraction tables to scan the system of record regularly and extract data to a staging table. Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.

    \[Omitted image "erp-explore-2.png"\] Alt text: Zero copy connector for ERP extraction tables tab displaying a list of several extraction tables.

    -   Create as many separate extraction tables as needed, such as one for each supported country. For more information, see [Extracting and transforming data in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-extraction-tables.md).
    -   You must first create the table transform map that connects the source table \(on the system of record\) to a Glide table on the ServiceNow AI Platform. For more information on creating table transform maps, see [Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/system-import-sets/t_CreateATransformMap.md).
    -   Extraction processes are configured in the ServiceNow app that uses them, for example, Workflow Studio.
    -   After the extraction process is run, use import sets to map imported data into ServiceNow AI Platform tables. For more information, see [Import sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/system-import-sets/import-sets-landing-page.md).
7.  Build flows in Workflow Studio to specify details for when you query or update the ERP \(Enterprise Resource Planning\) system. For more information, see [Building flows to read or update the ERP system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-build-flow-operation.md).
8.  Move the ERP systems, ERP models, tables, operations, and flows to a production environment when they're ready. For more information, see [Managing ERP development pipelines in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/manage-erp-tables-pipelines.md).
9.  Use the ERP data as the data source when building apps on the ServiceNow AI Platform using:
    -   ServiceNow Studio: For more information, see  and .
    -   Flows in Workflow Studio: For more information, see .
    -   Playbooks in Workflow Studio: For more information, see .
    -   Table Builder: For more information, see .
    -   UI Builder: For more information, see .
    -   Workspace Builder: For more information, see .

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

[Working with ERP systems in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-work-with-systems.md)

</td><td>

sn\_erp\_integration.erp\_admin

</td></tr><tr><td>

Build ERP models to create read, update, and create operations and organize mirrored ERP data

</td><td>

[Building and managing models to work with ERP data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/work-with-erp-data-models.md)

</td><td>

sn\_erp\_integration.erp\_admin

</td></tr><tr><td>

Work with and query remote tables to view ERP data on the system of record

</td><td>

[Using ERP remote tables in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-work-with-remote-tables.md)

</td><td>

-   To modify remote tables: sn\_erp\_integration.erp\_admin
-   To read remote tables: sn\_erp\_integration.erp\_user

</td></tr><tr><td>

Access standard remote tables

</td><td>

[Standard remote tables for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erpi-standard-remote-tables.md)

</td><td>

-   sn\_erp\_integration.erp\_user
-   Additional, table-specific roles are required. For more information, see [Zero Copy Connector for ERP roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-roles.md).

</td></tr><tr><td>

Configure extraction tables to pull custom data from the ERP system regularly

</td><td>

[Extracting and transforming data in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-extraction-tables.md)

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

\[Omitted image "bus-whitepaper.svg"\] Alt text: [App Engine for ERP Overview on ServiceNow University](https://learning.servicenow.com/lxp/en/app-engine/enterprise-resource-planning-clean-core-with-app-engine-overview?id=learning_course_prev&course_id=ee84d77293bc35903cc0322d6cba10eb)

 **Note:** You must log in to ServiceNow University to access this resource.

</td></tr><tr><td>

\[Omitted image "bus-3-person.svg"\] Alt text: [ServiceNow Community site](https://www.servicenow.com/community/?id=community_search&q=erp%20canvas&spa=1)

</td></tr><tr><td>

\[Omitted image "bus-application-developer.svg"\] Alt text: [Video: Unlock the full potential of your ERP system](https://www.youtube.com/watch?v=R66HqYLfEc8)

</td></tr></tbody>
</table>-   **[Identifying ERP candidates to replatform with Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erpi-and-ecm-together.md)**  
Zero Copy Connector for ERP enables you to connect to your ERP \(Enterprise Resource Planning\) system of record, and to organize its data.
-   **[Zero Copy Connector for ERP custom field example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/ecm-example-case.md)**  
Zero Copy Connector for ERP helps you identify custom ERP \(Enterprise Resource Planning\) apps and fields in the system of record \(such as SAP\) to access their data on the ServiceNow AI Platform. The ERP system can have both standard and custom fields that are accessed by Zero Copy Connector for ERP.
-   **[Zero Copy Connector for ERP and security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-and-security.md)**  
In addition to role-based security and access control, Zero Copy Connector for ERP protects personally identifiable data in other ways.
-   **[Guided tours in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/guided-tours-in-erp-canvas.md)**  
Learn about Zero Copy Connector for ERP guided tours, including how to access and take them to build your knowledge of Zero Copy Connector for ERP.

**Parent Topic:**[Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-integration-overview.md)

