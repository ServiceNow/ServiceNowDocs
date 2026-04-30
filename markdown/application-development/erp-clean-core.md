---
title: App Engine for ERP with the ServiceNow AI Platform
description: Read and update your legacy ERP \(Enterprise Resource Planning\) system using ERP Data Hub and identify customizations with ERP Customization Mining \(ERP-CM\). You can then use additional ServiceNow AI Platform apps, such as App Engine Studio \(AES\), to organize and replatform ERP data.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Building low-code applications, Developing your application, Building applications]
---

# App Engine for ERP with the ServiceNow AI Platform

Read and update your legacy ERP \(Enterprise Resource Planning\) system using ERP Data Hub and identify customizations with ERP Customization Mining \(ERP-CM\). You can then use additional ServiceNow AI Platform apps, such as App Engine Studio \(AES\), to organize and replatform ERP data.

Replatforming is the process of scanning legacy ERP system code to find potential candidates to move onto your ServiceNow AI Platform instance as new apps. You can use data from the ERP system as a source for apps built on the ServiceNow AI Platform, improving performance, enhancing security, and reducing maintenance.

## Combined benefits of integrating ERP Data Hub and ERP-CM to replatform apps

Legacy systems of records, such as SAP, can have old, complex custom code and data that require more time and effort to move to newer versions of the system of record. Use ERP Data Hub and ERP Customization Mining \(ERP-CM\) to scan the system of record to find and replace custom code with digitized workflows, resulting in a clean ERP core.

![ERP Customization Mining diagnoses your ERP system to identify customizations and recommend next steps in replatforming the apps to the ServiceNow AI Platform.](../../build/erp-customization-mining/image/erpcm-landing-page-infographic.png "ERP Customization Mining and App Engine for ERP")

The replatforming of legacy code enables innovation on top of the system of record without knowledge of the legacy system. Database administrators and developers are then relieved of time-consuming efforts to create database views or endpoints in the system of record, freeing them to work on other projects, such as migration.

Replatformed data is immediately available, mirrored in easy-to-manage tables and apps. Users no longer need to request information from database administrators, which can take weeks. Replatformed apps use the ERP system of record as the live data source.

## Workflow for ERP Data Hub and ERP-CM

Using ERP Data Hub and ERP-CM together enables Solutions Integration consultants to implement the following workflow:

1.  Have your administrator use the Connections and Credentials app to configure credentials to connect ERP Data Hub to the ERP system of record. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).
2.  Create an ERP system in ERP Data Hub using the connection and credentials alias that you configured. For more information, see [Create an ERP system in ERP Data Hub](../../build/erp-integration/task/create-an-erp-system.md).
3.  In ERP Data Hub, build your ERP systems, ERP models, and tables in a development instance.
    1.  Create or clone an ERP model that scans the specified ERP module in the system of record for available tables and fields. Note the tables and fields in the ERP model for use in extraction and remote tables. For more information, see [Clone an ERP model in ERP Data Hub](../../build/erp-integration/task/erp-canvas-clone-data-model.md).
    2.  Add new tables, fields, and table joins to include additional data in the ERP model. For more information, see the following topics:
        -   [Managing how models read and update the ERP system](../../build/erp-integration/concept/erpc-managing-models-read.md)
        -   [Add joins between ERP tables](../../build/erp-integration/task/erp-canvas-add-join-data-model.md)
    3.  Create update operation using a BAPI \(Business Application Programming Interface\) to update data on the ERP system as needed.
    4.  Build and customize remote tables to make them available for use as a data source, such as when building apps. Remote tables get their records from running an associated script against an external data source. For more information, see:
        -   [View and edit ERP remote table details with ERP Data Hub](../../build/erp-integration/task/erpi-find-tables.md)
        -   [Customize fields for an ERP remote table in ERP Data Hub](../../build/erp-integration/task/erp-canvas-build-remote-table.md)
        -   [Query a remote table using ERP Data Hub](../../build/erp-integration/task/erp-canvas-query-remote-table.md)
    5.  Work with ETL extraction tables to regularly scan the system of record and extract data to a staging table. Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.
        -   Create as many separate extraction tables as needed, such as one for each supported country. For more information, see [Extracting and transforming data in ERP Data Hub](../../build/erp-integration/concept/erp-canvas-extraction-tables.md).
        -   You must first create the table transform map that connects the source table \(on the system of record\) to a Glide table on the ServiceNow AI Platform. For more information on creating table transform maps, see [Create a transform map](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).
        -   Extraction processes are configured in the ServiceNow app that uses them. For example, Workflow Studio.
        -   After the extraction process is run, use import sets to map imported data into ServiceNow AI Platform tables. For more information, see [Import sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).
4.  Identify legacy ERP system customizations to modernize and replatform with ERP-CM.
5.  Move the ERP Data Hub systems, ERP models, and tables to a production environment when they are ready. For more information, see [Managing ERP development pipelines in ERP Data Hub](../../build/erp-integration/concept/manage-erp-tables-pipelines.md).
    1.  Meet with a customer and agree to run an analysis with ERP Customization Mining on their ERP system of record.
    2.  Connect the customer ERP system of record to the ServiceNow instance using ERP Data Hub.

        **Note:** Most customers have their own instance.

        ERP-CM uses the system connections configured in ERP Data Hub. For more information, see [Working with ERP systems in ERP Data Hub](../../build/erp-integration/concept/erp-canvas-work-with-systems.md).

    3.  Use ERP Data Hub to build ERP models from fields on the available remote tables as specified in previous workflow steps.
    4.  Run ERP Customization Mining to find candidates. Candidates are custom code in the system of record that you can replace with ServiceNow apps. For more information, see [Browse an overview of candidates in ERP-CM](../../build/erp-customization-mining/task/erpcm-view-home-page-overview.md).
    5.  Choose candidates to replatform. For more information, see [Save potential candidates to replatform](../../build/erp-customization-mining/task/erpcm-find-candidates.md).
    6.  Use the candidate details in ERP-CM as a central place to enter comments and save attachments relating to the candidate. For more information, see [View and work with candidate details in ERP-CM](../../build/erp-customization-mining/task/erpcm-view-work-with-candidate-details.md).
    7.  In the candidate details, identify any similar candidates that you could combine into a single replatformed app. For more information, see [How ERP Customization Mining determines candidate score and potential](../../build/erp-customization-mining/concept/erpcm-potential-and-recommendations.md).
    8.  Return to ERP Data Hub to continue building data models with remote tables and extraction tables. Ensure that all the necessary data is available in the ServiceNow AI Platform. For more information, see [Building and managing ERP models to work with ERP data](../../build/erp-integration/concept/work-with-erp-data-models.md).
6.  Use the ERP data that is now available as the data source when building apps on the ServiceNow AI Platform, such as:
    -   App Engine Studio: For more information, see [Create a data model for your application](../../build/app-engine-studio/concept/add-data.md).
    -   Flows in Workflow Studio: For more information, see [Configuring flows](https://www.servicenow.com/docs/access?context=configuring-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
    -   Table Builder: For more information, see [Data in Table Builder](../../administer/form-builder/concept/table-builder.md).
    -   UI Builder: For more information, see [Dynamically expose data in UI Builder pages \(advanced feature\)](../../administer/ui-builder/concept/data-resources.md).
    -   Workflow Studio: For more information, see [Configuring flows](https://www.servicenow.com/docs/access?context=configuring-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).
    -   Workspace Builder: For more information, see [Configure a record page for a workspace in Workspace Builder](../../build/app-engine-studio/task/configure-record-page-workspace.md).
7.  Measure and monitor the performance of the new app using applicable metrics and parameters with your preferred analytic tools.

## Requirements for integrating ERP Data Hub and ERP-CM

1.  Requirements for installing ERP Data Hub include the following:

    -   A valid license
    -   ServiceNow AI Platform plugins
    -   MID server configuration
    -   Spoke integration
    -   SAP configuration
    For more information, see [Requirements for installing ERP Data Hub](../../build/erp-integration/reference/erpc-prereqs-for-installation.md).

2.  Requirements for installing ERP-CM include the following:
    -   License and entitlement. For more information, see [Install ERP Data Hub](../../build/erp-integration/task/install-erp-integration.md).
    -   ServiceNow AI Platform plugins. For more information, see [Install ERP Data Hub](../../build/erp-integration/task/install-erp-integration.md).
    -   SAP configuration. For more information, see [Configure SAP for ERP-CM](../../build/erp-customization-mining/task/ecm-configure-sap-system.md).

## Get started with ERP Data Hub and ERP-CM

Get started with ERP Data Hub and ERP-CM by completing these tasks:

1.  Install and configure ERP Data Hub. For more information, see [Configuring ERP Data Hub](../../build/erp-integration/concept/erp-integration-configuration-overview.md).
2.  Install and configure ERP-CM. For more information, see [Configuring ERP Customization Mining](../../build/erp-customization-mining/concept/configuring-ecm.md).
3.  Install and configure any additional ServiceNow AI Platform apps and builders that consume ERP data, such as the following:
    -   [Installing App Engine Studio](../../build/app-engine-studio/task/install-aes.md)
    -   [Configuring Flows in Workflow Studio](https://www.servicenow.com/docs/access?context=configuring-flow-designer&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)
    -   [Exploring Table Builder](../../administer/form-builder/concept/exploring-fb.md)
    -   [Getting started with Playbooks](https://www.servicenow.com/docs/access?context=getting-started-process-automation&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)
    -   [UI Builder quick start](../../administer/ui-builder/task/ui-builder-quick-start.md)
    -   [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)
    -   [Workspace Builder](../../build/app-engine-studio/concept/using-workspace-builder.md)

