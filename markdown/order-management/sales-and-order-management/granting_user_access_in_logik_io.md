---
title: Granting user access in ServiceNow CPQ
description: This outline briefly examines how to add or limit users to ServiceNow CPQ.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Granting user access in ServiceNow CPQ

This outline briefly examines how to add or limit users to ServiceNow CPQ.

User management takes different forms, depending upon the implementation scenario.

## ServiceNow CPQ is integrated with Salesforce CPQ

To add users, in Salesforce Admin, go to Setup, go to Manage Connected Apps, and then go to Logik Connected App.

-   In the OAuth Policies section, confirm that Permitted Users input is set to **Admin approved users are pre-authorized**.
-   In the Profiles section, click **Manage Profiles**. Select the checkboxes that correspond to the profiles you want to enable, and save.
-   To assign specific permission sets access to the Logik Connected App, click **Manage Permission Sets**. Select the check boxes that correspond to the permission sets to enable, and save.
-   New admin users must first access the ServiceNow CPQ Admin. Their admin access can then be toggled on by another admin user in the User Access section of Utilities. For more information, see [User access](please_share_your_feedback_on_admin_assist_responses.md)

To limit prevent certain profiles from accessing ServiceNow CPQ Admin, in Salesforce Admin, go to Setup, go to Object Manager, Product, and then Fields &amp; Relationships. Click the **View Logik Setup \(LGK\_\_ViewConfigurationSetup\_\_c\)** field, and then click **Set Field-Level Security**.

-   Deselect the check boxes for the profiles you do not wish to enter.
-   Admin users can also toggle user access in the ServiceNow CPQ Admin, in the User Access section of Utilities. Any sales users can have their admin access toggled off by selecting their name and clicking **Toggle Admin Access** in the upper right. If users have only END\_USER assigned to their user, they cannot access the ServiceNow CPQ Admin.

## ServiceNow CPQ is implemented headless \(outside of a SFDC org\)

When using a custom UI \(such as React\) that calls ServiceNow CPQ APIs, ServiceNow CPQ leverages your third-party IDP, such as Google or Salesforce. To add administration users, log a Support case. Include the name of the IDP and domain your company is using together with the first names, last names, and email addresses of the new users.

## Additional permissions to check

[Assigning non-Admin user permissions for ServiceNow CPQ in Salesforce](non-admin_user_permissions_for_logik_in_salesforce.md)

[What to do if receiving and Insufficient Privileges or blank screen when launching a ServiceNow CPQ configuration](https://logikio.atlassian.net/wiki/spaces/CS/pages/1616314402/What+to+do+if+receiving+and+Insufficient+Privileges+or+blank+screen+when+launching+a+Logik+configuration#reverse_twin_productlist.extended_data_to_quoteline/bookmark4)

**Related topics**  


[ServiceNow CPQ: User Access Control](logik_admin_user_access_control.md)

