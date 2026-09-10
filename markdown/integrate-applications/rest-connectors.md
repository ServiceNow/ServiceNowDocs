---
title: REST connectors
description: REST connectors use APIs, instead of JDBC, to retrieve data and metadata from an external source.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/rest-connectors.html
release: australia
topic_type: concept
last_updated: "2026-08-24"
reading_time_minutes: 1
breadcrumb: [Explore, Zero Copy Connectors, Workflow Data Fabric]
---

# REST connectors

REST connectors use APIs, instead of JDBC, to retrieve data and metadata from an external source.

Most connectors in the Zero Copy Connector Hub use JDBC to connect directly to a database. REST connectors work differently by retrieving data and metadata through API calls to the external source. A connector that uses this method is identified by a **REST** tag next to its name in the connector list, the connection page, and the Connection Guide panel.

## Before you begin

REST connectors aren't available in the connector list by default. To make them available, install Data Fabric REST Connectors, which is included with your Zero Copy Connector Hub WDF Foundation subscription. After you install this app, the REST connectors appear in the connector list, tagged as **REST**.

## API rate limits and consumption

REST connectors retrieve data by calling the external source's API. Running queries against a REST connector consumes API calls against that source system's rate limits and any associated usage costs. For example, if you connect to a Jira instance that has API rate limiting in place, queries you run through the REST connector count against that limit.

**Note:** Large or frequent queries can consume a significant portion of your source system's API allowance.

## Authentication

Unlike JDBC-based connectors, REST connectors don't expose separate authentication-type options \(such as basic authentication or OAuth\) on the connection form itself. Authentication is instead configured on the HTTP connection that the **Connection Alias** field references, using the Connections &amp; Credentials \(CnC\) framework.

The **Connection Alias** can reference an HTTP connection configured with any of the following credential types:

-   Basic authentication
-   Auth token
-   OAuth

**Related topics**  


[jira-zcc]

[Acumatica](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/acumatica-zcc.md)

