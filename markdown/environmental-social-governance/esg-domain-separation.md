---
title: Domain separation and Operational Sustainability Management
description: Domain separation is supported for Operational Sustainability Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Operational Sustainability Management \(formerly ESG\) reference, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Domain separation and Operational Sustainability Management

Domain separation is supported for Operational Sustainability Management. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Overview of domain separation

Domain separation is useful for users who:

-   Enforce absolute data segregation between business entities \(data separation\).
-   Customize business process definitions and user interfaces for each domain \(delegated administration\).
-   Maintain global processes and global reporting in a single instance.

These users can choose to expand or collapse the domain scope to show or hide data from other domains.

**Note:** Users always have access to data from domains that have been explicitly granted to them by domain visibility.

## How domain separation works in Operational Sustainability Management

While Operational Sustainability Management supports separation of data, separation of logic and process is not fully supported. Many types of records in the Operational Sustainability Management application are automatically generated through user processes. Integrations with Project Portfolio Management and GRC: Metrics can create and associate data automatically. For records that are automatically and manually generated, the domain of the record is the same as the domain of the user responsible for creating or generating the records. Users must ensure that they are creating and generating records at the right domain level so that they are visible to the right set of users.

For example, suppose you have domains that look like:

-   Global
-   TOP
    -   Domain A
    -   Domain B

If you have ESG goals, material topics and targets that you want to be assessed by users in domains A and B, the ESG goals, material topics and targets should be manually created at the global level. If ESG goals, material topics and targets are created in Domain B, you will not be able to use them in Domain A due to indexing.

If you have ESG goals, material topics and targets that you want to be assessed by users in Top and Domain A, you can create the risk or control in Domain A. Unless the ESG goals, material topics and targets are in the Global domain, users must not assign risks or controls in a higher domain to users in a lower domain. In the example given, if you have an ESG goal in the Top domain, you should not assign it to program manager in Domains A or B since those users would not have access to the this goal.

## Domain separated tables

The following is the list of domain separated tables:

-   Disclosure
-   Disclosure Summary
-   Goal Activity Summary
-   Heatmap Chart Color
-   Composite Metric Definition to Citation
-   Composite Metric Definition to Goal
-   Composite Metric Definition to Target
-   Control to Goal
-   Control Objective to Goal
-   Citation to Disclosure
-   Metric to Disclosure
-   Metric Definition to Disclosure
-   Entity to Goal
-   Goal to Citation
-   Goal to Disclosure
-   Material Topic to Goal
-   Metric to Citation
-   Metric Definition to Citation
-   Metric Definition to Goal
-   Metric Definition to Target
-   Metric to Goal
-   Metric to Target
-   Policy to Goal
-   Risk to Goal
-   Risk Statement to Goal
-   Material Topic

For more information on these tables, see [Components installed with Operational Sustainability Management \(formerly ESG Management\)](../reference/components-installed-with-esg.md).

## Use case

ESG data can be separated from the data of other departments. Each business area using the Operational Sustainability Management application can have separate data that cannot be shared with other departments. Therefore, each department can have its own goals, targets, material topics, and so on. When looking at a goal from the ESG domain, the user can choose to expand the domain scope to show values from the ESG domain or collapse the domain scope to show only goals that match the ESG domain. By default, domain separation adds a domain field to the Task \[task\]and Configuration Items \[cmdb\_ci\] tables and their extensions. You can extend domain separation to any new tables you create by adding a sys\_domain field to the table's dictionary definition. By default, the system only domain-separates platform and baseline application tables where appropriate.

**Note:** ServiceNow® does not recommend domain separating platform tables such as any table with the sys\_ prefix such as the Dictionary Entry \[sys\_dictionary\] and Dictionary Entry Override \[sys\_dictionary\_override\] tables because it can produce unexpected results.

In this use case, client scripts, business rules, workflows, processes, and so on can be domain-separated. While the behavior offered with domain separation provides multi-tenancy support, multi-tenancy is still contained within a single instance. This means that some global properties, some global data, and some global processes are shared across all domains. For example, the system’s “Remember me” option on the login page is global and cannot be specified per domain. If you need complete and total separation of all system properties and do not require global reporting or global processes, separate instances are the best option.

**Parent Topic:**[Operational Sustainability Management \(formerly ESG\) reference](reference-data-esg.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

