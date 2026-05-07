---
title: Granting user access in CPQ
description: This outline briefly examines how to add or limit users to CPQ.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Granting user access in CPQ

This outline briefly examines how to add or limit users to CPQ.

User management takes different forms, depending upon the implementation scenario.

## CPQ is integrated with Salesforce CPQ

To add users, in Salesforce Admin, go to Setup, go to Manage Connected Apps, and then go to Logik Connected App.

-   In the OAuth Policies section, confirm that Permitted Users input is set to **Admin approved users are pre-authorized**.
-   In the Profiles section, click **Manage Profiles**. Select the checkboxes that correspond to the profiles you want to enable, and save.
-   To assign specific permission sets access to the Logik Connected App, click **Manage Permission Sets**. Select the check boxes that correspond to the permission sets to enable, and save.
-   New admin users must first access the CPQ Admin. Their admin access can then be toggled on by another admin user in the User Access section of Utilities. For more information, see [User access](please_share_your_feedback_on_admin_assist_responses.md)

To limit prevent certain profiles from accessing CPQ Admin, in Salesforce Admin, go to Setup, go to Object Manager, Product, and then Fields &amp; Relationships. Click the **View Logik Setup \(LGK\_\_ViewConfigurationSetup\_\_c\)** field, and then click **Set Field-Level Security**.

-   Deselect the check boxes for the profiles you do not wish to enter.
-   Admin users can also toggle user access in the CPQ Admin, in the User Access section of Utilities. Any sales users can have their admin access toggled off by selecting their name and clicking **Toggle Admin Access** in the upper right. If users have only END\_USER assigned to their user, they cannot access the CPQ Admin.

## CPQ is implemented headless \(outside of a SFDC org\)

When using a custom UI \(such as React\) that calls CPQ APIs, CPQ leverages your third-party IDP, such as Google or Salesforce. To add administration users, log a Support case. Include the name of the IDP and domain your company is using together with the first names, last names, and email addresses of the new users.

## Additional permissions to check

[Assigning non-Admin user permissions for CPQ in Salesforce](non-admin_user_permissions_for_logik_in_salesforce.md)

[What to do if receiving and Insufficient Privileges or blank screen when launching a CPQ configuration](https://logikio.atlassian.net/wiki/spaces/CS/pages/1616314402/What+to+do+if+receiving+and+Insufficient+Privileges+or+blank+screen+when+launching+a+Logik+configuration#reverse_twin_productlist.extended_data_to_quoteline/bookmark4)

**Related topics**  


[CPQ: User Access Control](logik_admin_user_access_control.md)

