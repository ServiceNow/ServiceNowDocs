---
title: Get the sys\_id for a Custom Connector Gateway external content connector
description: Retrieve the sys\_id for a Custom Connector Gateway external content connector. This sys\_id value is required when creating or retrieving a Java Web Token \(JWT\) using the Custom Connector Gateway API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/get-sys-id-custom-connector-gateway-external-content-connector.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Custom Connector Gateway external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Get the sys\_id for a Custom Connector Gateway external content connector

Retrieve the sys\_id for a Custom Connector Gateway external content connector. This sys\_id value is required when creating or retrieving a Java Web Token \(JWT\) using the Custom Connector Gateway API.

## Before you begin

Role required: admin

## About this task

To create or retrieve a JWT \(Java Web Token\) using the Custom Connector Gateway API, you must specify the sys\_id of a Custom Connector Gateway external content connector. All requests you submit to the API endpoint with a JWT are scoped to the connector specified in the creation request for that JWT.

Follow this procedure to obtain the sys\_id for a Custom Connector Gateway external content connector.

## Procedure

1.  Navigate to the Custom Connector Configurations \[sn\_ext\_conn\_ccg\_configuration\] table's list view.

    1.  Select **All**.

    2.  In the navigation field, enter `sn_ext_conn_ccg_configuration.list`.

    3.  Press Enter.

2.  Open the record for your chosen Custom Connector Gateway external content connector by selecting it.

3.  On the Custom Connector Configuration form, open the Additional actions menu \[Omitted image "polaris-ui-form-context-menu-icon.png"\] Alt text:.

4.  Select **Copy sys\_id**, then record the copied sys\_id value in a secure location.


## What to do next

Use the copied connector sys\_id in your JWT creation or retrieval requests to the Custom Connector Gateway API. For details on JWT requests, see [Implementing a custom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/implementing-custom-connector.md).

**Parent Topic:**[Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/custom-connector-gateway-external-content-connector.md)

