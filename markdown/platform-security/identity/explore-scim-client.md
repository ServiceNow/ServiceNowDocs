---
title: Exploring SCIM Client
description: The SCIM Client facilitates provisioning and updates on identity resources through CRUD operations exposed by SCIM endpoint on an external system.
locale: en-US
release: yokohama
product: Identity
classification: identity
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [SCIM Client, System for Cross-domain Identity Management \(SCIM\), Identity]
---

# Exploring SCIM Client

The SCIM Client facilitates provisioning and updates on identity resources through CRUD operations exposed by SCIM endpoint on an external system.

The SCIM Client is used for creating, updating, and deleting identity resources in a system that supports SCIM compliant REST requests. The client is used for identity life-cycle management and for identity attribute synchronization across ServiceNow instances or between ServiceNow and other SCIM providers.​

Because the APIs are exposed by the client, you can automate the process of creating, updating, or deleting any resources on a single or multiple SCIM providers. For example, if a developer joins the organization, you have to provide access to Git, workplace, and so on.

The SCIM client enables you to perform the following actions:

-   Provision identities and access for user or group membership.
-   Synchronize identity and related resources with SCIM compliant systems.​
-   Integrate any SCIM Provider on ServiceNow®.
-   De-provision identities and access.

The SCIM client provides scriptable APIs that the integration developer can use to build workflows or automations to do specified jobs. To know more about the scriptable API, see [SCIM2Client API](https://www.servicenow.com/docs/access?context=SCIM2ClientAPI&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

![SCIM Client](../images/scim-client-app-working.png)

## Configurations for SCIM Client

To configure the SCIM Client, perform the following tasks:

-   Create a REST message for all outbound calls for a particular SCIM Provider. For more information, see [Create a REST message](../task/create-a-rest-message.md).
-   Create a SCIM Provider to fetch resource types and schemas information from the SCIM Provider with the REST message. Enable the configuration of the HTTP Method \(PUT or PATCH\) to update a resource in the SCIM Provider. For more information, see [Create a SCIM Provider](../task/create-scim-provider.md).
-   Create the mappings of SCIM attributes to ServiceNow attributes for a particular resource type and SCIM Provider. To know more, see [Create a SCIM Provider Resource Mapping](../task/scim-provider-resource-mapping.md).
-   Perform the mapping of SCIM field with the database table and field name. Pass the default value or write a script to fetch the value. For more information know, see [Create a SCIM attribute mapping](../task/create-scim-attribute-mappings.md).

