---
title: User criteria for Service Portal
description: User criteria enables you to allow access to users based on role, department, group, location, or company. Administrators can control access to pages, widgets, widget instances, announcements, and search sources in a portal by creating and applying user criteria.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing portal access, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# User criteria for Service Portal

User criteria enables you to allow access to users based on role, department, group, location, or company. Administrators can control access to pages, widgets, widget instances, announcements, and search sources in a portal by creating and applying user criteria.

User criteria records define conditions that are evaluated against user records. When user criteria is defined, portal records are only visible to users who pass the defined conditions.

User criteria is a platform feature used in Service Portal. Learn more about user criteria in the ServiceNow AI Platform:

-   Service Catalog: [Set security for items and categories](https://www.servicenow.com/docs/access?context=c_ServiceCatalogAccessControls&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).
-   Knowledge management: [Control access at the knowledge base level through user criteria](https://www.servicenow.com/docs/access?context=t_SelectUserCriteria&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Important:** After making user criteria additions or changes, you may need to log out and log back in to clear the prior configuration.

## Converting role-based permissions to user criteria records

User criteria in Service Portal replaces role-based permissions. After activating the user criteria for Service Portal plugin, you must [Set the user criteria for Service Portal system property](../task/activate-user-crit.md) to **true**. When the system property is set to true, any existing roles defined for a page, widget, or search source are automatically converted into user criteria records. To disable user criteria and continue using role-based permissions, set the system property to **false**.

## User criteria checks

User criteria uses the following checks in Service Portal to verify user access.

![User criteria check flow chart describing how the system verifies whether a user can access an item.](../image/UserCriteriaCheck.png)

## Page access user criteria

The following diagram shows how the system decides whether a user can access a page based on user criteria.

![Flow chart with descriptions of different checks in the page access process.](../image/PageAccessFlowChart2.png)

## Widget access user criteria

The following diagram shows how the system determines whether a user has access to a particular widget or widget instance.

![Flow chart detailing the process the system uses to verify a user's ability to access a widget.](../image/WidgetAccess2.png)

-   **[Activate the user criteria for Service Portal plugin](../task/activate-user-criteria.md)**  
You can activate the Service Portal User Criteria Support plugin \(com.glide.service-portal.user-criteria\) if you have the admin role.
-   **[Set the user criteria for Service Portal system property](../task/activate-user-crit.md)**  
After activating the Service Portal User Criteria Support plugin, you must set the system property to true.
-   **[Create a user criteria record for Service Portal](../task/create-user-criteria-record.md)**  
Create a user criteria record to apply to items in Service Portal and control user access to pages, widgets, widget instances, and search sources.
-   **[Apply user criteria to a page, widget, or widget instance](../task/widget-user-criteria.md)**  
Assign user criteria to pages, widgets, or widget instances to limit user access to content in a portal.
-   **[Apply user criteria to a search source](../task/user-crit-search-source.md)**  
Assign user criteria to search sources to limit user access to content in a portal.

**Parent Topic:**[Managing portal access](portal-security.md)

