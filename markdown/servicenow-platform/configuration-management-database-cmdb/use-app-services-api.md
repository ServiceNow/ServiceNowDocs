---
title: Use application services APIs
description: Application services provide APIs that let you perform operations such as creating and updating an service instance, populating it with CIs from the CMDB, and retrieving details from an existing service instance.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Application services, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use application services APIs

Application services provide APIs that let you perform operations such as creating and updating an service instance, populating it with CIs from the CMDB, and retrieving details from an existing service instance.

Role required: app\_service\_admin

A service instance is a set of interconnected applications and hosts that are configured to offer a service to the organization. Service instances can be internal, like an organization email system or customer-facing, like an organization website.

## Create an application service

Using the [createOrUpdateService - POST](https://www.servicenow.com/docs/access?context=application-service-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) REST API to create an service instance suits your organization if the ServiceNow CMDB already contains the CIs making up the service. Typically, it is the case when you have manually added CIs directly into the CMDB, or used the Discovery application to discover CIs and store information about them in the CMDB. You can also use this API to create an service instance containing CIs discovered using non-ServiceNow applications.

By default, when an service instance is created, all CI connections are of the **Depends on::Used by** relationship type. You can modify this default type by changing the value of the [sa.it\_service.manual\_ci\_rel\_type](../reference/components-installed-app-services.md) property.

Before creating an application service, ensure that:

-   The CMDB contains all the CIs comprising the application service.
-   You have the sys\_id of each CI comprised in the application service you want to create.
-   You understand the hierarchy that the CIs form.

The Mapped Application Service \[cmdb\_ci\_service\_discovered\] table contains every service instance including services you create using APIs.

You can also manually create an service instance using the user interface as described in [Create an application service](../../service-mapping/task/create-it-services.md).

## Retrieve content from an application service

Use the [getContent - GET](https://www.servicenow.com/docs/access?context=application-service-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US) REST API to retrieve a list of CIs and the relationships between them, for an application service that was created manually.

## Additional APIs

The following JavaScript APIs are also available:

-   [addCI\(\)](https://www.servicenow.com/docs/access?context=BusinessServiceManagerAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Add a CI to a manually created an service instance.

    For restrictions on the CIs being added and other details about adding a CI to an service instance, see [Manually add CIs to an application service](../../service-mapping/task/manually-add-ci-to-business-service.md).

-   [addManualConnection\(\)](https://www.servicenow.com/docs/access?context=BusinessServiceManagerAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Add a manually created connection to an application service.

-   [migrateManualToApplicationService\(\)](https://www.servicenow.com/docs/access?context=BusinessServiceManagerAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Convert a manual service to an application service.

-   [populateApplicationService\(\)](https://www.servicenow.com/docs/access?context=BusinessServiceManagerAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Populate an application service with CIs and relationships from the designated entry point.

-   [removeCI\(\)](https://www.servicenow.com/docs/access?context=BusinessServiceManagerAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Remove a manually created CI from an application service.

-   [removeManualConnection\(\)](https://www.servicenow.com/docs/access?context=BusinessServiceManagerAPI&version=zurich&pubname=zurich-api-reference&ft:locale=en-US): Remove a manually created connection and the connected CI from an application service.


**Related topics**  


[Application Service API](https://www.servicenow.com/docs/access?context=application-service-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

