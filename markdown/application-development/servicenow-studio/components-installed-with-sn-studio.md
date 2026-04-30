---
title: Components installed with ServiceNow Studio
description: When you activate the ServiceNow Studio plugin, various components like tables are automatically installed.
locale: en-US
release: xanadu
product: ServiceNow Studio
classification: servicenow-studio
topic_type: concept
last_updated: "2024-10-28"
reading_time_minutes: 1
breadcrumb: [Installing ServiceNow Studio, Configuring ServiceNow Studio, Building applications with ServiceNow Studio, Developing your application, Building applications]
---

# Components installed with ServiceNow Studio

When you activate the ServiceNow Studio plugin, various components like tables are automatically installed.

## Tables and roles installed with ServiceNow Studio

One table is shipped directly with ServiceNow Studio: Resources \[sn\_sns\_resources\]. This table populates the Resources section at the bottom of the home page.

No specific roles are shipped with ServiceNow Studio, but Admin and Delegated Developer roles are used. For more information, see [ServiceNow Studio personas and roles](sn-studio-personas-roles.md).

## Plugin installed with ServiceNow Studio

The ServiceNow Studio \[sn\_sns\] plugin is installed with several dependencies.

<table id="table_xfk_wxh_zdc"><thead><tr><th>

Plugin \[ID\]

</th><th>

Description

</th><th>

Dependencies

</th></tr></thead><tbody><tr><td>

ServiceNow Studio\[sn\_sns\]

</td><td>

ServiceNow Studio provides a unified experience for all ServiceNow development activities.

</td><td>

-   sn\_udc
-   sn\_studio\_commons
-   sn\_app\_obj\_wizards
-   sn\_deploy\_pipeline
-   sn\_workflow\_studio

</td></tr></tbody>
</table>**Parent Topic:**[Installing ServiceNow Studio](installing-servicenow-studio.md)

