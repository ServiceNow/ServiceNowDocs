---
title: Connect to other ERP using REST
description: Extract data securely from an ERP with REST for use in remote tables and extraction tables.
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

# Connect to other ERP using REST

Extract data securely from an ERP with REST for use in remote tables and extraction tables.

## Configure REST access

Access business data from an ERP using REST APIs. For more information, see [REST API connector for Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-rest-api-connector.md) and [Add a REST service manually in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-add-a-rest-service-manually.md).

For API details, see .

## Providing REST access to users

You must have an ERP system that has been enabled to make a REST connection. REST connections use the HTTP connection template. For more information, see [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/create-https-connection.md).

## Enabling download of XML files

The glide.attachment.extensions system property restricts the file types that can be downloaded. This property is empty by default. Check that the xml file extension hasn't been added to this property. For more information, see .

## Heartbeat information

For an ERP system, there are separate heartbeat indicators for RFC and HTTP. When a system is established, the heartbeats are set to active and the status is updated, including any errors. REST uses HTTP.

## Supported Workday APIs

Most Workday APIs are supported. For more information about services, see the [Workday REST Services Directory](https://community.workday.com/sites/default/files/file-hosting/restapi/) in the Workday Community.

For steps to add a REST entity to a model operation, see [Obtain data from Workday using REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/obtain-data-from-workday-using-rest-api.md) and [Add a REST entity to a model operation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-a-rest-entity-to-a-model-operation.md).

