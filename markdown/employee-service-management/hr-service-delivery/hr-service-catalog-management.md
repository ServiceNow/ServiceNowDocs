---
title: HR service catalog management
description: Empower employees to request HR services through the HR service catalog. The HR service catalog provides employees a catalog of HR services that they can request directly from HR, such as to add beneficiaries to a benefits plan, request a travel visa, or inquire about a discrepancy in their paycheck.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR service catalog management

Empower employees to request HR services through the HR service catalog. The HR service catalog provides employees a catalog of HR services that they can request directly from HR, such as to add beneficiaries to a benefits plan, request a travel visa, or inquire about a discrepancy in their paycheck.

Employees can access the HR service catalog from a self-service portal such as the Employee Service Center. You can manage the setup and categorization of the HR service catalog, as well as configure the individual HR catalog items that populate it.

## HR service catalog categorization

The HR service catalog is a collection of HR catalog items that employees can request directly from HR. The HR catalog items are organized into categories, which define the organizational structure for the catalog. For example, the items can be categorized by benefits, employee data management, employee relations, general, HR systems, payroll, talent management, and visas.

**Note:** The COEs available to you may differ depending on the HR package you have.

-   The categorization of HR catalog items are employee-facing only, and have no relation to the categorization of HR services under the HR Centers of Excellence \(COEs\) data model.
-   If you are creating a new HR service and plan to make it available for employee self-service, see [HR catalog item configuration](hr-catalog-item-configuration.md) instead. Creating a new HR catalog item automatically creates a corresponding HR service, and you can avoid creating duplicate services.
-   If you have an existing HR service that you want to make available for employee self-service, do not create an HR catalog item. \(Creating a HR catalog item automatically creates a corresponding HR service.\) Instead, see [Configure a record producer for an HR service](../task/configure-hr-record-producer.md) to add the existing service as an HR catalog item in the HR service catalog.
-   The Agent Workspace for HR Case Management is highly configurable for HR agents. It supports the same functionality in the Classic HR Service Delivery Agent Workspace.

![The HR service catalog organizes the HR catalog items by category.](../image/hr-service-catalog-categorization.png)

You can manage the creation or modification of categories in the HR service catalog, as well as assign or remove HR catalog items from a category or assign or remove categories from an HR catalog item. To manage the categorization of HR catalog items in the HR service catalog, see [HR service catalog categorization](hr-service-catalog-categorization.md#).

## HR catalog item configuration

HR catalog items are the HR services that your organization makes available for employees to request directly from the HR service catalog. \(Not all HR services need to be accessible to employees; some services are only initiated internally by HR agents. This means that all HR catalog items have a corresponding HR service, but not all HR services have a corresponding HR catalog item.\) To configure the HR catalog items, see [HR catalog item configuration](hr-catalog-item-configuration.md).

Once an HR catalog item is published to the HR service catalog, it is available for employees to request. When an employee submits an HR catalog item request, an HR case is created.

-   **[HR service catalog categorization](hr-service-catalog-categorization.md#)**  
HR catalog items in the HR service catalog are organized into categories. The categories define the organizational structure for the catalog so that employees can more easily browse and request the HR services they need.
-   **[HR catalog item configuration](hr-catalog-item-configuration.md)**  
HR catalog items are the HR services that your organization makes available for employees to request directly from the HR service catalog.

**Parent Topic:**[HR services](hr-service-administration.md)

**Related topics**  


[Service Catalog](https://www.servicenow.com/docs/access?context=service-catalog&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

