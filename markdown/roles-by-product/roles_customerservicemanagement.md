---
title: Customer Service Management roles
description: These roles are available for the application
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/roles-by-product/roles\_customerservicemanagement.html
release: australia
topic_type: reference
last_updated: "2024-03-11"
reading_time_minutes: 5
breadcrumb: [Roles for all products]
---

# Customer Service Management roles

These roles are available for the application

<table><thead><tr><th>

Role

</th><th>

Description

</th><th>

Contains roles

</th><th>

Groups with this role

</th><th>

Special considerations

</th></tr></thead><tbody><tr><td>

Consumer \[sn\_customerservice.consumersn\_customerservice.consumer\]

</td><td>

Assign this Consumer role to users for researching questions, issues, or problems.

</td><td>

-   sn\_esm\_user
-   snc\_external

</td><td>

All users with the assigned Consumer role.

</td><td>

Consumers can create cases and view and edit existing cases for products that they have purchased. They can also view a list of their products. For more information see .

</td></tr><tr><td>

Consumer service agent \[sn\_customerservice.consumer\_agent\]

</td><td>

Use this role to create cases, view and edit cases, and work with customers and subject matter experts to resolve cases. This role helps agents assist consumers with questions, issues, and problems.

</td><td>

-   sn\_esm\_agent
-   chat\_admin
-   sn\_shn.editor
-   template\_editor
-   knowledge

</td><td>

All consumer service agents.

</td><td>

**Note:** A consumer service agent typically supports a specific set of products across one or more communication channels. An agent can belong to one or more agent groups.

For more information see .

</td></tr><tr><td>

Customer \[sn\_customerservice.customer\]

</td><td>

Assign this role to customers for researching questions, issues, or problems. Customers can create cases, and view and edit existing cases. They can also view a list of assets belonging to their accounts.

</td><td>

-   sn\_esm\_user
-   snc\_external

</td><td>

All users with customer roles and access to a list of assets belonging to their accounts.

</td><td>

For more information see .

</td></tr><tr><td>

Customer administrator \[sn\_customerservice.customer\_admin\]

</td><td>

Use this Administrator role for a customer account. This user has access to data within the account.

</td><td>

-   sn\_customerservice.customer
-   sn\_esm\_user\_admin

</td><td>

All users with an administrator role for a customer account.

</td><td>

For more information see .

</td></tr><tr><td>

Customer case manager \[sn\_customerservice.customer\_case\_manager\]

</td><td>

Assign this Customer role for managing the cases in an account and any related child accounts.

</td><td>

sn\_customerservice.customer

</td><td>

All users with a case manager role for a customer account.

</td><td>

The customer case manager role includes the privileges of the customer role and adds the following privileges:

-   Create a case on behalf of another contact in the account.
-   View a list of cases belonging to the account.
-   Edit cases belonging to the account.

**Note:** The customer case manager role is not automatically added to the sn\_customerservice.contact\_role\_assignment system property. To expose this role to customer and partner administrators, navigate to **Customer Service** &gt; **Administration** &gt; **Properties** and add it to this property.

 For more information see .

</td></tr><tr><td>

Customer service agent \[sn\_customerservice\_agent\]

</td><td>

Use this role to create cases, view and edit cases, and work with customers and subject matter experts to resolve cases. This role helps agents assist customers and partners with questions, issues, and problems.

</td><td>

-   knowledge
-   chat\_admin
-   sn\_customerservice.deescalation\_requester
-   timecard\_user
-   template\_editor
-   sn\_esm\_agent

**Note:** This role contains the cmdb\_read role.

-   sn\_shn.editor
-   domain\_expand\_scope

</td><td>

Customer service agents.

</td><td>

**Note:** A customer service agent typically supports a specific set of products across one or more communication channels. An agent can belong to one or more agent groups.

For more information see .

</td></tr><tr><td>

Customer service manager \[sn\_customerservice\_manager\]

</td><td>

Use this role with the additional responsibility for managing agents or agent groups and overriding agent actions. A customer service agent can also use this role with the additional capability of this role.

</td><td>

-   sn\_customerservice\_agent
-   timecard\_manager
-   timecard\_approver
-   skill\_admin
-   sn\_app\_cs\_social\_social\_profile\_user
-   sam
-   sn\_customerservice.consumer\_agent
-   asset
-   sn\_shn.admin
-   sn\_publications.approver
-   contract\_manager
-   sn\_app\_cs\_social\_log\_user
-   awa\_manager
-   sn\_majorissue\_mgt.major\_issue\_manager
-   email\_client\_quick\_message\_author
-   workspace\_admin
-   skill\_model\_user
-   sn\_templated\_snip.template\_snippet\_writer
-   approver\_user

**Note:** For customers upgrading to Xanadu, the approver\_user role replaces the approval\_admin role. Users with the customer service manager role can approve the approval requests that are assigned to them.

-   notify\_view

**Note:** The notify\_view role is added to the sn\_customerservice\_manager role only when the Chat Zoom Connector application is installed.


</td><td>

Customer service managers, and Customer service agents with the additional responsibility for managing agents or agent groups and overriding agent actions.

</td><td>

For more information see .

</td></tr><tr><td>

Partner \[sn\_customerservice.partner\]

</td><td>

Assign this role to create a case for the partner's own account or on behalf of a customer account.

</td><td>

-   sn\_customerservice.customer
-   sn\_esm\_partner

</td><td>

All users serving customer accounts.

</td><td>

A partner can view and edit all of the cases they have created:

-   For their own account.
-   On behalf of customer accounts they are related to.

**Note:** If you are establishing a new relationship between a partner and a customer, the partner or partner admin does not have access to historic cases created for the customer. This is because the historic cases do not have the Partner or Partner Contact fields populated on the Case form.

For more information see .

</td></tr><tr><td>

Partner administrator \[sn\_customerservice.partner\_admin\]

</td><td>

Assign this administrator role to a user with a partner account.

</td><td>

-   sn\_customerservice.partner
-   sn\_customerservice.customer\_admin
-   sn\_esm\_partner\_admin

</td><td>

All users with the admin role for a partner account.

</td><td>

The partner administrator can do the following:

-   Access the data within the partner account.
-   Access the data created by the contacts in their company in the customer account.
-   Manage users for the partner account and for customer accounts.
-   View all of the cases created by a partner.

 For more information see .

</td></tr><tr><td>

Recipients list user \[sn\_publications\_recipients\_list\_user\]

</td><td>

The recipients list user can create and view recipient lists.

</td><td>

None.

</td><td>

All users.

</td><td>

For more information see .

</td></tr><tr><td>

Role for REST APIs related to CSM web services \[csm\_ws\_integration\]

</td><td>

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

</td><td>

snc\_internal

</td><td>

All users.

</td><td>

For more information see .

</td></tr><tr><td>

Service management admin \[sn\_esm\_admin\]

</td><td>

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

</td><td>

None.

</td><td>

All users.

</td><td>

For more information see .

</td></tr><tr><td>

Service management agent \[sn\_esm\_agent\]

</td><td>

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

</td><td>

-   assignment\_workbench
-   wm\_read
-   cmdb\_read
-   agent\_schedule\_user
-   interaction\_agent
-   sn\_publications\_recipients\_list\_user

</td><td>

All users.

</td><td>

For more information see .

</td></tr><tr><td>

Service management partner \[sn\_esm\_partner\]

</td><td>

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

</td><td>

sn\_esm\_user

</td><td>

All users.

</td><td>

For more information see .

</td></tr><tr><td>

Service management partner admin \[sn\_esm\_partner\_admin\]

</td><td>

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

</td><td>

-   sn\_esm\_user\_admin
-   sn\_esm\_admin

</td><td>

All users.

</td><td>

For more information see .

</td></tr><tr><td>

Service management user \[sn\_esm\_user\]

</td><td>

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

</td><td>

-   snc\_external
-   sn\_apptmnt\_booking.appointment\_booking\_user

</td><td>

All users.

</td><td>

For more information see .

</td></tr><tr><td>

Service management user admin \[sn\_esm\_user\_admin\]

</td><td>

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

</td><td>

sn\_esm\_user

</td><td>

All users.

</td><td>

For more information see .

</td></tr></tbody>
</table>**Parent Topic:**[Roles for all products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/roles-by-product/roles-for-all-products.md)

