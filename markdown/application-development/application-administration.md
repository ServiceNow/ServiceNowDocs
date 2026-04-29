---
title: Application administration
description: Protect sensitive application data by using application administration to restrict how users acquire application-specific roles.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Application administration

Protect sensitive application data by using application administration to restrict how users acquire application-specific roles.

## Functions of application administration

Use application administration to:

-   Help prevent unauthorized users from accessing sensitive data via forms, lists and UI, such as financial records or personally identifiable information.
-   Determine who can assign scope-protected roles such as the administrator and designated developers for the application.
-   Help prevent users with the system-level admin role from:
    -   Assigning themselves a protected application role.
    -   Assigning themselves to a group containing a protected application role.
    -   Bypassing existing access controls to a protected application by creating access controls.
    -   Impersonating a user who has a protected application administration role, unless the developer or administrator also has that role.
    -   Inheriting a protected application role.
    -   Overriding existing access controls to a protected application.

## Roles in application administration

You can make any role an application-specific administrator by selecting the **Application Administrator** check box in Role Configuration. To learn more, see [Restrict access to an application](../task/enable-application-administration.md). By convention, create the following roles:

<table id="table_kdp_xkr_vlb"><thead><tr><th>

Role name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application-specific admin

</td><td>

Users with this role can assign other users to an application-specific role for that application. For example, you can create a role named my\_application.admin. It should include the name of the restricted application, with a suffix of "admin" to indicate that it is the admin role for the application.

</td></tr><tr><td>

Application-specific developer

</td><td>

Users with this role can access the restricted application. For example, you can create a role named my\_application.developer. It should include the name of the restricted application, with a suffix of "developer" to indicate that it is the developer role for the application. The developer role needs both application administrator and delegated development permissions to modify the application files.To learn more, see [Delegated development and deployment](c_DelegatedDevelopment.md) and [Delegate development and deployment permissions to personnel](../task/t_AddADeveloper.md).

</td></tr></tbody>
</table>## Application-specific admin role

The application-specific admin role enables a user to access a specific application, but does not grant the user any other admin rights. Assign the system-level admin role to a user before that user can do these tasks:

-   Configure form and list layouts.
-   Change application tables and fields.
-   Assign the application-specific admin role to new users.

If you do not want a user with the application-specific admin role to have the system-level admin role:

-   Do not assign the system-level admin role to the user. Assign only the application-specific admin role.
-   Have the user assign themselves the application-specific developer role.

As an application-specific developer, the user can perform a subset of administrative tasks without having the system-level admin role.

**Note:** Assign the application-specific admin role to more than one user. Then if a user with the application-specific admin role leaves the company, you are not prevented from changing the application.

## Enabling application administration and assigning application-specific roles

You can enable application administration for an application from the application record and restrict the assignment of application-specific roles from the user role record.

**Note:** Enable application administration and assign application-specific roles after completing development of the application, but before adding application records. This practice protects sensitive data in the application records from access by unauthorized users.

The target instance must have at least one authorized user with the application-specific admin role.

-   If you enable application administration for an application but do not assign the application-specific roles, no user can access the application.
-   If you assign only one application-specific role, you cannot delete that role.

A warning appears if you enable application administration for an application, but no users have the application-specific admin role required to assign roles for the application. The warning reminds you to assign the application-specific roles for administrators and developers of the application.

Set the **\[scoped\_app\_name\].min\_admin\_count property** to require that more than one user must have the application-specific admin role. Assigning the application-specific admin role to multiple users reduces the risk of getting locked out of the scoped application. The **\[scoped\_app\_name\].min\_admin\_count** property has the following limitations:

-   If you specify an invalid value for the property, the default requirement for assigning at least one application-specific admin is enforced.
-   If you specify a valid value for the property, you can't delete any application-specific admins unless you exceed the specified value. For example, if you specify a value of two and you have three application-specific admins, you can delete only one of those roles.
-   You can specify a value higher than the actual number of assigned application-specific admins. However, you can't delete any application-specific admins until you exceed the specified value. For example, if you specify a value of six, but have only three application-specific admins, you can't delete any of those roles.

For procedures, see [Restrict access to an application](../task/enable-application-administration.md).

## Deploying applications with application administration

You must have the system-level admin role in both your developer and production instances to deploy an application protected by application administration. The process is outlined in the following steps.

1.  Develop the application on a development instance.
2.  Create the application-specific admin role.
3.  Grant the application-specific admin role to all system-level admin users.
4.  Update the application record to enable application administration and restrict access to the application.
5.  Publish the application to the application repository.
6.  From a production instance, install the application from the application repository.
7.  As a system-level admin on the production instance, grant the application-specific admin role to the appropriate users.
8.  Remove the application-specific admin role from all users with the system-level admin role.

For procedures to enable application administration and restrict the assignment of application-specific roles, see [Restrict access to an application](../task/enable-application-administration.md).

## Training

The ServiceNow® Developer Site has training for [Securing Applications](https://developer.servicenow.com/dev.do#!/learn/courses/yokohama/app_store_learnv2_securingapps_yokohama_securing_applications/app_store_learnv2_securingapps_yokohama_securing_applications_against_unauthorized_users/app_store_learnv2_securingapps_yokohama_securing_applications_and_modules).

**Related topics**  


[Delegated development and deployment](c_DelegatedDevelopment.md)

