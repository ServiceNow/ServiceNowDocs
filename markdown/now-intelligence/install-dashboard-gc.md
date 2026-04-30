---
title: Install the General Counsel \(GC\) Dashboard
description: For a general counsel, this dashboard provides transparency into legal service delivery and operations.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-18"
reading_time_minutes: 1
breadcrumb: [General Counsel \(GC\) Dashboard, Executive dashboard overview, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Install the General Counsel \(GC\) Dashboard

For a general counsel, this dashboard provides transparency into legal service delivery and operations.

## Before you begin

Role required: sn\_lsd\_dashboard.gc\_dashboard\_admin, sn\_lsd\_dashboard.gc\_dashboard\_user

**Note:** The General Counsel Dashboard application is free from the ServiceNow Store. However, the contents of the dashboard require professional entitlements to the following applications: Legal Services Delivery. This application includes a license for Platform Analytics.

These solutions consist of Platform Analytics indicators and associated data collection jobs, used by the metrics on the GC Dashboard. If you don’t have the prerequisite licenses, the installation proceeds. However, without the required plugins \(found in the application manager\) and applications \(found in the ServiceNow store\) and the underlying data, the dashboard won’t show any relevant metrics. If you have any questions about your licensing and entitlements, consult your account executive.

Application plugins:

-   sn\_lg\_ops
-   sn\_lg\_matter
-   sn\_lg\_lpa\_core
-   sn\_lg\_pa
-   sn\_lg\_contracts
-   sn\_lg\_coi
-   sn\_lg\_forensics

## Procedure

1.  Log in to `https://store.servicenow.com`.

2.  Search for the GC Dashboard application.

3.  Select the **Request Install** button to create the app installation request.

    Select **Request** to request the GC Dashboard application plugin for the specified instance and provide the instance details with your reason for request and validate the instance.

    ![](../image/cxo-request-install.png)

4.  Navigate to **System applications** &gt; **All available applications**.

5.  Search for and install the GC Dashboard plugin \(sn\_lsd\_dashboard\).

6.  Assign roles to configure and view the GC Dashboard.

    -   **GC Dashboard admin**

        Assign the role sn\_lsd\_dashboard.gc\_dashboard\_admin to users or groups who require configuration privileges on the dashboard.

        **Note:** Only users with this role are able to configure the GC dashboard.

    -   **GC Dashboard end users**

        Assign the user role sn\_lsd\_dashboard.gc\_dashboard\_user to users or groups who must view the dashboard.

    Users must log out and log back in to enable their new roles after the admin assigns them. For more information on user roles, see [Exploring user administration](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


