---
title: Install the Chief Customer Operations Officer Dashboard
description: The Chief customer Operations Officer Dashboard provides the visibility into customer support and operations that helps leadership to fine tune the operations for effectiveness.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-08-18"
reading_time_minutes: 1
breadcrumb: [Chief Customer Operations Officer \(CCO\) Dashboard, Executive dashboard overview, Dashboards, Platform Analytics experience, Platform Analytics]
---

# Install the Chief Customer Operations Officer Dashboard

The Chief customer Operations Officer Dashboard provides the visibility into customer support and operations that helps leadership to fine tune the operations for effectiveness.

## Before you begin

Role required: sn\_cco\_dashboard.cco\_dashboard\_admin, sn\_cco\_dashboard.cco\_dashboard\_user

**Note:** The CCO Dashboard application is free from the ServiceNow Store. However, the contents of the dashboard require professional entitlements to the following applications: Customer Service Management.These professional entitlements include a license for Platform Analytics.

These solutions consist of Platform Analytics indicators and associated data collection jobs, used by the metrics on the CCO Dashboard. If you don’t have the prerequisite licenses, the installation proceeds. However, without the required plugins \(found in the application manager\) and applications \(found in the ServiceNow store\) and the underlying data, the dashboard won’t show any relevant metrics. If you have any questions about your licensing and entitlements, consult your account executive.

Application plugins:

-   com.sn\_customerservice
-   com.snc.pa.customer\_service\_advanced
-   com.snc.proactive\_cs\_ops
-   com.snc.self\_service\_analytics\_core
-   com.snc.pa.self\_service\_analytics\_csm
-   com.sn\_communities
-   com.glide.cs.chatbot

## Procedure

1.  Log in to `https://store.servicenow.com`.

2.  Search for the CCO Dashboard application.

3.  Select the **Request Install** button to create the app installation request.

    Select **Request** to request the CCO Dashboard application plugin for the specified instance and provide the instance details with your reason for request and validate the instance.

    ![](../image/cxo-request-install.png)

4.  Navigate to **System applications** &gt; **All available applications**.

5.  Search for and install the CCO Dashboard plugin \(sn\_cco\_dashboard\).

6.  Assign roles to configure and view the CCO Dashboard.

    -   **CCO Dashboard admin**

        Assign the role sn\_cco\_dashboard.cco\_dashboard\_admin to users or groups who require configuration privileges on the dashboard.

        **Note:** Only users with this role are able to configure the CCO dashboard.

    -   **CCO Dashboard end users**

        Assign the user role sn\_cco\_dashboard.cco\_dashboard\_user to users or groups who must view the dashboard.

    Users must log out and log back in to enable their new roles after the admin assigns them. For more information on user roles, see [Exploring user administration](https://www.servicenow.com/docs/access?context=exploring-user-administration&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).


