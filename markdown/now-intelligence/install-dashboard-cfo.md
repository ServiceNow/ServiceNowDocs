---
title: Install the Chief Financial Officer \(CFO\) Dashboard
description: The Chief Financial Officer \(CFO\) Dashboard provides a unified, real-time view of enterprise financial performance across key dimensions such as portfolio health, software investments, procurement efficiency, and audit and risk management.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-18"
reading_time_minutes: 1
breadcrumb: [Chief Financial Officer \(CFO\) Dashboard, Executive dashboard overview, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Install the Chief Financial Officer \(CFO\) Dashboard

The Chief Financial Officer \(CFO\) Dashboard provides a unified, real-time view of enterprise financial performance across key dimensions such as portfolio health, software investments, procurement efficiency, and audit and risk management.

## Before you begin

Roles required: sn\_cfo\_dashboard.admin, sn\_cfo\_dashboard.user

**Note:** The CFO Dashboard application is free from the ServiceNow Store. However, the contents of the dashboard require professional entitlements to the following applications:

-   Performance Analytics - Content Pack - PPM Standard
-   Performance Analytics – Software Asset Management Professional
-   Performance Analytics for Sourcing and Procurement Operations
-   GRC: Advanced Risk

These professional entitlements include a license for Platform Analytics.

These solutions consist of Platform Analytics indicators and associated data collection jobs, used by the metrics on the Chief Financial Officer Dashboard. If you don’t have the prerequisite licenses, the installation proceeds. However, without the required plugins \(found in the application manager\) and applications \(found in the ServiceNow store\) and the underlying data, the dashboard won’t show any relevant metrics. If you have any questions about your licensing and entitlements, consult your account executive.

Plugins:

-   com.snc.pa.pmo\_dashboards
-   sn\_pa\_samp
-   sn\_spend\_pa
-   sn\_risk\_advanced

## Procedure

1.  Log in to `https://store.servicenow.com`.

2.  Search for the CFO Dashboard application.

3.  Select the **Request Install** button to create the app installation request.

    Select **Request** to request the CFO Dashboard application plugin for the specified instance and provide the instance details with your reason for request and validate the instance.

    ![](../image/cxo-request-install.png)

4.  Navigate to **System applications** &gt; **All available applications**.

5.  Search for and install the CFO Dashboard plugin \(sn\_cfodashboard\).

6.  Assign roles to configure and view the CFO Dashboard.

    -   **CFO Dashboard admin**

        Assign the role sn\_cfo\_dashboard.admin to users or groups who require configuration privileges on the dashboard.

        **Note:** Only users with this role are able to configure the CFO dashboard.

    -   **CFO Dashboard end users**

        Assign the user role sn\_cfo\_dashboard.user to users or groups who must view the dashboard.

    Users must log out and log back in to enable their new roles after the admin assigns them. For more information on user roles, see [Exploring user administration](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


