---
title: Add application security
description: Control who is permitted to use or edit your application by configuring roles in App Engine Studio \(AES\).
locale: en-US
release: yokohama
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Add application security

Control who is permitted to use or edit your application by configuring roles in App Engine Studio \(AES\).

Adding security in App Engine Studio, UI Builder, and Catalog Builder

## Working with roles

You add security to your application by defining roles. A role is used to limit and control access to your application. The access that you define for a role is granted to all users who are assigned to the role.

**Note:** If you don't have permission to work with roles for an app, the **Add** button for the Security section appears, but you can't select it.

An administrator assigns a role to the appropriate user based on the kind of work that the role permits. For example, to enable a manager to read and approve employee requests, an administrator would assign a role that has access to read and update records from the relevant table. The role may also need access to the portal or workspace where the manager would see the request.

Application templates automatically add security to your application. If you use a template to create your application, you can edit the roles that were added or add different roles.

<table id="table_bwp_5ty_d5b"><thead><tr><th>

Learn more about AES roles and security

</th><th>

Additional ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="3">

App Engine Studio includes default roles that you can use for your application.

 Alternatively, you can build custom roles for your application.

 After you submit your application, an administrator on-boards the requesting team by assigning the roles that you've defined.

</td><td>

![](../../../reuse/icons/brand-icons/bus-application-developer.svg) [What is Security? - ServiceNow Developers site](https://developer.servicenow.com/dev.do#!/learn/courses/vancouver/app_store_learnv2_aescreateappfromscratch_vancouver_create_an_app_from_scratch_with_app_engine_studio/app_store_learnv2_aescreateappfromscratch_vancouver_secure_apps_and_data/app_store_learnv2_aescreateappfromscratch_vancouver_what_is_security)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-application-developer.svg) [Security and Roles - ServiceNow Developers site](https://developer.servicenow.com/dev.do#!/learn/courses/sandiego/app_store_learnv2_bmfaesa_sandiego_build_my_first_app_engine_studio_application/BAP_sandiego/BAP_SecurityAndRoles_sandiego)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-application-developer.svg) [Elevating Privileges - ServiceNow Developers site](https://developer.servicenow.com/dev.do#!/learn/courses/vancouver/app_store_learnv2_aescreateappfromscratch_vancouver_create_an_app_from_scratch_with_app_engine_studio/app_store_learnv2_aescreateappfromscratch_vancouver_secure_apps_and_data/app_store_learnv2_aescreateappfromscratch_vancouver_elevating_privileges)

</td></tr></tbody>
</table>-   **[Build a new role for your application](../task/aes-create-role.md)**  
Create a custom role for your application in App Engine Studio \(AES\).
-   **[Use an existing role for your application](../task/aes-existing-role.md)**  
Use a previously created role for your application in App Engine Studio \(AES\).
-   **[Change access settings for a role](../task/edit-role.md)**  
Control the application permissions for a role in App Engine Studio \(AES\).
-   **[Delete a role](../task/delete-role.md)**  
Delete a role that you no longer need in App Engine Studio \(AES\).

**Parent Topic:**[Enhance your app](customize-application.md)

