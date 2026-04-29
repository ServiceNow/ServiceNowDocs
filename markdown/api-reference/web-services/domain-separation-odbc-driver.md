---
title: Domain separation and ODBC driver
description: This is an overview of domain separation and ODBC drivers.Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create data sources from other apps using ODBC driver, Additional integration resources, Web services, API implementation, API implementation and reference]
---

# Domain separation and ODBC driver

This is an overview of domain separation and ODBC drivers.Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic\*

-   There is business logic to ensure data goes into the proper domain for the application’s service provider use cases.
-   In the application, the user interface, cache keys, reporting, rollups, aggregations, and so on, all consider domain at run time.
-   The owner of the instance needs to be able to set up the application to function normally across multiple tenants.

Use case: As a service provider when I use chat to respond to a tenant-customer’s message, the client must be able to see my response.

**Parent Topic:**[Create data sources from other apps using ODBC driver](c_ODBCDriver.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

