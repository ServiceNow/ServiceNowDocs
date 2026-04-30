---
title: Configure AES personas and roles
description: The responsibilities of your staff are controlled by roles assigned to each member. Personas aren’t explicitly part of App Engine Studio \(AES\) but administrators assign roles to give team members permission to configure or use AES.
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure AES, Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure AES personas and roles

The responsibilities of your staff are controlled by roles assigned to each member. Personas aren’t explicitly part of App Engine Studio \(AES\) but administrators assign roles to give team members permission to configure or use AES.

-   **Low-code/citizen developer**

    Low-code/citizen developers are tech savvy and interested in creating apps. Though they might not have formal coding or app development training, citizen developers can submit ideas for new apps and, if approved, build them using AES.

-   **App Engine Studio admin**

    App Engine Studio admins manage all processes related to app development in AES. They review new app ideas, manage app development and deployment, and manage collaborators, usually in the App Engine Management Center.

-   **App template admin**

    The app template admin makes sure that the right people have access to appropriate predefined and custom templates for app development in App Engine Studio.

-   **App template author**

    The app template author creates and edits custom app templates in App Engine Studio and can share them with other users or groups.

-   **Security admin**

    The security admin creates and modifies roles and access control lists for apps. This role is set on the platform level, and it is required for making updates to roles in App Engine Studio.

-   **System administrator**

    The system administrator has access to all system features, functions, and data, regardless of security constraints. Grant this privilege carefully. If you have sensitive information, such as HR records, that you must protect, create a custom admin role for that area and train a person who is authorized to see those records to act as the administrator.

-   **Professional ServiceNow developer**

    Professional ServiceNow developers can work in App Engine Studio, usually as collaborators with citizen developers. Because of their coding knowledge and development background, though, they're more likely to build and customize apps on the ServiceNow AI Platform, using more complex building tools.


<table id="table_pbn_ms3_rsb"><thead><tr><th>

Persona

</th><th>

Roles required

</th><th>

Responsibilities

</th></tr></thead><tbody><tr><td rowspan="2">

Low-code/citizen developer

</td><td>

App Engine Studio Users group \(sn\_app\_eng\_studio.user\)

</td><td>

-   Submit requests for new custom applications to build in App Engine Studio.
-   Understand ServiceNow and application development best practices.
-   Build and test applications in App Engine Studio.
-   Submit App Engine Studio applications for IT review.
-   Maintain and change the application during its life cycle if determined during the intake process.

</td></tr><tr><td>

App Engine Studio User Limited group \(sn\_app\_eng\_studio.user\)

</td><td>

-   Collaborate with other users on applications they've been given permission to see.
-   Submit App Engine Studio applications for IT review.
-   Understand ServiceNow and application development best practices.

 **Note:** Users in the App Engine Studio User Limited group can't create new apps.

</td></tr><tr><td>

App Engine Studio admin group

</td><td>

-   atf\_test\_designer
-   scan\_admin
-   app\_engine\_admin
-   sn\_app\_eng\_studio.admin
-   sn\_collab\_request.collab\_request\_admin
-   sn\_table\_bldr\_wzd.table\_bldr\_wzd\_admin

</td><td>

-   Manage App Engine Studio processes and properties.
-   Review and approve/reject submitted application requests based on intake guardrails defined by the system administrator.
-   Provision App Engine Studio user access.
-   Review submitted App Engine Studio applications.
-   Manage deployment requests.
-   Manage promotion of App Engine Studio applications across instances.
-   Execute ATF tests/suites in testing instances.
-   Ensure instance scans run with proper definitions.
-   Collaborate with the system administrator to resolve application conflicts that arise on the platform.

</td></tr><tr><td>

App template admin

</td><td>

app\_template\_admin

</td><td>

-   Control access to custom and predefined templates.
-   Activate and deactivate templates.
-   Share templates globally or with users and groups.

</td></tr><tr><td>

App template author

</td><td>

app\_template\_author

</td><td>

-   Create and edit custom templates in App Engine Studio.
-   Share custom templates with users or groups.

</td></tr><tr><td>

Security admin

</td><td>

security\_admin

</td><td>

-   Create and modify roles and access control lists.
-   Required for making updates to roles in App Engine Studio.

</td></tr><tr><td>

System administrator

</td><td>

Admin

</td><td>

-   Install and configure App Engine Studio and its dependent apps.
-   Define environments.
-   Configure pipelines.
-   Provision access to the App Engine Studio administrator group.
-   Upgrade the App Engine Studio application, when applicable.
-   Define guardrails for which AES administrators can approve or reject application intake requests.
-   Collaborate with professional ServiceNow developers to create instance scan definitions for the platform.
-   Collaborate with AES administrators to resolve application conflicts that arise on the platform.

</td></tr><tr><td>

Professional ServiceNow developer

</td><td>

-   atf\_test\_admin
-   delegated\_developer
-   scan\_admin
-   sn\_app\_eng\_studio.user
-   sn\_collab\_request.collab\_request\_admin

</td><td>

-   Build and test applications in ServiceNow Studio and App Engine Studio
-   Collaborate with citizen developers on an as-needed basis to deliver applications in App Engine Studio, including the following tasks:
    -   Ensuring application development and organizational best practices are followed by citizen developers.
    -   Helping with review and testing of submitted App Engine Studio applications.
    -   Building complex configurations involving UI Builder, Mobile App Builder, Workflow Studio, or other builder tools.
-   Create ATF tests/suites for applications.
-   Collaborate with a system administrator to create instance scan definitions for the platform.

</td></tr><tr><td>

AES admin

</td><td>

sn\_app\_eng\_studio.admin

</td><td>

Granular admin role that provides access to App Engine Studio and enables administrative access to AES tables. Can be combined with other granular admin roles or delegated development for additional permissions. For more information about granular admin roles, see [Granular admin roles required to secure your instance](https://www.servicenow.com/docs/access?context=roles-within-platform-security&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

</td></tr><tr><td>

AES collaboration admin

</td><td>

sn\_collab\_request.collaboration\_request\_admin

</td><td>

Granular admin role that provides administrative access to collaboration tables.

</td></tr><tr><td>

AES table admin

</td><td>

sn\_table\_bldr\_wzd.table\_bldr\_wzd\_admin

</td><td>

Granular admin role that provides access to manage permissions during table creation in AES.

</td></tr></tbody>
</table>**Important:** Granular admin roles cannot manage tables that depend on ServiceNow AI Platform tables, such as the Experience Visibility Control table \(sn\_udc\_experience\_visibility\_control\) or Preferred Tables \(sn\_preferred\_table\). To manage such tables, additional granular admin roles are necessary. For more information, see [Granular admin roles required to secure your instance](https://www.servicenow.com/docs/access?context=roles-within-platform-security&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

**Parent Topic:**[Configure App Engine Studio](configure-aes.md)

