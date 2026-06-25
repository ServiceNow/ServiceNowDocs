---
title: Next steps after extracting data from your ERP system using ERP Data Hub
description: After you identify and extract ERP \(Enterprise Resource Planning\) data with ERP Data Hub, you can use that data on the ServiceNow AI Platform as the data source for products and apps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/erp-integration-framework/erpi-next-steps-replatforming.html
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Next steps after extracting data from your ERP system using ERP Data Hub

After you identify and extract ERP \(Enterprise Resource Planning\) data with ERP Data Hub, you can use that data on the ServiceNow AI Platform as the data source for products and apps.

## Use retrieved ERP data in flows

Build flows in Workflow Studio to specify details for when you query or update the ERP \(Enterprise Resource Planning\) system.

For example, you can generate a record for each response from the ERP system, making that data available for use on the ServiceNow AI Platform. For more information, see [Building flows to read or update the ERP system](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/erp-canvas-build-flow-operation.md).

## Build a ServiceNow app that consumes ERP data

ERP data from the system of record is available in the remote tables and ERP extraction tables that you configure in ERP Data Hub. You can also use table transform maps to put extracted ERP data into a Glide table.

After ERP data is available on tables in the ServiceNow AI Platform, you can use those tables as the foundation for app builders. For example, you can use ERP tables as a data source when you add data in App Engine Studio. For more information, see [Create a data model for your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/add-data.md).

## ServiceNow low- and pro-code builders

Use any of the following ServiceNow builders to create apps using custom data:

-   [App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/aes-overview.md)
-   [Flows in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/build-workflows/workflow-studio/exploring-flows.md)
-   [Playbooks in Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/build-workflows/workflow-studio/exploring-process-automation-designer.md)
-   [Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/form-builder-glide-family-release/tb-landing-page.md)
-   [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/ui-builder/ui-builder-overview.md)
-   [Workspace Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/workspace-builder/add-workspace.md)

## Using Glide to query ERP data

You can also access data from the system of record through the Glide API.

For more information, see [Sample Glide query for ERP data in ERP Data Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/erp-canvas-sample-glide-query-code.md).

**Parent Topic:**[Using ERP models, extraction tables, and remote tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/work-with-erp-systems-connections-and-remote-tables.md)

