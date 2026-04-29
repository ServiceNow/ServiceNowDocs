---
title: Responsive dashboard properties
description: Use properties to fine-tune dashboard behavior and appearance.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Responsive dashboard properties

Use properties to fine-tune dashboard behavior and appearance.

Navigate to **System Properties** &gt; **Dashboard Properties** to configure the main responsive dashboard properties.

## Responsive Dashboard properties

<table id="table_x3q_xgb_fbb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable the unified analytics workspace experience, which shows all responsive dashboards and Next Experience dashboards in the same overview in the Analytics Center. Upon upgrade to Australia, this property is set to true by default.

com.glide.par.unified\_analytics.enabled

</td><td>

-   Type: true \| false
-   Default value: true
-   Location: **System Properties** &gt; **Dashboard Properties**

 When enabled, users see both Platform Analytics and core UI \(responsive\) dashboards in the Analytics Center. Users can still drill down to KPI details from responsive dashboard indicator visualizations.

</td></tr><tr><td>

Apply security rules to the list of users, user groups, and roles that are visible when sharing dashboards.

glide.cms.dashboards.sharing\_with\_secure\_search

</td><td>

-   Type: true \| false
-   Default value: false
-   Location: **System Properties** &gt; **Dashboard Properties**

 When enabled, the list of users, user groups, and roles that are visible in the sharing panel is restricted. The restriction is based on the configuration of the sys\_user, sys\_user\_group, and sys\_user\_role ACLs. For more information, see [Access control list rules](https://www.servicenow.com/docs/access?context=access-control-rules&version=australia&pubname=australia-platform-security&ft:locale=en-US).

 There is a performance penalty associated with enabling this property. Performance degradation may be based on the number and complexity of business rules and ACLs on your instance.

</td></tr><tr><td>

Specify a comma-separated list of roles that can share their own dashboards.

glide.cms.share\_dashboards.role

</td><td>

-   Type: string
-   Default value: Empty

When this property is empty, all users can share their own dashboards.

-   Location: **System Properties** &gt; **Dashboard Properties**

 **Note:** Properties that restrict dashboard sharing do not apply to users with the admin and dashboard\_admin roles. Users with these two roles can always share any dashboard.

</td></tr><tr><td>

Maximum number of seconds for a widget to render on a responsive dashboard.

glide.canvas.grid.widget\_performance\_threshold

</td><td>

-   Type: integer
-   Default value: none
-   Location: **System Properties** &gt; **Dashboard Properties**

 For more information, see [Optimize widget rendering time on responsive dashboards](../task/t_optimizeWidgetRenderingTime.md).

</td></tr><tr><td>

Maximum number of widgets that can render simultaneously on a responsive dashboard.

glide.canvas.grid.widget\_render\_concurrent\_max

</td><td>

-   Type: integer
-   Default value: 3
-   Location: **System Properties** &gt; **Dashboard Properties**

 For more information, see [Optimize widget rendering time on responsive dashboards](../task/t_optimizeWidgetRenderingTime.md).

</td></tr><tr><td>

Number of seconds that responsive dashboard widgets are cached in the browser.

glide.canvas.grid.widget\_cache\_ttl

</td><td>

-   Type: integer
-   Default value: 2
-   Location: **System Properties** &gt; **Dashboard Properties**

</td></tr><tr><td>

Number of users, groups, and roles returned when searching for a name in the Share panel of a Responsive Dashboard.The value of this property is per category, so the default value of 100 may yield 300 results - 100 users, 100 groups, and 100 roles.

glide.cms.dashboards.sharing.search.maxRecords

</td><td>

-   Type: integer
-   Default value: 100
-   Location: sys\_properties.list

 Setting the value too low can cause the expected results not to be found. The minimum value is 5. Setting the value too high can cause performance issues.

</td></tr></tbody>
</table>