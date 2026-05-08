---
title: Domain separation and Universal Task
description: Domain separation is supported for ServiceNow Universal Task. Universal Task enables agents to request extra information from the employee or to task the employee to accomplish an activity, in order to resolve a ticket. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Universal Task
classification: universal-task
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up and configuring Universal Task, Universal Task, Employee Service Management]
---

# Domain separation and Universal Task

Domain separation is supported for ServiceNow Universal Task. Universal Task enables agents to request extra information from the employee or to task the employee to accomplish an activity, in order to resolve a ticket. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Basic



-   Business logic: Ensure that data goes into the proper domain for the application’s service provider use cases.
-   The application supports domain separation at run time. The domain separation includes separation from the user interface, cache keys, reporting, rollups, and aggregations.
-   The owner of the instance must set up the application to function across multiple tenants.

Sample use case: When a service provider \(SP\) uses chat to respond to a tenant-customer’s message, the customer must be able to see the SP's response.

For more information on support levels, see Application support for domain separation.

## Overview

In the Universal Task framework, all the configurations are process domain-separated, and the data tables, namely, Universal Task table, Employee form table, and Task template table are data domain separation offerings.

## How domain separation works in Universal Task

The configuration tables in Universal Task are process domain-separated. So, the configurations created by the parent domains are also implemented in the child domains. However, a child domain can override the configuration, if needed. For example, In an organization, the services are the child domains, while the organization is the parent domain. The task types available for Universal Task in a particular organization, will also be available for the various services of the organization. However, a particular service can override the task types as needed.

The data tables in Universal Task are data domain-separated. So the data stored in any of the child domains is accessible to the parent domain. For instance, if a service is using task templates, the data captured in the Task templates table for the service domain is accessible to the organization domain, but not to the domains of other services, unless configured.

## Tables

The following Configuration tables are process separated.

-   sn\_uni\_task\_config
-   sn\_uni\_task\_base\_task\_config
-   sn\_uni\_task\_catalog\_task\_config
-   sn\_uni\_task\_emp\_input\_task\_config

The following Data tables are data separated.

-   sn\_uni\_task\_universal\_task
-   sn\_uni\_task\_template
-   sn\_uni\_task\_employee\_form

**Parent Topic:**[Setting up and configuring Universal Task](set-up-universal-task.md)

**Related topics**  


[bundle-psec.domain-sep-landing-page]

