---
title: Manage data
description: With the data model \(tables and fields\) created and security set up, add data into the application’s table\(s\).
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Define and build the data model, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Manage data

With the data model \(tables and fields\) created and security set up, add data into the application’s table\(s\).

## Import sets

To populate tables in ServiceNow from an external platform, use import sets and transform maps. To retrieve data from an external source on a regular basis, use a scheduled import.

Self-Paced Training: [Importing Data into ServiceNow](https://developer.servicenow.com/dev.do#!/learn/courses/rome/app_store_learnv2_importingdata_rome_importing_data_into_servicenow)

Guidelines for Import Set Performance:

-   Break up large amounts of data into smaller sets for faster imports. Consider 100,000 rows to be a baseline and break up anything larger than that into sets of 100,000. For example, importing 10 sets of 100,000 will finish quicker than one set of 1,000,000 records. Also consider using [Concurrent Imports](https://servicenow.com/docs/bundle/rome-platform-administration/page/administer/import-sets/concept/concurrent-imports.html) with larger numbers of records.
-   Importing large data sets simultaneously can put load on an instance. Stagger large imports so the imports do not overlap.
-   If possible, deselect the Run business rules check box on the transform map table to avoid running Business Rules and other logic during an import. Consider using an onComplete transform script to run business logic, such as calculations, at the end of an import rather than on each record as Business Rules do.
-   Use default functionality for imports. Whenever possible, avoid writing custom scripts. For example, use the coalesce functionality rather than writing a custom coalesce script.
-   Avoid GlideRecord queries in an import set.
-   Make sure any fields configured to coalesce are indexed.
-   If replacing a system with a requirement to import historical data, import only the historical data required for the application. Consider storing historical data in a [data lake](https://en.wikipedia.org/wiki/Data_lake).

## Inbound integrations

In addition to Import Sets, ServiceNow includes APIs to accept data from external platforms.

To push data directly into an application table from another system, use Web Service Import Sets instead of writing directly to application tables using the REST Table API or SOAP APIs.

To handle data transactions that are more complex than writing data to a table, such as sending an attachment or ordering a catalog item, review the available [APIs](https://developer.servicenow.com/dev.do#!/reference/api/rome/rest/c_TableAPI) to see if one exists that supports the required logic.

Use a [Scripted REST API](https://servicenow.com/docs/bundle/rome-application-development/page/integrate/custom-web-services/concept/c_CustomWebServices.html) or [Scripted SOAP Web Service](https://servicenow.com/docs/bundle/rome-application-development/page/integrate/inbound-soap/concept/c_ScriptedWebServices.html) to build REST or SOAP endpoints, respectively. Scripted REST API and Scripted SOAP Web Service endpoints can execute ServiceNow server-side code when the endpoint is consumed by an external system.

Self-Paced Training: [REST Integrations](https://developer.servicenow.com/dev.do#!/learn/courses/rome/app_store_learnv2_rest_rome_rest_integrations)

**Parent Topic:**[Define and build the data model](define-and-build-data-model.md)

