---
title: Domain separation in Privacy Management
description: This is an overview of domain separation and the Governance, Risk, and Compliance application Privacy Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Privacy Management, Governance, Risk, and Compliance]
---

# Domain separation in Privacy Management

This is an overview of domain separation and the Governance, Risk, and Compliance application Privacy Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Overview of domain separation

Domain separation is best for those customers who:

-   Need to enforce absolute data segregation between business entities \(data separation\).
-   Customize business process definitions and user interfaces for each domain \(delegated administration\).
-   Maintain some global processes and global reporting in a single instance.

These users can choose to expand or collapse the domain scope to show or hide data from other domains.

**Note:** Users always have access to data from domains that have been explicitly granted to them by domain visibility.

## How domain separation works in GRC

-   While GRC supports separation of data, separation of logic and process is not fully supported.
-   Many types of records in GRC are automatically generated through user processes. Entities, controls, risks, indicators, control tests, and processing activities are all fields that can be generated automatically. For records that are automatically generated \(and for any GRC record that is manually generated\), the domain of the record is the same as the domain of the user responsible for creating or generating the records.

    Automatic generation should be kept in mind when working in a domain-separated GRC implementation. Users should be sure that they are creating or generating records at the right domain level so that they are visible to the right set of users.

    For example, suppose you have a domain hierarchy that has Global at the top level followed by Top domain. Top domain, in turn, has two sub domains: Domain A and domain B.


-   If you have an entity that you want to send a privacy assessment that must assessed by users in domains A and B, the entity should be generated or manually created at the global level. If the entity is created in Domain B, you will not be able to recreate the entity in Domain A due to indexing.
-   If you have an entity that you want to be assessed by users in Top and Domain A, you can create the entity in Domain A.

Unless the entities are in the Global domain, users should not assign entities in a higher domain to users in a lower domain. In the example above, if you have an entity in the TOP domain, you should not assign it for privacy assessment to users in Domains A or B since those users would not have access to the assessment; thus the assessment questionnaire would not be generated.

Similarly, users should not assign control objectives and risk statements in a higher domain to attestations and assessments in a lower domain. Otherwise the attestation or assessment questionnaire would not be generated.

## Use case

GRC data for IT can be separated from the GRC data of other departments. Each business area using the GRC application can have separate data that cannot be shared with other departments. Therefore each department can have its own entities, policies, controls, risks, and so on.

When looking at a control from the IT domain, the user can choose to expand the domain scope to show values from the Finance domain or collapse the domain scope to show only controls that match the IT domain.

By default, domain separation adds a domain field to the Task `[task]`and Configuration Items `[cmdb_ci]` tables and their extensions.

You can extend domain separation to any new tables you create by adding a `sys_domain` field to the table's dictionary definition. By default, the system only domain-separates platform and baseline application tables where appropriate.

**Warning:** ServiceNow does not recommend domain separating platform tables \(any table with the sys\_ prefix such as the Dictionary Entry `[sys_dictionary]`and Dictionary Entry Override `[sys_dictionary_override]` tables\) because it can produce unexpected results.

In this use case, client scripts, business rules, workflows, processes, and so on can be domain-separated.

While the behavior offered with domain separation provides multi-tenancy support, multi-tenancy is still contained within a single instance. This means that some global properties, some global data, and some global processes are shared across all domains. For example, the system’s “Remember me” option on the login page is global and cannot be specified per domain.

If you need complete and total separation of all system properties and do not require global reporting or global processes, separate instances are the best option.

**Parent Topic:**[Privacy Management reference](../reference/privacy-mgmt-reference.md)

