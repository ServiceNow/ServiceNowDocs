---
title: User Experience Analytics roles
description: Designate people in your organization to use and configure User Experience Analytics for Service Portal.
locale: en-US
release: xanadu
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [User Experience Analytics for Service Portal, Analytics and Reporting Solutions for Service Portal, Using portal analytics, Service Portal, Configure UIs and portals, Configure user experiences]
---

# User Experience Analytics roles

Designate people in your organization to use and configure User Experience Analytics for Service Portal.

The portal\_analytics\_admin and portal\_analytics\_viewer roles are installed with the Service Portal Analytics plugin \(com.glide.service-portal.analytics\).

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

User Experience Analytics Admin\[analytics\_admin\]

</td><td>

Administrators:-   can view the **Dashboard** link and settings within User Experience Analytics in the application navigator.
-   can control the User Experience Analytics settings for each mobile application and portal.
-   have **admin** role permissions to be able to create funnel and cohort reports from the User Experience Analytics Dashboard.

</td><td>

-   web\_analytics\_admin
-   mobile\_analytics\_admin
-   analytics\_viewer

</td></tr><tr><td>

User Experience Analytics Viewer\[analytics\_viewer\]

</td><td>

Users with this role can view the **Dashboard** link within User Experience Analytics in the application navigator, and have viewer role permissions for User Experience Analytics.

</td><td>

-   web\_analytics\_viewer
-   mobile\_analytics\_viewer

</td></tr><tr><td>

Mobile Analytics Admin\[mobile\_analytics\_admin\]

</td><td>

Administrators:-   can view the **Analytics Dashboard** link and settings within Mobile Analytics in the application navigator.
-   can control the Mobile Analytics settings for each mobile application.
-   have **admin** role permissions to be able to create funnel and cohort reports from the Analytics Dashboard.

</td><td>

mobile\_analytics\_viewer

</td></tr><tr><td>

Mobile Analytics Viewer\[mobile\_analytics\_viewer\]

</td><td>

Users with this role can view the **Analytics Dashboard** link within Mobile Analytics in the application navigator, and have viewer role permissions for Mobile Analytics.

</td><td>

None

</td></tr><tr><td>

Web Analytics Admin\[web\_analytics\_admin\]

</td><td>

Administrators:-   can view the **Analytics Dashboard** link and settings within User Experience Analytics in the application navigator.
-   can control the User Experience Analytics settings for each web application.
-   have **admin** role permissions to be able to create funnel and cohort reports from the Analytics Dashboard.

</td><td>

-   web\_analytics\_viewer
-   portal\_analytics\_admin

</td></tr><tr><td>

Web Analytics Viewer\[web\_analytics\_viewer\]

</td><td>

Users with this role can view the **Analytics Dashboard** link within User Experience Analytics in the application navigator, and have viewer role permissions for web application analytics.

</td><td>

portal\_analytics\_viewer

</td></tr><tr><td>

Portal Analytics Admin\[portal\_analytics\_admin\]

</td><td>

Administrators:-   can view the **Analytics Dashboard** link and settings within **Service Portal** &gt; **Analytics** in the application navigator.
-   can create User Experience Analytics settings for Service Portal.

</td><td>

portal\_analytics\_viewer

</td></tr><tr><td>

Portal Analytics Viewer\[portal\_analytics\_viewer\]

</td><td>

Users with this role can view the **Analytics Dashboard** link and settings within **Service Portal** &gt; **Analytics** in the application navigator, and have viewer role permissions for portal metrics in the User Experience Analytics Dashboard.

</td><td>

None

</td></tr></tbody>
</table>**Parent Topic:**[User Experience Analytics for Service Portal](../concept/sp-analytics.md)

