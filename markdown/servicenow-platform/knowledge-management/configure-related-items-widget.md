---
title: Configure related catalog item widget instance options
description: Configure the Related Catalog Item widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal. These options relate to the list of catalog items mapped to an article.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Knowledge Management Service Portal widgets, Configure the Knowledge Management Service Portal, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure related catalog item widget instance options

Configure the Related Catalog Item widget instance options for the Knowledge Management article view page in the Knowledge Management Service Portal. These options relate to the list of catalog items mapped to an article.

## Before you begin

Role required: sp\_admin or admin

## About this task

The knowledge article view page displays the Related Items section when an article has related catalog items. Use the widget instance options to customize the Related Items section on the article view page.

## Procedure

1.  Navigate to the Knowledge Management homepage in the Knowledge Management Service Portal by adding `/kb` to the end of your instance URL.

    **Note:** Your administrator might have changed this default navigation.

2.  Search for and click the article for which you want to modify the instance options for the Related Catalog Item widget.

3.  Press Control and right-click the Related Items section.

4.  Click **Instance Options**.

5.  Configure settings for the Related Catalog Item widget.

    |Instance option|Description|
    |---------------|-----------|
    |Source Table|Source table containing related catalog items. The source table specified in the base system is Related Catalog Items \(kb\_2\_sc\).|
    |Source Column|Field in the source table referring to the source record. The source column specified in the base system is Knowledge article \(kb\_knowledge\).|
    |Title|Title that appears on the widget header. The default title is Related Items.|
    |Max Number|Maximum number of catalog items to include in the Related Items section on the article view page. The maximum number specified in the base system is 5.|
    |Use Full Width|Option for displaying the widget in a 12-column grid at 100% of the available width. If you clear the check box, the widget displays at 75% of the available width.|
    |Target Column|Field in the source table referring to the target record. The target column specified in the base system is Catalog item \(sc\_cat\_item\).|
    |Source Id|URL parameter containing the unique record identifier \(sys\_id\) of the source record. For the article view page, the URL parameter containing the source ID is sys\_kb\_id.|

6.  Click **Save**.


**Parent Topic:**[Knowledge Management Service Portal widgets](../concept/km-service-portal-widget-instances.md)

**Related topics**  


[Map catalog items related to an article](map-related-items.md)

