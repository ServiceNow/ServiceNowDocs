---
title: HR services
description: HR services are the requests and assistance an HR organization provides its employees, such as benefits enrollment, direct deposit setup, and requests for relocation assistance.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR services

HR services are the requests and assistance an HR organization provides its employees, such as benefits enrollment, direct deposit setup, and requests for relocation assistance.

They are the starting point for HR case creation and define the process for that case type, from request to fulfillment. You can create new or modify existing HR services, as well as configure them to be available for internal use only or for employee self-service.

## HR Centers of Excellence data model

HR services are categorized under one of the HR Centers of Excellence \(COEs\), which are part of a data model that organizes HR data, services, and processes by functional discipline. Each COE is an extension of the HR Case \[sn\_hr\_core\_case\] table, and each COE is further organized by HR topic category and detail. Before you begin configuring the individual HR services, review and set up the categorization structure for them.

-   [HR Centers of Excellence data model](hr-centers-of-excellence-coes.md)
-   [HR service categorization](hr-service-categorization.md#)

## HR request to fulfillment process

In determining what HR services to offer, you should consider:

-   What are the requests you expect to receive and the services you want to provide?
-   How do you plan to report on this data? This affects how you categorize your HR services.
-   What information must you collect to fulfill the requests?
-   How can the requests be made?
    -   Email
    -   Phone
    -   Employee self-service through the HR service catalog
-   How is the request ultimately fulfilled?
    -   HR case form
    -   Fulfillment instructions
    -   Approvals
    -   Tasks
    -   Child HR services
    -   Lifecycle events
    -   Knowledge articles

## HR service configuration

HR services are the starting point for HR case creation and define the request to fulfillment process for that case type. The configuration requirements for an HR service depend on whether it is available for internal use only, or if you are allowing the employee to request the service directly from the HR service catalog through a self-service portal such as the Employee Center.

<table id="table_vy2_32n_3fb"><thead><tr><th>

HR service type

</th><th>

Configuration requirements

</th></tr></thead><tbody><tr><td>

Internal use only

</td><td>

-   HR service
-   HR case template

</td></tr><tr><td>

Employee self-service

</td><td>

-   HR service
-   HR case template
-   HR catalog item \(also known as a record producer\)

</td></tr></tbody>
</table>Not all HR services need to be accessible for employee self-service. Some services may only be initiated by HR agents, such as to set up payroll for a new hire. Some services may require the employee to contact HR directly by email or phone, such as when a manager requests a promotion for a direct report. In these cases, the HR case is created internally by the HR agent. HR services intended for internal use only require configuration of the HR service and HR case template. See [HR service configuration](hr-service-configuration.md) for more information.

Other HR services, however, may also be initiated by the employee, such as to update an employee profile or to request a password reset. These services are made available as HR catalog items in the HR service catalog. Employees can browse the HR service catalog and make requests directly from a self-service portal such as the Employee Center. HR services intended for employee self-service require configuration of the HR catalog item \(also known as a record producer\) in addition to the HR service and HR case template. See [HR catalog item configuration](hr-catalog-item-configuration.md) for more information.

## HR service catalog management

The HR service catalog provides employees a catalog of HR services that they can request directly from HR. Employees can access the HR service catalog from a self-service portal such as the Employee Center. You can manage the setup and categorization of the HR service catalog, as well as configure the individual HR catalog items that populate it.

-   [HR service catalog management](hr-service-catalog-management.md)
-   [HR service catalog categorization](hr-service-catalog-categorization.md#)

## HR template configuration

HR templates allow you to: automatically populate fields on an HR case or task form. You can configure HR templates for:

-   HR services
-   HR catalog items
-   HR service activities
-   Lifecycle event activities

For more information, see [HR templates](hr-template-configuration.md).

-   **[HR Centers of Excellence data model](hr-centers-of-excellence-coes.md)**  
Organize HR data, services, and processes by functional discipline with the HR Centers of Excellence \(COEs\) data model.
-   **[HR service configuration](hr-service-configuration.md)**  
HR services are the requests and assistance an HR organization provides its employees. You can configure an HR service to define the request to fulfillment process for that case type.
-   **[HR service catalog management](hr-service-catalog-management.md)**  
Empower employees to request HR services through the HR service catalog. The HR service catalog provides employees a catalog of HR services that they can request directly from HR, such as to add beneficiaries to a benefits plan, request a travel visa, or inquire about a discrepancy in their paycheck.
-   **[HR fulfillment instructions](hr-fulfillment-instructions.md)**  
HR fulfillment instructions provide focused and targeted information on how an agent can complete an HR case faster and more efficiently for HR Service Delivery Agent Workspace and legacy HR Case Management.
-   **[HR templates](hr-template-configuration.md)**  
HR templates allow you to automatically populate fields on an HR case or task form. You can configure HR templates for HR services, HR catalog items, HR service activities, and lifecycle event activities.

**Parent Topic:**[HR Administration](c_AdministerHRServiceManagement.md)

