---
title: Creating custom user roles
description: System administrators can create custom roles or modify the access of existing roles by using script includes and extension points/instances.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Roles installed with Customer Service Management, Components installed with Customer Service Management, Reference, Customer Service Management]
---

# Creating custom user roles

System administrators can create custom roles or modify the access of existing roles by using script includes and extension points/instances.

The Customer Service Management application uses platform ACLs and query business rules to restrict data access based on user roles. If needed, users with the administrator role can create custom roles or modify the access of existing roles by using script includes and extension points/instances.

-   The script includes store JavaScript functions and classes to handle the role access control logic.
-   Extension points/instances designate places where custom scripts can be called and then processed to extend base functionality.

The administrator can use the extension points/instances to create their own role access constants file similar to CSQueryBRUtilOOBConstants.

The administrator can create an extension instance for the existing extension point and use it to define custom role configuration constants. The following items are included with the Customer Service Management application:

-   global.CSQeryExtensionPoint: the provided extension point for CSM role configuration
-   instance.CSQueryExtensioninstanceOOB: the provided extension instance for CSM role configuration

To create a role:

1.  Create a constant file to hold the configurations for the new role similar to CSQueryBRUtilOOBConstants. For example:

    ```
    CSQueryBRUtilOOBConstantstest.ROLE_PERMISSIONS_POOL = {
       ‘sn_customerservice.customer_new_role’:{ ‘sn_customerservice_case’:{‘condition’:[‘my_new_condition’]},
    } ,
    ```

2.  Create an extension instance to hold the logic returning this new constant file to CSQueryBRUtil.
3.  Make sure that this role is on the instance and contains the sn\_esm\_user role.
4.  Assign this new role to a contact.
5.  Create or modify the ACLs and query business rules for this role as necessary.

For more information about modifying ACLs and query business rules, see [KB0685767](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsysparm_article%3DKB0685767%26sysparm_stack%3D%26sysparm_view%3D).

**Parent Topic:**[Roles installed with Customer Service Management](../reference/r_RolesInstalledWithCustomerService.md)

**Related topics**  


[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md)

[Using scripted extension points in server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/scripted-extension-points.md)

[Using UI extension points in server-side UI macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/ui-extension-points.md)

[Using client extension points in client-side UI scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/client-extension-points.md)

