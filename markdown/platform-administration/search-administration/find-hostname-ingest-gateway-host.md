---
title: Find the hostname for your ingest gateway host
description: Look up the hostname for the ingest gateway host associated with your ServiceNow AI Platform instance. Your custom connector needs this hostname to send its Custom Connector Gateway API requests to the proper host.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/search-administration/find-hostname-ingest-gateway-host.html
release: australia
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-09-28"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Custom Connector Gateway external content connector, Configure, External Content Connectors, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Find the hostname for your ingest gateway host

Look up the hostname for the ingest gateway host associated with your ServiceNow AI Platform® instance. Your custom connector needs this hostname to send its Custom Connector Gateway API requests to the proper host.

## Before you begin

Role required: admin

## About this task

The custom connector needs to submit add and delete requests to the `xcc-ingest` endpoint provided by the Custom Connector Gateway API. This endpoint is accessible on the ingest gateway host associated with your ServiceNow AI Platform instance. The connector needs the hostname for the ingest gateway host so it can send its requests to the proper endpoint.

The hostname for an instance's ingest gateway host is stored as the value of the **sn\_itom\_cloud\_svc.itomgateway\_url** system property on that instance. Perform the following steps to find this hostname.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the navigation field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Edit the system property record with name **sn\_itom\_cloud\_svc.itomgateway\_url**.

3.  Copy the hostname specified in the record's **Value** field and store it in a secure location.

    This is the hostname for the ingest gateway host associated with your ServiceNow AI Platform instance.


## What to do next

Provide the copied hostname to the development team responsible for implementing your custom connector. For details on how they need to incorporate this hostname into the functionality of the custom connector, see [Implementing a custom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/implementing-custom-connector.md).

**Parent Topic:**[Custom Connector Gateway external content connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/search-administration/custom-connector-gateway-external-content-connector.md)

