---
title: Install the CDO Dashboard
description: The Chief Digital Officer \(CDO\) Dashboard provides ...
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Digital Officer \(CDO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Install the CDO Dashboard

The Chief Digital Officer \(CDO\) Dashboard provides ...

## Before you begin

Role required: admin, platform\_analytics\_admin, cdo\_dashboard\_admin

**Note:** The CDO Dashboard application is free from the ServiceNow Store. However, the contents of the dashboard require professional entitlements to the following applications: IT Service Management. This professional entitlement includes a license for Platform Analytics.

These solutions consist of Platform Analytics indicators and associated data collection jobs, used by the metrics on the CDO Dashboard. If you don’t have the prerequisite licenses, the installation proceeds. However, without the required plugins \(found in the application manager\) and applications \(found in the ServiceNow store\) and the underlying data, the dashboard won’t show any relevant metrics. If you have any questions about your licensing and entitlements, consult your account executive.

In addition, the com.snc.pa.premium.all\_content application plugin is required from the professional license.

## Procedure

1.  Log in to `https://store.servicenow.com`.

2.  Search for the CDO Dashboard application.

3.  Select the **Request Install** button to create the app installation request.

    Select **Request** to request the CDO Dashboard application plugin for the specified instance and provide the instance details with your reason for request and validate the instance.

4.  Navigate to **System applications** &gt; **All available applications**.

5.  Search for and install the CDO Dashboard plugin \(sn\_cdo\_dashboard\).

6.  Assign roles to configure and view the CDO Dashboard.

    -   **CDO Dashboard admin**

        Assign the role sn\_cdodashboard.cdo\_dashboard\_admin to users or groups who require configuration privileges on the dashboard.

        **Note:** Only users with this role are able to configure the CDO dashboard.

    -   **CDO Dashboard end users**

        Assign the user role sn\_cdodashboard.cdo\_dashboard\_user to users or groups who must view the dashboard.

    Users must log out and log back in to enable their new roles after the admin assigns them. For more information on user roles, see [Exploring user administration](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


