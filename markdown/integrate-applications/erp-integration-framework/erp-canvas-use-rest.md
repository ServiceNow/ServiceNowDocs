---
title: Connect Zero Copy Connector for ERP to SAP using REST
description: Extract data securely from ERP with REST for use in remote tables and extraction tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-use-rest.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-06-16"
reading_time_minutes: 1
breadcrumb: [Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Connect Zero Copy Connector for ERP to SAP using REST

Extract data securely from ERP with REST for use in remote tables and extraction tables.

## Providing REST access to users

You must have an SAP system that has been enabled to make a REST connection. REST connections use the HTTP connection template. For more information, see .

## Enabling download of XML files

The glide.attachment.extensions system property restricts the file types that can be downloaded. This property is empty by default. Check that the xml file extension hasn't been added to this property. For more information, see .

## Heartbeat information

For an ERP system, there are separate heartbeat indicators for RFC and HTTP. When a system is established, the heartbeats are set to active and the status is updated, including any errors. REST uses HTTP.

## Supported Workday APIs

Most Workday APIs are supported. For more information about services, see the [Workday REST Services Directory](https://community.workday.com/sites/default/files/file-hosting/restapi/) in the Workday Community.

**Note:** WQL is not supported, but can be configured using Zero Copy Trino. For a similar example, see [Create a ServiceNow Remote Instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-servicenow-remote-instance-connection.md).

## More information

For more information about using REST in Zero Copy Connector for ERP, see

-   [REST API connector for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-rest-api-connector.md)
-   [Obtain data from Workday using REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/obtain-data-from-workday-using-rest-api.md)
-   [Add a REST service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-rest-service-manually.md)
-   [Add a REST entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-a-rest-entity-to-a-model-operation.md)

**Parent Topic:**[Configuring Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-integration-configuration-overview.md)

