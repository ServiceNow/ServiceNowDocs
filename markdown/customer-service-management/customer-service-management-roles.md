---
title: Customer Service Management roles
description: The Customer Service Management \(CSM\) application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between users. CSM is installed with certain basic and primary roles.Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.Use this role to create cases, view and edit cases, and work with customers and subject matter experts to resolve cases. This role helps agents assist customers and partners with questions, issues, and problems.Use this role with the additional responsibility for managing agents or agent groups and overriding agent actions. A customer service agent can also use this role with the additional capability of this role.Use this role to create cases, view and edit cases, and work with customers and subject matter experts to resolve cases. This role helps agents assist consumers with questions, issues, and problems.Assign this role to customers for researching questions, issues, or problems. Customers can create cases, and view and edit existing cases. They can also view a list of assets belonging to their accounts.Use this Administrator role for a customer account. This user has access to data within the account.Assign this Customer role for managing the cases in an account and any related child accounts.Assign this role to create a case for the partner's own account or on behalf of a customer account.Assign this administrator role to a user with a partner account.Assign this Consumer role to users for researching questions, issues, or problems.Can create, view, update and delete records in the following table:​ ​ Case type \[sn\_case\_type\]​Can create, view, update and delete records in the following table:​ ​ Customer Service Case \[sn\_customerservice\_case\]​Can delete records in the following table:​ ​ Case line \[sn\_case\_line\]​Can delete records in the following table:​ ​ Case Digest \[sn\_csm\_case\_digest\_task\]​. ​ Can create, view, update and delete records in the following table:​ ​ Case Digest Configuration \[sn\_csm\_case\_digest\_config\]​.Can read records in the following table:​ ​ Case Action Summary \[sn\_csm\_case\_digest\_cas\],​ Post Case Review \[sn\_csm\_case\_digest\_pcr\]​. ​ Can create, view, update and delete records in the following table:​ ​ CS Document Template \[sn\_csm\_doctemplate\_template\]​Can create, view, update and delete records in the following table:​ ​ Task Plan Category \[sn\_task\_plan\_category\]​, Task Plan Template Configuration \[sn\_task\_plan\_config\]​, Task Plan Configuration Category \[sn\_task\_plan\_config\_category\]​, Task Plan Template \[sn\_task\_plan\_template\]​, Task Plan Template Access \[sn\_task\_plan\_template\_access\]​, Task Plan Template Category \[sn\_task\_plan\_template\_category\]​, Task Plan Template Execution \[sn\_task\_plan\_template\_execution\]​, Template Item \[sn\_task\_plan\_template\_item\]​, Template Item Condition \[sn\_task\_plan\_template\_item\_condition\]​, Template Item Configuration \[sn\_task\_plan\_template\_item\_config\]​Can read records in the following table:​ ​Customer Project Task \[customer\_project\_task\]​Can create, view, update and delete records in the following tables:​ ​ Related Record Definition \[sn\_related\_record\_definition\]​, Related Record Context \[sn\_related\_record\_context\]​, Context Related Record Definition \[sn\_m2m\_context\_related\_record\_defn\]​
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 14
keywords: [Customer Service Management Base roles, Customer Service Management Base roles, Customer Service Management Base roles, Customer Service Management Base roles, Customer Service Management Base roles, Customer Service Management Base roles, Customer Service Management Base roles, Customer Service Management Primary roles, Customer Service Management Primary roles, Customer Service Management Primary roles, Customer Service Management Primary roles, Customer Service Management Primary roles, Customer Service Management Primary roles, Customer Service Management Primary roles, Customer Service Management Primary roles, Customer Service Management Primary roles]
breadcrumb: [Reference, Customer Service Management]
---

# Customer Service Management roles

The Customer Service Management \(CSM\) application uses roles to provide access to information, identify internal and external users, maintain data security, and establish different types of relationships between users. CSM is installed with certain basic and primary roles.

Customer Service Management provides several primary roles that support the following business models:

-   Business-to-business \(B2B\): With this business model, you can support accounts and contacts. Additionally, you can create relationships and account teams to support your customers.
-   Business-to-consumer \(B2C\): With this business model, you can support individual consumers.

These roles ensure access to data while maintaining data security for different types of business relationships.

Besides the Base and Primary roles \(that are based on the Base roles\), there are Explicit roles as well. You may have business requirements that can vary how you use the roles. The Explicit roles in CSM feature lets you assign both internal and external roles to external users. It is important to regularly review user role assignments to ensure that they are set according to your business requirements.

For more information about reviewing and updating user role assignments, see:

-   [KB0829930](https://support.servicenow.com/kb_view.do?sysparm_article=KB0829930)
-   [Fix external user role assignments](../concept/fixing-external-role-assignment.md)

To learn more about managing Customer Service Management roles, see [Components installed with CSM workspaces](installed-with-cust-serv-workspace.md) and [Components installed with additional plugins for Customer Service Management](inst-wi-cust-serv-addtl-plugins.md).

**Parent Topic:**[Customer Service Management](../concept/c_CustomerServiceManagement.md)

## Service management agent \[sn\_esm\_agent\]

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

All users.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Service management partner \[sn\_esm\_partner\]

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

### Contains Roles

List of roles contained within the role.

sn\_esm\_user

### Groups

List of groups this role is assigned to by default.

All users.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Service management user admin \[sn\_esm\_user\_admin\]

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

### Contains Roles

List of roles contained within the role.

sn\_esm\_user

### Groups

List of groups this role is assigned to by default.

All users.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Service management admin \[sn\_esm\_admin\]

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

All users.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Service management user \[sn\_esm\_user\]

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

### Contains Roles

List of roles contained within the role.

-   snc\_external
-   sn\_apptmnt\_booking.appointment\_booking\_user

### Groups

List of groups this role is assigned to by default.

All users.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Service management partner admin \[sn\_esm\_partner\_admin\]

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

### Contains Roles

List of roles contained within the role.

-   sn\_esm\_user\_admin
-   sn\_esm\_admin

### Groups

List of groups this role is assigned to by default.

All users.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Role for REST APIs related to CSM web services \[csm\_ws\_integration\]

Use this Base role to access all features available within Customer Service Management. This role is available and installed with the Customer Service Base Entities plugin.

### Contains Roles

List of roles contained within the role.

snc\_internal

### Groups

List of groups this role is assigned to by default.

All users.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Customer service agent \[sn\_customerservice\_agent\]

Use this role to create cases, view and edit cases, and work with customers and subject matter experts to resolve cases. This role helps agents assist customers and partners with questions, issues, and problems.

### Contains Roles

List of roles contained within the role.

-   knowledge
-   chat\_admin
-   sn\_customerservice.deescalation\_requester
-   timecard\_user
-   template\_editor
-   sn\_esm\_agent

    **Note:** This role contains the cmdb\_read role.

-   sn\_shn.editor
-   domain\_expand\_scope

### Groups

List of groups this role is assigned to by default.

Customer service agents.

### Special considerations

**Note:** A customer service agent typically supports a specific set of products across one or more communication channels. An agent can belong to one or more agent groups.

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Customer service manager \[sn\_customerservice\_manager\]

Use this role with the additional responsibility for managing agents or agent groups and overriding agent actions. A customer service agent can also use this role with the additional capability of this role.

### Contains Roles

List of roles contained within the role.

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


### Groups

List of groups this role is assigned to by default.

Customer service managers, and Customer service agents with the additional responsibility for managing agents or agent groups and overriding agent actions.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Consumer service agent \[sn\_customerservice.consumer\_agent\]

Use this role to create cases, view and edit cases, and work with customers and subject matter experts to resolve cases. This role helps agents assist consumers with questions, issues, and problems.

### Contains Roles

List of roles contained within the role.

-   sn\_esm\_agent
-   chat\_admin
-   sn\_shn.editor
-   template\_editor
-   knowledge

### Groups

List of groups this role is assigned to by default.

All consumer service agents.

### Special considerations

**Note:** A consumer service agent typically supports a specific set of products across one or more communication channels. An agent can belong to one or more agent groups.

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Customer \[sn\_customerservice.customer\]

Assign this role to customers for researching questions, issues, or problems. Customers can create cases, and view and edit existing cases. They can also view a list of assets belonging to their accounts.

### Contains Roles

List of roles contained within the role.

-   sn\_esm\_user
-   snc\_external

### Groups

List of groups this role is assigned to by default.

All users with customer roles and access to a list of assets belonging to their accounts.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Customer administrator \[sn\_customerservice.customer\_admin\]

Use this Administrator role for a customer account. This user has access to data within the account.

### Contains Roles

List of roles contained within the role.

-   sn\_customerservice.customer
-   sn\_esm\_user\_admin

### Groups

List of groups this role is assigned to by default.

All users with an administrator role for a customer account.

### Special considerations

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Customer case manager \[sn\_customerservice.customer\_case\_manager\]

Assign this Customer role for managing the cases in an account and any related child accounts.

### Contains Roles

List of roles contained within the role.

sn\_customerservice.customer

### Groups

List of groups this role is assigned to by default.

All users with a case manager role for a customer account.

### Special considerations

The customer case manager role includes the privileges of the customer role and adds the following privileges:

-   Create a case on behalf of another contact in the account.
-   View a list of cases belonging to the account.
-   Edit cases belonging to the account.

**Note:** The customer case manager role is not automatically added to the sn\_customerservice.contact\_role\_assignment system property. To expose this role to customer and partner administrators, navigate to **Customer Service** &gt; **Administration** &gt; **Properties** and add it to this property.

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Partner \[sn\_customerservice.partner\]

Assign this role to create a case for the partner's own account or on behalf of a customer account.

### Contains Roles

List of roles contained within the role.

-   sn\_customerservice.customer
-   sn\_esm\_partner

### Groups

List of groups this role is assigned to by default.

All users serving customer accounts.

### Special considerations

A partner can view and edit all of the cases they have created:

-   For their own account.
-   On behalf of customer accounts they are related to.

**Note:** If you are establishing a new relationship between a partner and a customer, the partner or partner admin does not have access to historic cases created for the customer. This is because the historic cases do not have the Partner or Partner Contact fields populated on the Case form.

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Partner administrator \[sn\_customerservice.partner\_admin\]

Assign this administrator role to a user with a partner account.

### Contains Roles

List of roles contained within the role.

-   sn\_customerservice.partner
-   sn\_customerservice.customer\_admin
-   sn\_esm\_partner\_admin

### Groups

List of groups this role is assigned to by default.

All users with the admin role for a partner account.

### Special considerations

The partner administrator can do the following:

-   Access the data within the partner account.
-   Access the data created by the contacts in their company in the customer account.
-   Manage users for the partner account and for customer accounts.
-   View all of the cases created by a partner.

For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Consumer \[sn\_customerservice.consumersn\_customerservice.consumer\]

Assign this Consumer role to users for researching questions, issues, or problems.

### Contains Roles

List of roles contained within the role.

-   sn\_esm\_user
-   snc\_external

### Groups

List of groups this role is assigned to by default.

All users with the assigned Consumer role.

### Special considerations

Consumers can create cases and view and edit existing cases for products that they have purchased. They can also view a list of their products. For more information see [Roles installed with Customer Service Management](r_RolesInstalledWithCustomerService.md).

## Case Type Configuration Admin \[sn\_csm\_case\_type.config\_admin\]

Can create, view, update and delete records in the following table:​ ​ Case type \[sn\_case\_type\]​

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Customer Service Case Admin  \[sn\_customerservice.case\_admin​\]

Can create, view, update and delete records in the following table:​ ​ Customer Service Case \[sn\_customerservice\_case\]​

### Contains Roles

List of roles contained within the role.

None.

**Note:** Limited fields accessibility. No full privilege. ​ ​

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Case Line Admin  \[sn\_case\_line.admin​\]

Can delete records in the following table:​ ​ Case line \[sn\_case\_line\]​

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Case Digest Admin  \[sn\_csm\_case\_digest.admin​\]

Can delete records in the following table:​ ​ Case Digest \[sn\_csm\_case\_digest\_task\]​. ​ Can create, view, update and delete records in the following table:​ ​ Case Digest Configuration \[sn\_csm\_case\_digest\_config\]​.

### Contains Roles

List of roles contained within the role.

sn\_csm\_doctemplate.admin​.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Doc Template Admin \[sn\_csm\_doctemplate.admin​\] ​

Can read records in the following table:​ ​ Case Action Summary \[sn\_csm\_case\_digest\_cas\],​ Post Case Review \[sn\_csm\_case\_digest\_pcr\]​. ​ Can create, view, update and delete records in the following table:​ ​ CS Document Template \[sn\_csm\_doctemplate\_template\]​

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Task Plan Admin  \[sn\_task\_plan.admin​\]

Can create, view, update and delete records in the following table:​ ​ Task Plan Category \[sn\_task\_plan\_category\]​, Task Plan Template Configuration \[sn\_task\_plan\_config\]​, Task Plan Configuration Category \[sn\_task\_plan\_config\_category\]​, Task Plan Template \[sn\_task\_plan\_template\]​, Task Plan Template Access \[sn\_task\_plan\_template\_access\]​, Task Plan Template Category \[sn\_task\_plan\_template\_category\]​, Task Plan Template Execution \[sn\_task\_plan\_template\_execution\]​, Template Item \[sn\_task\_plan\_template\_item\]​, Template Item Condition \[sn\_task\_plan\_template\_item\_condition\]​, Template Item Configuration \[sn\_task\_plan\_template\_item\_config\]​

### Contains Roles

List of roles contained within the role.

-   sn\_task\_plan.creator​
-   sn\_task\_plan.delete
-   sn\_task\_plan.report\_viewer​
-   sn\_task\_plan.navigation\_menu​

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Customer Project Management Admin  \[sn\_csm\_ppm.admin\]

Can read records in the following table:​ ​Customer Project Task \[customer\_project\_task\]​

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## UIB Dynamic Related Records Admin \[sn\_uib\_dyn\_rel\_rec.admin​\]

Can create, view, update and delete records in the following tables:​ ​ Related Record Definition \[sn\_related\_record\_definition\]​, Related Record Context \[sn\_related\_record\_context\]​, Context Related Record Definition \[sn\_m2m\_context\_related\_record\_defn\]​

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

