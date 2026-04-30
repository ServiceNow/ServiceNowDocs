---
title: Set security for items and categories
description: An administrator can control access to content in the service catalog by creating and applying user criteria records.
locale: en-US
release: zurich
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Service Catalog security, Service Catalog configuration, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set security for items and categories

An administrator can control access to content in the service catalog by creating and applying user criteria records.

Catalog managers and catalog editors can apply existing user criteria for items and categories to which they are assigned. Catalog managers and catalog editors cannot create or edit user criteria directly.

You can [create user criteria records](../task/t_CreateAUserCriteriaRecord.md#) that define conditions for user information and then apply these criteria records to catalog items and categories. In this way you can control access to these items and categories.

For example, create a **USA Sales** user criteria record matching users who are both in the sales team and based in the USA. Then apply this record to the **USA IT Hardware** catalog category, so only users matching the record can access that category.

The feature is active by default in new Fuji instances and upgraded instances that do not use [entitlement-based](c_LegcySrvcCatAccessCntrol.md) access controls. If you upgrade an instance that uses entitlements, you can [migrate to user criteria](c_MigrtSvcCatUserCriteria.md#) to take advantage of the improved control, flexibility, and reuse.

Access controls allow you to:

-   Manage access to multiple items and categories in one user criteria record. For example, create a single **UK Employees** user criteria record and apply it to multiple items and categories that are available to employees in the UK.
-   Allow access if one condition matches, or if all conditions match. For example, define that only users who are both in a specific location and who belong to a specific department can have access.
-   Use **Available For** and **Not Available For** lists to allow or prohibit access to users matching the conditions in a criteria record. For example, specify that a US-based catalog category is available for the users located in the USA but is not available for users belonging to the Sales department \(whether in the US or not\).
-   [Extend matching](../task/t_ExtendUserCriteria.md) to create conditions matching additional fields in the User \[sys\_user\] table, without having to use a script. For example, you can add a condition to match items against the **Cost center** field in user records.

**Important:** After making user criteria additions or changes, you may need to log out and log back in to clear the prior configuration.

-   **[Create a user criteria record in Service Catalog](../task/t_CreateAUserCriteriaRecord.md#)**  
Create a user criteria record to define conditions that are evaluated against user records.
-   **[Apply user criteria to items and categories](../task/t_AppUserCritItemsCat.md#)**  
Apply a user criteria record to items and categories, either from the item or category form or from the user criteria form.
-   **[Extend user criteria](../task/t_ExtendUserCriteria.md)**  
Extend the user criteria table when the available user criteria fields are not sufficient. User criteria references various user fields \(fields from the User \[sys\_user\] table\), such as department, company, and groups. You can extend user criteria with a custom field to include any other user reference field \(field from the User \[sys\_user\] table\) of interest.
-   **[User criteria migration](c_MigrtSvcCatUserCriteria.md#)**  
Service catalog user criteria records provide access control for service catalog items and categories.

**Parent Topic:**[Service Catalog security](../topic/p_ServiceCatalogSecurity.md)

**Related topics**  


[Debug user criteria of a catalog item](../task/debug-user-criteria-cat-item.md)

