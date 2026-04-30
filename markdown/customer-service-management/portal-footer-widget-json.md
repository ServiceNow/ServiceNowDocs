---
title: Portal Polaris Footer widget JSON parameters
description: Use the JSON parameters to define aspects of the Portal Polaris Footer widget on the portal page.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customer Service Management reference, Customer Service Management]
---

# Portal Polaris Footer widget JSON parameters

Use the JSON parameters to define aspects of the Portal Polaris Footer widget on the portal page.

**Note:** This information assumes that you’re familiar with the JSON code format.

<table id="table_csm_base_entities"><thead><tr><th>

Parameter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

org\_info

</td><td>

The company name and address to appear on the portal footer.

</td></tr><tr><td>

copyright

</td><td>

Copyright information appears on the portal footer.You can display copyright symbol, the year of copyright, and the name of the copyright holder or organization in the footer.

</td></tr><tr><td>

logo\_img\_name

</td><td>

The image that can be displayed as a logo in the footer. The image name should be accessed from the Images \[db\_image\] table.

</td></tr><tr><td>

sitemap\_links\_menu\_sys\_id

</td><td>

The system identifier \(sys\_id\) of the menu record is used to display sitemap links in the Portal Polaris Footer widget. You can create a menu record and map it to the sitemap links by including its sys\_id in the JSON code. For more information on how to create a menu record, see [Menu Item form](https://www.servicenow.com/docs/access?context=menu-item-form&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

</td></tr><tr><td>

footer\_links\_menu\_sys\_id

</td><td>

The system identifier \(sys\_id\) of the menu record is used to display footer links in the Portal Polaris Footer widget. You can create a menu record and map it to the footer links by including its sys\_id in the JSON code. For more information on how to create a menu record, see [Menu Item form](https://www.servicenow.com/docs/access?context=menu-item-form&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

</td></tr><tr><td>

social\_links\_menu\_sys\_id

</td><td>

The system identifier \(sys\_id\) of the menu record is used to display social links in the Portal Polaris Footer widget. You can create a menu record and map it to the social links by including its sys\_id in the JSON code. For more information on how to create a menu record, see [Menu Item form](https://www.servicenow.com/docs/access?context=menu-item-form&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US).

</td></tr></tbody>
</table>