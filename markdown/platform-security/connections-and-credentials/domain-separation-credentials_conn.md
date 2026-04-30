---
title: Domain separation and Credentials and Connections
description: Domain separation is supported in Credentials and Connections. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: yokohama
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Exploring credentials, connections, and aliases, Connections and Credentials, Access Management]
---

# Domain separation and Credentials and Connections

Domain separation is supported in Credentials and Connections. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](../../../administer/company-and-domain-separation/reference/domain-separated-apps.md).

## Overview

Credentials are tied to various ServiceNow features which access systems outside the instance. Credentials follow the domain separation tied to the feature employing the credentials.

Connections are protocol-specific information referencing a target host outside the instance. A connection can specify the domain to run an activity.

## How domain separation works in Credentials and Connections

Credentials access resources outside of the instance, and are used by the [Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), [Orchestration](https://www.servicenow.com/docs/access?context=r-orchestration&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US), [Service Mapping](https://www.servicenow.com/docs/access?context=c_ServiceMappingOverview&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), and [Cloud Provisioning and Governance](https://www.servicenow.com/docs/access?context=cloud-management-v2-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) applications. These credentials are not tied to a specific domain, rather, they can be bound to an application and then follow the domain separation that the application uses. Credentials can also be assigned to a [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US), and then follow the domain separation specified by the MID Server configuration.

Connections access a target host using a JMS, JDBC, or HTTP\(s\) connection. You can specify global or a specific domain to which the connection belongs.

**Parent Topic:**[Exploring credentials, connections, and aliases](credentials-connections-alias.md)

**Related topics**  


[Domain separation for service providers](../../../administer/company-and-domain-separation/reference/domain-sep-landing-page.md)

