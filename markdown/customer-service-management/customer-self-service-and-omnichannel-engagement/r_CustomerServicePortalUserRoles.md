---
title: Customer Service Portal user roles
description: Several different roles allow customers to create and edit cases and manage users from the customer portal.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure the Customer and Consumer Service Portals, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Customer Service Portal user roles

Several different roles allow customers to create and edit cases and manage users from the customer portal.

<table id="table_g4p_jyh_ts"><thead><tr><th>

User role

</th><th>

What this user can do on the Customer Service Portal

</th></tr></thead><tbody><tr><td>

Customer\[sn\_customerservice.customer\]

</td><td>

-   Create a case for this user's account.
-   View a list of cases created by this user.
-   Edit cases created by this user.
-   View a list of assets belonging to this user's account.
-   Search for information.

</td></tr><tr><td>

Customer case manager \[sn\_customerservice.customer\_case\_manager\]

</td><td>

-   Create a case for this user's account and for child accounts.
-   View a list of cases created by this user and view cases for child accounts.
-   Edit cases created by this user and edit cases for child accounts.
-   View a list of assets belonging to this user's account and to child accounts.
-   Search for information.
-   Create a case on behalf of another contact in this account.
-   View a list of cases belonging to this account.
-   Edit cases belonging to the account.

 **Note:** The customer case manager role is not automatically added to the **sn\_customerservice.contact\_role\_assignment** system property. To expose this role to customer and partner administrators, navigate to **Customer Service** &gt; **Administration** &gt; **Properties** and add it to this property.

</td></tr><tr><td>

Customer administrator \[sn\_customerservice.customer\_admin\]

</td><td>

-   Create a case for this user's account.
-   Create a case on behalf of another contact for this account.
-   View a list of cases belonging to this account.
-   Edit cases belonging to this account.
-   View a list of assets belong to this user's account.
-   Search for information.
-   Manage users for this account.

</td></tr><tr><td>

Partner\[sn\_customerservice.partner\]

</td><td>

-   Create a case for this user's account.
-   Create a case on behalf of customer accounts.
-   View a list of cases belonging to this user.
-   Edit cases belonging to this user.
-   View a list of assets belong to this user's account.
-   Search for information.

</td></tr><tr><td>

Partner administrator \[sn\_customerservice.partner\_admin\]

</td><td>

-   Create a case for this user's account.
-   Create a case on behalf of customer accounts.
-   View a list of cases belonging to this account and to customer accounts.
-   View a list of assets belong to this account and to customer accounts.
-   Edit cases belonging to this account and to customer accounts.
-   Manage users for this account and for customer accounts.

</td></tr></tbody>
</table>