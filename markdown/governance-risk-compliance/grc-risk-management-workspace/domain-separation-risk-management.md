---
title: Domain separation in Risk Management
description: Domain separation is supported for Risk Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Reference, Risk Management, Governance, Risk, and Compliance]
---

# Domain separation in Risk Management

Domain separation is supported for Risk Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Overview of domain separation

Domain separation is best for those customers who:

-   Need to enforce absolute data segregation between business entities \(data separation\).
-   Customize business process definitions and user interfaces for each domain \(delegated administration\).
-   Maintain some global processes and global reporting in a single instance.

These users can choose to expand or collapse the domain scope to show or hide data from other domains.

**Note:** Users always have access to data from domains that have been explicitly granted to them by domain visibility.

## How domain separation works in GRC

-   While GRC supports separation of data, separation of logic and process is not fully supported.
-   Many types of records in GRC are automatically generated through user processes. Entities, controls, risks, indicators, and control tests are all fields that can be generated automatically. For records that are automatically generated, the domain of the record is determined by the domain iterator configured for the job. Otherwise, it defaults to the default domain \(if defined\) or to the Global domain. For records that are manually generated, the domain is derived from the domain of the user creating the record.

    Automatic generation should be kept in mind when working in a domain-separated GRC implementation. Users should be sure that they are creating / generating records at the right domain level so that they are visible to the right set of users.

    For example, suppose you have domains that look like:

    -   Global
    -   TOP
        -   Domain A
        -   Domain B

-   If you have a risk or control that you want to be assessed by users in domains A and B, the risk or control should be generated or manually created at the global level. If the risk or control is created in Domain B, you will not be able to recreate the risk or control in Domain A due to indexing.
-   If you have a risk or control that you want to be assessed by users in TOP and Domain A, you can create the risk or control in Domain A.

Unless the risks and controls are in the Global domain, users should not assign risks or controls in a higher domain to users in a lower domain. In the example above, if you have a control in the TOP domain, you should not assign it for attestation to users in Domains A or B since those users would not have access to the control; thus the attestation or assessment questionnaire would not be generated.

Similarly, users should not assign control objectives and risk statements in a higher domain to attestations and assessments in a lower domain. Otherwise the attestation or assessment questionnaire would not be generated.

## Use case

GRC data for IT can be separated from the GRC data of other departments. Each business area using the GRC application can have separate data that cannot be shared with other departments. Therefore each department can have its own entities, policies, controls, risks, and so on.

When looking at a control from the IT domain, the user can choose to expand the domain scope to show values from the Finance domain or collapse the domain scope to show only controls that match the IT domain.

By default, domain separation adds a domain field to the Task `[task]`and Configuration Items `[cmdb_ci]` tables and their extensions.

You can extend domain separation to any new tables you create by adding `sys_domain` and `sys_domain_path` fields to the table's dictionary definition. By default, the system only domain-separates platform and baseline application tables where appropriate.

**Warning:** ServiceNow does not recommend domain separating platform tables \(any table with the sys\_ prefix such as the Dictionary Entry `[sys_dictionary]`and Dictionary Entry Override `[sys_dictionary_override]` tables\) because it can produce unexpected results.

In this use case, client scripts, business rules, workflows, processes, and so on can be domain-separated.

While the behavior offered with domain separation provides multi-tenancy support, multi-tenancy is still contained within a single instance. This means that some global properties, some global data, and some global processes are shared across all domains. For example, the system’s “Remember me” option on the login page is global and cannot be specified per domain.

If you need complete and total separation of all system properties and do not require global reporting or global processes, separate instances are the best option.

## How domain values are allocated to GRC objects

Records that are automatically generated, the domain of the record is determined by the domain iterator configured for the job. The following table shows how domain values are allocated to different GRC objects:

|GRC objects|Domain source|
|-----------|-------------|
|Risk|Gets domain value from Entity.|
|Risk assessment|Gets domain value from Risk.|
|Object assessment|Gets domain value from Object.|
|Risk assessment response|Gets domain value from Risk Assessment instance.|
|Risk identification|Gets domain value from Entity.|
|Aggregated risk|Gets domain value from Entity and Risk statement.|
|Basel reports|Gets domain value from Risk events.|
|Risk to control|Gets domain value from Risk.|

**Note:** When the domain source is global or nil, then that object's domain will be set to Default.

**Parent Topic:**[Risk Management reference](../reference/risk-management-reference.md)

