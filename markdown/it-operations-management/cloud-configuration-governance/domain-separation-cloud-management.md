---
title: Domain separation and Cloud Provisioning and Governance
description: Domain separation is supported in Cloud Provisioning and Governance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Domain separation and Cloud Provisioning and Governance

Domain separation is supported in Cloud Provisioning and Governance. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Cloud Provisioning and Governance domain separation overview

All tables in Cloud Provisioning and Governance are not domain separated. Delegated domain separation is not supported.

Domain separation for Cloud Provisioning and Governance supports:

-   **Service Providers \(SPs\) using the application to provide data separation.**

    In this scenario, SPs can provide data separation to multiple customers, where domains are necessary to contain all relevant customer data and processes. For example, an SP provides support to customers who typically use Cloud Provisioning and Governance to manage their IT infrastructure on the cloud. SPs can provide catalogs, template profiles, resource pools, and filter, resource profiles, quotas, permissions, IP address management \(IPAM\), lease and business hours scheduling, and a view to billing, as domain-separated offerings to their customers.


## How domain separation works in Cloud Provisioning and Governance

Domain separation for Cloud Provisioning and Governance aligns one or more companies to a domain. To use domain separation with the application, assign all user accounts to a specific company associated with that domain.

All entities that are related to the company, such as cloud accounts and service accounts, are created in the same domain as the company. When a new company is created, create a domain with a unique name and assign it to the company. All related entities for an account, such as contacts and cases, must reside in the same domain. When you create a related entity for a domain-separated account, the entity is assigned to the company domain.

Members of a domain can only view the data that is contained within their domain or child domains that are lower in the domain hierarchy. By default, all users and all records are members of the global domain unless you assign them to a particular domain. Once you assign a user or a record to a domain, the instance compares the user's domain to the record's domain to determine whether the user can view the record.

Service Providers \(SPs\) use domain separation to segregate data for each customer. Users in a given domain can only view the data in their own domains or in child domains. SPs typically control the top-level domain, which allows them to view data that is associated with all domains. Don't delegate administration to cloud admin users of the child domains in Cloud Provisioning and Governance.

## Set up domain separation for Cloud Provisioning and Governance

-   **Ensure that you activate the following plugins:**

    Domain Support - Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions.installer\) to enable domain separation in Cloud Provisioning and Governance

    Service Catalog - Domain Separation plugin \(glideapp.servicecatalog.domain\_separation\) to enable separation of catalog items in different domains in Cloud Provisioning and Governance


## Changes to Cloud Provisioning and Governance tables

Domain separation for Cloud Provisioning and Governance adds the **Domain** and **Domain Path** fields to the list views. These fields are not exposed by default. As a domain admin you can customize lists and forms to view these fields. Not all tables in Cloud Provisioning and Governance are domain separated. While some top-level tables are domain separated, several child tables are not domain separated. However, this does not impact how the Cloud Provisioning and Governance application works in a domain-separated context.

## Account domains and related entities

When you create related entities for an account, the domain for the related entities is set to the account domain.

## Domain visibility for cloud administrators and users

Manually assign users with the Cloud User Portal \(sn\_cmp.cloud\_service\_user\) roles and Cloud Admin Portal \(sn\_cmp.cmp\_root\_admin\) roles for each domain to the **TOP/MSP/Default/Company** or leaf domain. Domain administrators and users in Cloud Provisioning and Governance can only view data in the domain that they are created in, until they are assigned to the TOP domain. The Top domain represents a single common parent domain, which acts as a single parent node, for the Service Provider domains.

## Next Steps

For more information on creating, implementing, and maintaining domain separation for Cloud Provisioning and Governance services in the instance you are setting up for your customers, see [Domain separation in Cloud Provisioning and Governance - considerations for service providers](../reference/cloud-mgmt-dom-sep-recommend.md).

**Related topics**  


[Domain separation for service providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

