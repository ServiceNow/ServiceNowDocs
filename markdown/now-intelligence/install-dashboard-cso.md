---
title: Install the Chief Information Security Officer Dashboard
description: The Chief Information Security Officer \(CISO\) Dashboard provides a single pane glass view of end-to-end security operations.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Information Security Officer \(CISO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Install the Chief Information Security Officer Dashboard

The Chief Information Security Officer \(CISO\) Dashboard provides a single pane glass view of end-to-end security operations.

## Before you begin

Role required: admin, platform\_analytics\_admin, sn\_ciso\_dashboard.admin

**Note:** The CISO Dashboard application is free from the ServiceNow Store. However, the contents of the dashboard require professional entitlements to the following applications:

-   Security Operations \(SecOps\)
-   Governance, Risk, and Compliance \(GRC\)

These professional entitlements include a license for Platform Analytics.

These solutions consist of Platform Analytics indicators and associated data collection jobs, used by the metrics on the CISO Dashboard. If you don’t have the prerequisite licenses, the installation proceeds. However, without the required plugins \(found in the application manager\) and applications \(found in the ServiceNow store\) and the underlying data, the dashboard won’t show any relevant metrics. If you have any questions about your licensing and entitlements, consult your account executive.

Plugin: com.snc.vulnerability.analytics.

Applications:

-   sn\_sir\_analytics
-   sn\_vul\_analytics
-   sn\_grc\_pa\_advanced
-   sn\_vulc\_analytics

## Procedure

1.  Log in to `https://store.servicenow.com`.

2.  Search for the CISO Dashboard application.

3.  Select the **Request Install** button to create the app installation request.

    Select **Request** to request the CISO Dashboard application plugin for the specified instance and provide the instance details with your reason for request and validate the instance.

4.  Navigate to **System applications** &gt; **All available applications**.

5.  Search for and install the CISO Dashboard plugin \(sn\_cisodashboard\).

6.  Assign roles to configure and view the CISO Dashboard.

    -   **CISO Dashboard admin**

        Assign the role sn\_ciso\_dashboard.admin to users or groups who require configuration privileges on the dashboard.

        **Note:** Only users with this role are able to configure the CISO dashboard.

    -   **CISO Dashboard end users**

        Assign the user role sn\_ciso\_dashboard.user to users or groups who must view the dashboard.

    -   **Viewer**

        Assign the pa\_viewer role to those who need to view Performance Analytics scores.

    Users must log out and log back in to enable their new roles after the admin assigns them. For more information on user roles, see [Exploring user administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/exploring-user-administration.md).


