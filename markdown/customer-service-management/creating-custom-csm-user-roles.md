---
title: Creating custom user roles
description: System administrators can create custom roles or modify the access of existing roles by using script includes and extension points/instances.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Roles installed with Customer Service Management, Components installed with Customer Service Management, Customer Service Management reference, Customer Service Management]
---

# Creating custom user roles

System administrators can create custom roles or modify the access of existing roles by using script includes and extension points/instances.

The Customer Service Management application utilizes platform ACLs and query business rules to restrict data access based on user roles. If needed, users with the system administrator role can create custom roles or modify the access of existing roles by using script includes and extension points/instances.

-   Script includes store JavaScript functions and classes to handle the role access control logic.
-   Extension points/instances designate places where custom scripts can be called and then processed to extend base functionality.

The system administrator can use the extension points/instances to create their own role access constants file similar to CSQueryBRUtilOOBConstants.

The system administrator can create a new extension instance for the existing extension point and use it to define custom role configuration constants. The following items are included with the Customer Service Management application:

-   global.CSQeryExtensionPoint: the provided extension point for CSM role configuration
-   instance.CSQueryExtensioninstanceOOB: the provided extension instance for CSM role configuration

To create a new role:

1.  Create a new constant file to hold the configurations for the new role similar to CSQueryBRUtilOOBConstants. For example:

    ```
    CSQueryBRUtilOOBConstantstest.ROLE_PERMISSIONS_POOL = {
       ‘sn_customerservice.customer_new_role’:{ ‘sn_customerservice_case’:{‘condition’:[‘my_new_condition’]},
    } ,
    ```

2.  Create a new extension instance to hold the logic returning this new constant file to CSQueryBRUtil.
3.  Make sure this role is on the instance and contains the sn\_esm\_user role.
4.  Assign this new role to a contact.
5.  Create or modify the ACLs and query business rules for this role as necessary.

For more information about modifying ACLs and query business rules, see [KB0685767](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0685767%26sysparm_stack%3D%26sysparm_view%3D).

**Parent Topic:**[Roles installed with Customer Service Management](../reference/r_RolesInstalledWithCustomerService.md)

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

