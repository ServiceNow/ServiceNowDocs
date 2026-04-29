---
title: Install the Chief Human Resources Officer Dashboard
description: The CHRO Dashboard helps people leadership to run its business to deliver value quickly, improve productivity and optimize risks.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Human Resources Officer \(CHRO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Install the Chief Human Resources Officer Dashboard

The CHRO Dashboard helps people leadership to run its business to deliver value quickly, improve productivity and optimize risks.

## Before you begin

Role required: admin, platform\_analytics\_admin, chro\_dashboard\_admin

**Note:** The CHRO Dashboard application is free from the ServiceNow Store. However, the contents of the dashboard require a professional entitlement to the HRSD \(com.sn\_hr\_core\) application. This professional entitlement includes a license for Platform Analytics and the content pack solutions for the associated applications.

These solutions consist of Platform Analytics indicators and associated data collection jobs, used by the metrics on the CHRO Dashboard. If you don’t have the prerequisite licenses, the installation proceeds. However, without the required plugins \(found in the application manager\) and applications \(found in the ServiceNow store\) and the underlying data, the dashboard won’t show any relevant metrics. If you have any questions about your licensing and entitlements, consult your account executive.

Plugins:

-   sn\_hr\_er\_pa
-   sn\_hr\_le\_pa
-   sn\_hr\_pa

## Procedure

1.  Log in to `https://store.servicenow.com`.

2.  Search for the CHRO Dashboard application.

3.  Select the **Request Install** button to create the app installation request.

    Select **Request** to request the CHRO Dashboard application plugin for the specified instance and provide the instance details with your reason for request and validate the instance.

4.  Navigate to **System applications** &gt; **All available applications**.

5.  Search for and install the CHRO Dashboard plugin \(sn\_chro\_dashboard\).

6.  Assign roles to configure and view the CHRO Dashboard.

    -   **CHRO Dashboard admin**

        Assign the role sn\_chro\_dashboard.chro\_dashboard\_admin to users or groups who require configuration privileges on the dashboard.

        **Note:** Only users with this role are able to configure the CHRO dashboard.

    -   **CxO Dashboard end users**

        Assign the user role sn\_chro\_dashboard.chro\_dashboard\_user to users or groups who must view the dashboard.

    Users must log out and log back in to enable their new roles after the admin assigns them. For more information on user roles, see [Exploring user administration](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).


