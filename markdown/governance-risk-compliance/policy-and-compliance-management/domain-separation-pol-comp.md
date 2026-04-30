---
title: Domain separation in GRC: Policy and Compliance Management
description: Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Reference, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Domain separation in GRC: Policy and Compliance Management

Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Benefits of having domain-separated tables in Policy and Compliance Management

Domain separation is best for those customers who:

-   Need to enforce absolute data segregation between business entities \(data separation\).
-   Customize business process definitions and user interfaces for each domain \(delegated administration\).
-   Maintain some global processes and global reporting in a single instance.

These users can choose to expand or collapse the domain scope to show or hide data from other domains.

**Note:** Users always have access to data from domains that have been explicitly granted to them by domain visibility.

## How GRC handles domain separation

While GRC supports separation of data, separation of logic and process is not fully supported.

-   Many types of records in GRC are automatically generated through user processes. Entities, controls, risks, indicators, and control tests are all records that can be generated automatically. For records that are automatically generated \(and for any GRC record that is manually generated\), the domain of the record is the same as the domain of the user responsible for creating or generating the records.
-   Automatic generation should be kept in mind when working in a domain-separated GRC implementation. Users should be sure that they are creating / generating records at the right domain level so that they are visible to the right set of users.

    For example, suppose you have domains that look like:


![Domain separation in GRC.](../image/domain-separation-pc.png "Domain separation")

-   If you have a risk or control that you want to be assessed by users in domains A and B, the risk or control should be generated or manually created at the global level. If the risk or control is created in Domain B, you will not be able to recreate the risk or control in Domain A due to indexing.
-   If you have a risk or control that you want to be assessed by users in TOP and Domain A, you can create the risk or control in Domain A.

Unless the risks and controls are in the Global domain, users should not assign risks or controls in a higher domain to users in a lower domain. In the example above, if you have a control in the TOP domain, you should not assign it for attestation to users in Domains A or B since those users would not have access to the control; thus the attestation or assessment questionnaire would not be generated.

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

## Allocation of domain values to Policy and Compliance Management objects

Records that are automatically generated either through scheduled jobs or background scripts are domain separated based on their parent object or user domain for all Policy and Compliance objects. Similarly, controls, risks, or risk assessments that are auto-generated based on the entities must also be domain separated.

The following changes are made to the domain assignment process to manage data segregation by the Managed Service Providers related to Policy and Compliance Management tables:

|Policy and Compliance Management objects|Domain source|
|----------------------------------------|-------------|
|Policy|User Domain|
|Acknowledgement Campaign|Policy Domain|
|Policy to Control Objective|Policy Domain|
|Authority Document|User Domain|
|Citation|Document Domain|
|Control Objective|User Domain|
|Control Objective to Citation|Citation Domain|
|Policy exception|User Domain|
|Approvals for Policy Exception|Policy Exception Domain|
|Policy Exception Related Records|Policy Exception Domain|
|Acknowledgement|KB Article Domain|
|Policy Category|User Domain|
|Policy Exception Integration Registry|User Domain|
|Policy exception risk rating mapping|User Domain|
|Policy/regulation compliance status|Document Domain|
|Reason Choice List|User Domain|
|Reason Choices|Policy Exception Integration Registry Domain|
|Authority document to taxonomy|Authority Document Domain|
|Citation to taxonomy|Citation Domain|
|Control|Entity Domain|
|Entity compliance status|Entity Domain|
|Control to entity|Control.Entity Domain|
|Control objective to item|Control Objective Domain|
|Control Objective to Entity Type|Entity Type Domain|
|Policy to Entity Type|Entity Type Domain|
|Article Template|User Domain|
|Compliance data source registry|User Domain|

**Parent Topic:**[Policy and Compliance Management reference](reference-data-policy-compliance.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

