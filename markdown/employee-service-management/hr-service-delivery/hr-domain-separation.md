---
title: Domain Separation and HR Service Delivery
description: The ServiceNow HR Service Delivery application improves the employee service experience by automating HR interactions and providing a single platform for all HR services. Domain separation is supported in HR Service Delivery.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [HR Service Delivery, Employee Service Management]
---

# Domain Separation and HR Service Delivery

The ServiceNow® HR Service Delivery application improves the employee service experience by automating HR interactions and providing a single platform for all HR services. Domain separation is supported in HR Service Delivery.

Domain separation separates data, processes, and administrative tasks into logical groupings called domains within a single ServiceNow instance. You can then control several aspects of this separation, including which users can see and access data.

To learn more about domain separation, see:

-   [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0715934)
-   [Understanding domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/c_DomainSeparation.md)

HR Service Delivery provides the basic level of domain separation support. Basic domain separation \(data separation \) implies that if the data and all the related configurations reside within a particular domain, HR Service Delivery will function as expected. Hierarchical domain structure, sharing of data/configurations and logic/process separation is not supported by default in HR Service Delivery as per the basic domain separation definition.

## Support level: Basic

**Note:** To learn more about support levels, see [Domain separation levels of support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-domain-levels.md).

-   There is business logic to ensure data goes into the proper domain for the application’s service provider use cases.
-   In the application, the user interface, cache keys, reporting, rollups, aggregations, and so on, all consider domain at run time.
-   The owner of the instance needs to be able to set up the application to function normally across multiple tenants.

Use case: As a Service Provider organization, when I receive a case or a chat from a tenant in the system, I should be able to see and resolve that case without other tenant customers being aware of the case or process.

## Overview of HRSD domain separation

Domain separation is best for customers who:

-   Enforce absolute data segregation between business entities \(data separation\).
-   Customize business process definitions and user interfaces for each domain \(delegated administration\).
-   Maintain some global processes and global reporting in a single instance.

These users can choose to expand or collapse the domain scope to show or hide data from other domains. For example, data from Company A can be separated from the data of Company B and Company C. Each domain using the HR Service Delivery application can have separate data that cannot be shared with other domains.

**Note:** Based on the hierarchy, users can see data in their home domain and child domains of that home domain. Users will not have access to data in their parent domains, peer domains, or domains in other branches of the hierarchy. Users always have access to data from domains that have been explicitly granted to them by domain visibility and domain contains.

![Infographic explaining Domain Separation in HR Service Delivery](../image/domain-separation-hrsd.png)

## How domain separation works in HR Service Delivery

-   While HR Service Delivery supports separation of data, separation of logic and process is not fully supported.

    **Note:**

    -   For more details on domain separation in HR Service delivery, see [Guidance for proper HR Service Delivery domain separation](hr-domain-rec.md).
    -   To learn more about process separation, see the Data Separation versus Process Separation section in this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0715934).
-   When working in a domain-separated implementation, ensure that records are created at the right domain level so that it is visible to the right set of users.

    For example, domains that look like:

    -   Global → TOP

        -   Domain A
        -   Domain B
        **Note:** Global is not a domain.

        When agents are shared across domains, agents should reside in global and have access to the remote HR cases of all onboarded consumers.

    -   For any user in Domain A or Domain B to access an HR case, the HR case must be created at an global level.
    -   If an HR case is created in Domain A, a user from Domain B cannot access it. Likewise, if an HR case is created in Domain B, a user from Domain A cannot access it.
    -   For an HR case to be visible to the users in TOP and Domain A, create the HR case in Domain A.
    -   For an HR case to be visible to the users in TOP and Domain B, create the HR case in Domain B.

## Use case: Domain separation in HR Service Delivery

While the behavior offered with domain separation provides multi-tenancy support, multi-tenancy is still contained within a single instance. A few properties, data and processes are always global and shared across all domains. For example, the system’s “Remember me” option on the login page is global and cannot be specified per domain.

If a complete and total separation of all system properties is needed and does not require global reporting or global processes, separate instances are the best option.

