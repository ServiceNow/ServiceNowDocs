---
title: HR Centers of Excellence data model
description: Organize HR data, services, and processes by functional discipline with the HR Centers of Excellence \(COEs\) data model.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [HR services, HR Administration, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR Centers of Excellence data model

Organize HR data, services, and processes by functional discipline with the HR Centers of Excellence \(COEs\) data model.

The HR Centers of Excellence video provides an overview of the HR Centers of Excellence \(COEs\), their benefits, the COE data model, how to configure and use the COE data model, and how to handle a request for a new COE.Each COE can be configured to its unique function, such as to payroll or employee relations. The COE data model further allows you to limit access to sensitive information, promote consistency for metrics and reporting, and help drive automation by defining the request to fulfillment process at the HR service level.

## HR Centers of Excellence \(COEs\) overview

Each HR Center of Excellence is an extension of the HR Case \[sn\_hr\_core\_case\] table and is organized around a functional discipline, such as employee relations, lifecycle events, payroll, talent management, workforce administration, total rewards, HRIT operations, benefits, compensation, corporate communications, and global mobility.

**Note:** The benefits, compensation, corporate communications, and global mobility COEs are disabled by default.

**Note:** The COEs available to you may differ depending on the HR package you have.

-   The categorization of HR catalog items are employee-facing only, and have no relation to the categorization of HR services under the HR Centers of Excellence \(COEs\) data model.
-   If you are creating a new HR service and plan to make it available for employee self-service, see [HR catalog item configuration](hr-catalog-item-configuration.md). Creating a new HR catalog item automatically creates a corresponding HR service, and you can avoid creating duplicate services.
-   If you have an existing HR service that you want to make available for employee self-service, do not create an HR catalog item. \(Creating a HR catalog item automatically creates a corresponding HR service.\) Instead, see [Configure a record producer for an HR service](../task/configure-hr-record-producer.md) to add the existing service as an HR catalog item in the HR service catalog.
-   The Agent Workspace for HR Case Management is highly configurable for HR agents. It supports the same functionality in the Classic HR Service Delivery Agent Workspace.

![HR COE data model](../image/hr-coe-data-model.png)

Each COE is further organized by HR topic category and detail, which defines the first- and second-level of categorization for HR services under that COE. Each COE can have one or more topic categories. Each topic category can have one or more topic details. And each topic detail can have one or more HR services. This structure enables you to categorize HR services by functional area, and you can configure the categorization structure and the individual HR services to meet the needs of your organization.

![HR COE data model](../image/hr-coe-data-model-components.png)

## HR service categorization setup

Before you begin configuring the individual HR services, review and set up the categorization structure for them.

**Note:** For a list of base system COEs and how to enable or disable them, see [Enable or disable an HR Center of Excellence \(COE\)](hr-service-categorization.md#).

## Roles

The System Administrator \(admin\) role can configure and create new COEs.

The Lifecycle Event Administrator \(sn\_hr\_le.admin\) role with the Delegated Developer \(delegated\_developer\) role can also configure and create new COEs.

-   **[HR service categorization](hr-service-categorization.md#)**  
HR services are categorized under one of the HR Centers of Excellence \(COEs\), which are part of a data model that organizes HR data, services, and processes by functional discipline.

**Parent Topic:**[HR services](hr-service-administration.md)

