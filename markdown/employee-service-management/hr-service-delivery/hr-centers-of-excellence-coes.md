---
title: HR Centers of Excellence data model
description: Organize HR data, services, and processes by functional discipline with the HR Centers of Excellence \(COEs\) data model.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR Centers of Excellence data model

Organize HR data, services, and processes by functional discipline with the HR Centers of Excellence \(COEs\) data model.

## COE data model overview

The HR Centers of Excellence \(COEs\) data model provides a structured approach to organizing HR services by functional discipline. This model helps organizations standardize processes, improve service delivery, and maintain consistent reporting across different HR domains.

The HR Centers of Excellence video provides an overview of the HR Centers of Excellence \(COEs\), their benefits, the COE data model, how to configure and use the COE data model, and how to handle a request for a new COE.

Each COE can be configured to its unique function, such as payroll or employee relations. The COE data model allows you to limit access to sensitive information, promote consistency for metrics and reporting, and help drive automation by defining the request to fulfillment process at the HR service level.

## HR Centers of Excellence structure

Each HR Center of Excellence is an extension of the HR Case \[sn\_hr\_core\_case\] table and is organized around a functional discipline, such as employee relations, lifecycle events, payroll, talent management, workforce administration, total rewards, HRIT operations, benefits, compensation, corporate communications, and global mobility.

**Note:** The benefits, compensation, corporate communications, and global mobility COEs are inactive by default.

![HR COE data model showing the hierarchical structure of Centers of Excellence](../image/hr-coe-data-model.png)

## Data model hierarchy

Each COE is organized by HR topic category and detail, which defines the first- and second-level categorization for HR services under that COE. This hierarchical structure provides flexibility in organizing services:

-   Each COE can have one or more topic categories
-   Each topic category can have one or more topic details
-   Each topic detail can have one or more HR services

This structure enables you to categorize HR services by functional area, and you can configure the categorization structure and the individual HR services to meet your organization's needs.

![HR COE data model components showing the relationship between COEs, topic categories, topic details, and services](../image/hr-coe-data-model-components.png)

## HR service categorization setup

Before configuring individual HR services, review and set up the categorization structure for them. This foundational step ensures that your services are properly organized within the COE framework.

**Note:** For a list of base system COEs and how to enable or disable them, see [Enable or disable an HR Center of Excellence \(COE\)](hr-service-categorization.md#).

## Roles

The following roles can create and configure COEs:

-   System administrator \(admin\).
-   Lifecycle event administrator \(sn\_hr\_le.admin\) with the Delegated Developer \(delegated\_developer\) role.

-   **[HR service categorization](hr-service-categorization.md#)**  
HR services are categorized under one of the HR Centers of Excellence \(COEs\), which are part of a data model that organizes HR data, services, and processes by functional discipline.

**Parent Topic:**[HR services](hr-service-administration.md)

