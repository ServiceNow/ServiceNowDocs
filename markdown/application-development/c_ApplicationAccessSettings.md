---
title: Application access settings
description: Application access settings determine whether one application can access resources from another application.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application access settings

Application access settings determine whether one application can access resources from another application.

Application access settings are similar to access controls \(ACLs\) in that they allow you to restrict access to certain resources, but instead of restricting tables and records from users they restrict applications resources from other applications. There are several ways to set cross-scope access.

<table id="table_cxq_1b5_n1b"><thead><tr><th>

Setting type

</th><th>

Use

</th><th>

Description

</th><th>

Access setting location

</th></tr></thead><tbody><tr><td>

[Application design and runtime settings](../reference/r_ApplicationDesignAndRuntimeSettings.md)

</td><td>

Your application or application script requires access to a cross-scope resource.

</td><td>

Application designers can configure the following application access settings for the entire application.

-   Specify whether cross-scope tables can be selected during design-time activities.
-   Specify when scripts can run on cross-scope resources.
-   Specify what JavaScript standard the application supports.

</td><td>

Access determined by the cross-scope privilege record owned by the calling application.

</td></tr><tr><td>

[Table design and runtime settings](../reference/r_TableApplicationAccessFields.md)

</td><td>

A cross-scope application or web service requires access to perform CRUD operations on a table.

</td><td>

Application developers can also configure application access settings for individual tables.

-   Specify whether the table is available to other application scopes.
-   Specify what runtime operations from other application scopes the table supports.
-   Specify whether the table can be selected during design-time activities.
-   Specify whether the table can be accessed from web services.

</td><td>

Access determined by settings on the target table.

</td></tr><tr><td>

[Restricted caller access privilege settings](restricted-caller-access-privilege.md)

</td><td>

A cross-scope application or script requires access to your application or application resource.

</td><td>

Admin users can configure the following application access settings for an entire application scope or application resource.

-   Specify whether a cross-scope script can access your application scope or an application resource.
-   Track cross-scope requests for access to application resources.
-   Approve or deny cross-scope requests to access application resources.

</td><td>

Access determined by the restricted caller access record owned by the target application.

</td></tr></tbody>
</table>