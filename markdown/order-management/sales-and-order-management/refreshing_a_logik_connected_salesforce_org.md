---
title: Refreshing a ServiceNow CPQ connected Salesforce org
description: Refreshing a Salesforce org severs the database sync between ServiceNow CPQ and Salesforce. To get things working again, take these steps after the refresh.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [ServiceNow CPQ integration with Salesforce B2B Commerce, ServiceNow CPQ with other apps, Integrate, Sales Customer Relationship Management]
---

# Refreshing a ServiceNow CPQ connected Salesforce org

Refreshing a Salesforce org severs the database sync between ServiceNow CPQ and Salesforce. To get things working again, take these steps after the refresh.

When a ServiceNow CPQ connected Salesforce org is refreshed, the database sync between ServiceNow CPQ and Salesforce will be temporarily broken. This is because a refresh automatically changes many pieces of the Salesforce org, including the Salesforce org ID, product IDs, and user names.

These ID changes are used for many integration points between the two systems, such as the Refresh Token User Runtime APIs that depend on a User ID, the product, the Pricebook, Pricebook entry sync, and the user access set up for the ServiceNow CPQ Admin.

To complete the ServiceNow CPQ side of the refresh, create a Support case. Provide the following information:

-   The current ServiceNow CPQ Environment URL
-   The date the refresh will be performed
-   What you'd like to do with the connected ServiceNow CPQ environment's existing data:
    -   Retain its data \(a repoint\)
    -   Start from scratch \(decommission and create a new environment\)
-   The new SFDC org ID \(if unknown at the time, simply give TBD\)
-   The SFDC My Domain URL \(if changed\)
-   The SFDC Usernames for users that will need ServiceNow CPQ Admin access
-   Whether you want to change the ServiceNow CPQ environment host name, and if so, what it should be
-   The provisioning username with the email address of [provisioning@logik.io](mailto:provisioning@logik.io) and system administrator privileges.

Once the environment is refreshed, you will need to:

-   Send the new SFDC org ID
-   Navigate to Salesforce Setup &gt; Custom Settings &gt; Manage Logik tenant and modify the ServiceNow CPQ URLs.

    Navigate to SFDC &gt; Setup &gt; Custom Settings &gt; Manage ServiceNow CPQ Tenant &gt; Edit, and change the Runtime Configuration URL and Administration URL.

-   If using Salesforce CPQ, change the external configurator URL.

    Navigate to SFDC &gt; Setup &gt; Installed Packages &gt; Configure Salesforce CPQ &gt; Additional Settings, and change the external configurator URL to the new site with `/ui/configure` appended to the end.

-   Submit a new refresh token user name with system administrator permissions.

    Navigate to ServiceNow CPQ Admin &gt; Settings, and delete or reset Refresh Token Username.

-   If using any Runtime APIs in SFDC, create new Runtime Clients.

    Navigate to ServiceNow CPQ Admin &gt; Runtime Clients, and create the new clients.


