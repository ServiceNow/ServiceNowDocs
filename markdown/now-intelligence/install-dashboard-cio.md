---
title: Install the CIO Dashboard
description: The Chief Information Officer \(CIO\) Dashboard provides a decision-making framework for key decisions, critical questions, and the insights to stay on course and scale your business.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Information Officer \(CIO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Install the CIO Dashboard

The Chief Information Officer \(CIO\) Dashboard provides a decision-making framework for key decisions, critical questions, and the insights to stay on course and scale your business.

## Before you begin

Role required: admin, platform\_analytics\_admin, cio\_dashboard\_admin

**Note:** The CIO Dashboard application is free from the ServiceNow Store. However, the contents of the dashboard require professional entitlements to the following applications:

-   IT Service Management
-   IT Operations Management
-   IT Asset Management
-   Security Operations \(SecOps\)
-   Strategic Portfolio Management \(SPM\)

These professional entitlements include a license for Platform Analytics.

These solutions consist of Platform Analytics indicators and associated data collection jobs, used by the metrics on the CIO Dashboard. If you don’t have the prerequisite licenses, the installation proceeds. However, without the required plugins \(found in the application manager\) and applications \(found in the ServiceNow store\) and the underlying data, the dashboard won’t show any relevant metrics. If you have any questions about your licensing and entitlements, consult your account executive.

Plugins:

-   com.snc.pa.cmdb
-   com.snc.pa.slacom.snc.pa
-   com.snc.pa.itsm\_dashboards
-   com.snc.pa.sla
-   com.snc.pa.request
-   com.snc.pa.change
-   com.snc.pa.premium.sam
-   com.snc.pa.pmo\_dashboards
-   com.snc.pa.self\_service\_analytics
-   com.sn\_communities
-   com.snc.pa.request2

Applications:

-   sn\_sir\_analytics
-   sn\_vul\_analytics
-   sn\_compliance
-   sn\_ppm\_imd

## Procedure

1.  Log in to `https://store.servicenow.com`.

2.  Search for the CIO Dashboard application.

3.  Select the **Request Install** button to create the app installation request.

    Select **Request** to request the CIO Dashboard application plugin for the specified instance and provide the instance details with your reason for request and validate the instance.

4.  Navigate to **System applications** &gt; **All available applications**.

5.  Search for and install the CIO Dashboard plugin \(sn\_ciodashboard\).

6.  Assign roles to configure and view the CIO Dashboard.

    -   **CIO Dashboard admin**

        Assign the role sn\_ciodashboard.ciodashboard\_admin to users or groups who require configuration privileges on the dashboard.

        **Note:** Only users with this role can configure the CIO Dashboard.

    -   **CIO Dashboard end users**

        Assign the user role sn\_ciodashboard.ciodashboard\_user to users or groups who must view the dashboard.

    Users must log out and log back in to enable their new roles after the admin assigns them. For more information on user roles, see [Exploring user administration](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


