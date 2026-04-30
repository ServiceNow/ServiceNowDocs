---
title: Reference for HR Multi Instance Integration
description: Reference for HR Multi Instance Integration.Several types of components are installed with activation of the HR Multi Instance Integration for Provider plugin, including user roles.Several types of components are installed with activation of the HR Multi Instance Integration for Consumer plugin, including tables, user roles, and scheduled jobs.Review these general guidelines and limitations before using the HR Multi Instance Integration application.
locale: en-US
release: zurich
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [HR Multi Instance Integration, HR Service Delivery, Employee Service Management]
---

# Reference for HR Multi Instance Integration

Reference for HR Multi Instance Integration.

## Installed with HR Multi Instance Integration for Provider

Several types of components are installed with activation of the HR Multi Instance Integration for Provider plugin, including user roles.

### Roles installed

<table id="table_bqs_2vr_gdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HR Multi Instance Integration Provider​ Admin\[sn\_hr\_mii\_provider.admin\]

</td><td>

Can connect with a consumer instance, create or update a remote record producer on provider instance, read or write provider tasks, create consumer criteria for remote access controls, and enable or disable magic links.

</td><td>

-   sn\_hr\_mii\_base.admin
-   sn\_hr\_mii\_provider.user

</td></tr><tr><td>

HR Multi Instance Integration Provider​ User\[sn\_hr\_mii\_provider.user\]

</td><td>

This role is used by the Create HR Case from Provider Task flow for creating a remote HR case from a provider task.

</td><td>

 

</td></tr></tbody>
</table>## Installed with HR Multi Instance Integration for Consumer

Several types of components are installed with activation of the HR Multi Instance Integration for Consumer plugin, including tables, user roles, and scheduled jobs.

### Roles installed

<table id="table_bqs_2vr_gdc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

HR Multi Instance Integration Consumer​ Admin\[sn\_hr\_mii\_consumer.admin\]

</td><td>

Can connect with the provider instance, enable a remote record producer and related properties on consumer instance, read or write provider tasks, add pre-approval flows, set the value of the **Redirect timeout** option in the magic links settings.

</td><td>

sn\_hr\_mii\_base.admin

</td></tr></tbody>
</table>## General guidelines and limitations

Review these general guidelines and limitations before using the HR Multi Instance Integration application.

See this [KB1808151](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1808151).

