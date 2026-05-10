---
title: Install the Chief Procurement Officer Dashboard
description: The Chief Procurement Officer Dashboard provides key insights around the procurement process of your organization.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chief Procurement Officer \(CPRO\) Dashboard, Executive dashboard overview, Platform Analytics]
---

# Install the Chief Procurement Officer Dashboard

The Chief Procurement Officer Dashboard provides key insights around the procurement process of your organization.

## Before you begin

Role required: admin, platform\_analytics\_admin, sn\_cpro\_dashboard.admin

**Note:** The CPRO Dashboard application is free from the ServiceNow Store. However, the contents of the dashboard require professional entitlements to the following applications:

-   Performance Analytics Content Pack for Procurement Service Management
-   Purchase Automation Integration with Risk Assessment
-   Procurement Case Management
-   Procurement Specialist Workspace
-   Procurement Integration Framework
-   Finance Common Architecture
-   Service Delivery Common
-   Purchase Modification Experience Pack for Procurement Case Management
-   Sourcing and Purchasing Automation
-   Virtual Agent Experience Pack for Procurement Service Management
-   Procurement Common Architecture
-   Procurement with Project Management
-   ShoppingHub Mobile
-   Finance - ERP Integration
-   Procurement File Transfer Framework
-   Procurement Service Management NLU Model

These professional entitlements include a license for Platform Analytics.

These solutions consist of Platform Analytics indicators and associated data collection jobs, used by the metrics on the CPRO Dashboard. If you don’t have the prerequisite licenses, the installation proceeds. However, without the required plugins \(found in the application manager\) and applications \(found in the ServiceNow store\) and the underlying data, the dashboard won’t show any relevant metrics. If you have any questions about your licensing and entitlements, consult your account executive.

## Procedure

1.  Log in to `https://store.servicenow.com`.

2.  Search for the CPRO Dashboard application.

3.  Select the **Request Install** button to create the app installation request.

    Select **Request** to request the CPRO Dashboard application plugin for the specified instance and provide the instance details with your reason for request and validate the instance.

4.  Navigate to **System applications** &gt; **All available applications**.

5.  Search for and install the CPRO Dashboard plugin \(sn\_cpro\_dashboard\).

6.  Assign roles to configure and view the CPRO Dashboard.

    -   **CPRO Dashboard admin**

        Assign the role sn\_cpro\_dashboard.admin to users or groups who require configuration privileges on the dashboard.

        **Note:** Only users with this role are able to configure the CPRO dashboard.

    -   **CPRO Dashboard end users**

        Assign the user role sn\_cpro\_dashboard.user to users or groups who must view the dashboard.

    Users must log out and log back in to enable their new roles after the admin assigns them. For more information on user roles, see [Exploring user administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/exploring-user-administration.md).


