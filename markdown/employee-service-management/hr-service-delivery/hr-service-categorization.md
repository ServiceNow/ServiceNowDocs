---
title: HR service categorization
description: HR services are categorized under one of the HR Centers of Excellence \(COEs\), which are part of a data model that organizes HR data, services, and processes by functional discipline.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [HR Centers of Excellence data model, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# HR service categorization

HR services are categorized under one of the HR Centers of Excellence \(COEs\), which are part of a data model that organizes HR data, services, and processes by functional discipline.

Each COE is an extension of the HR Case \[sn\_hr\_core\_case\] table, and each COE is further organized by HR topic category and detail. Before you begin configuring the individual HR services, determine which COEs you want to use, and then create or modify the appropriate HR topic categories and details for each COE.

-   **[Enable or disable an HR Center of Excellence \(COE\)](../task/configure-hr-center-of-excellence-coe.md)**  
Enable or disable an HR Center of Excellence \(COE\) for use. COEs are tables that extend the HR Case \[sn\_hr\_core\_case\] table and part of a functional discipline, such as total rewards or talent management. COEs are also part of HR services that contain topic category and detail.
-   **[Configure an HR topic category](../task/configure-hr-topic-category.md)**  
Create or modify an HR topic category to define the first-level of categorization for HR services. Each topic category is associated with a single HR Center of Excellence \(COE\).
-   **[Configure an HR topic detail](../task/configure-hr-topic-detail.md)**  
Create or modify an HR topic detail to define the second-level of categorization for HR services. Each topic detail is associated with a single topic category and HR Center of Excellence \(COE\).
-   **[Configuring HR Service Delivery Center of Excellence \(COE\) security policies](hr-coe-security-policies.md)**  
Use COE Access Control List \(ACLs\) Configuration to allow specific groups read or write access to HR cases under a specific COE.
-   **[Create COE security](configure-hr-coe-security.md)**  
Place security on a COE to prevent a group from accessing another group's cases.
-   **[Use COE Security Diagnostics](coe-diagnostics-tool.md)**  
Enable HR administrators to determine how the COE \(HR Centers of Excellence\) security policies are evaluated for HR agents.

**Parent Topic:**[HR Centers of Excellence data model](hr-centers-of-excellence-coes.md)

