---
title: Components installed with User Experience Analytics
description: Several components are installed with the User Experience Analytics plugin, including user roles, scheduled jobs, and tables.View the Dashboard link and settings within User Experience Analytics in the application navigator and control the User Experience Analytics settings for each mobile, web, and service portal application. Assigned users can create funnel and cohort reports from the User Experience Analytics Dashboard.view the Dashboard link and settings within User Experience Analytics in the application navigator and control the User Experience Analytics settings for each mobile application. Assigned users have admin role permissions to be able to create funnel and cohort reports from the User Experience Analytics Dashboard.View the Dashboard link and settings under User Experience Analytics in the application navigator and Control the User Experience Analytics settings for each web application. Assigned users have admin role permissions to create funnel and cohort reports from the User Experience Analytics Dashboard.View the Dashboard link under User Experience Analytics in the application navigator. Assigned users have viewer role permissions for User Experience Analytics for mobile and web applications.View the Dashboard link under User Experience Analytics in the application navigator. Assigned users have viewer role permissions for User Experience Analytics for mobile applications.View the Dashboard link under User Experience Analytics in the application navigator. Assigned users have viewer role permissions for User Experience Analytics for web applications.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [User Experience Analytics reference, User Experience Analytics, Platform Analytics]
---

# Components installed with User Experience Analytics

Several components are installed with the User Experience Analytics plugin, including user roles, scheduled jobs, and tables.

User Experience Analytics uses these roles, scheduled jobs, tables, and business rules.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](https://www.servicenow.com/docs/access?context=find-components&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Scheduled jobs

|Scheduled job|Description|
|-------------|-----------|
|User Experience Analytics Settings|Queries the sys\_sg\_native\_client table hourly and processes any mobile applications that do not have corresponding User Experience Analytics Settings defined in the sys\_analytics\_bucket table.|
|Analytics|Registers any entry in sys\_analytics\_bucket that doesn’t have a matching entry in sys\_analytics\_authentication \(analytics buckets with no authentication settings\).|

## Tables

<table><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Experience Analytics Settings\[sys\_analytics\_bucket\]

</td><td>

Primary table. Contains the information that associates the application it references with the ServiceNow server.

</td></tr></tbody>
</table>## Business rules

|Business rule|Table|Description|
|-------------|-----|-----------|
|Create User Experience Analytics settings|sys\_sg\_native\_client|Creates User Experience Analytics Settings each time a new web or mobile application is created.|
|Register new web and mobile applications|sys\_sg\_native\_client|Enables immediate registration of new web and mobile applications.|

## Roles

## Analytics admin \[analytics\_admin\]

View the **Dashboard** link and settings within User Experience Analytics in the application navigator and control the User Experience Analytics settings for each mobile, web, and service portal application. Assigned users can create funnel and cohort reports from the User Experience Analytics Dashboard.

### Contains Roles

List of roles contained within the role.

-   analytics\_viewer
-   chat\_analytics\_admin
-   mobile\_analytics\_admin
-   sdk\_anaylitcs\_admin
-   web\_analytics\_admin

-   Can view the **Dashboard** link and settings within User Experience Analytics in the application navigator.
-   Can control the User Experience Analytics settings for each mobile, web, and service portal application.
-   Have **admin** role permissions to be able to create funnel and cohort reports from the User Experience Analytics Dashboard.

### Groups

Analytics admin \[analytics\_admin\] is included in the Analytics settings managers group.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Mobile analytics admin\[mobile\_analytics\_admin\]

view the **Dashboard** link and settings within User Experience Analytics in the application navigator and control the User Experience Analytics settings for each mobile application. Assigned users have admin role permissions to be able to create funnel and cohort reports from the User Experience Analytics Dashboard.

### Contains Roles

Mobile analytics admin \[mobile\_analytics\_admin\] contains with Mobile analytics viewer \[mobile\_analytics\_viewer\] role.

### Groups

Mobile analytics admin \[mobile\_analytics\_admin\] is included in the Mobile analytics settings managers group.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Web analytics admin\[web\_analytics\_admin\]

View the Dashboard link and settings under User Experience Analytics in the application navigator and Control the User Experience Analytics settings for each web application. Assigned users have admin role permissions to create funnel and cohort reports from the User Experience Analytics Dashboard.

### Contains Roles

List of roles contained within the role.

-   core\_ui\_analytics\_admin
-   now\_experience\_analytics\_admin
-   portal\_analytics\_admin
-   web\_analytics\_viewer

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## User experience analytics viewer \[analytics\_viewer\]

View the Dashboard link under User Experience Analytics in the application navigator. Assigned users have viewer role permissions for User Experience Analytics for mobile and web applications.

### Contains Roles

List of roles contained within the role.

-   web\_analytics\_viewer
-   mobile\_analytics\_viewer
-   sdk\_analytics\_viewer
-   chat\_analytics\_viewer

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Mobile analytics viewer \[mobile\_analytics\_viewer\]

View the **Dashboard** link under User Experience Analytics in the application navigator. Assigned users have viewer role permissions for User Experience Analytics for mobile applications.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Web analytics viewer \[web\_analytics\_viewer\]

View the Dashboard link under User Experience Analytics in the application navigator. Assigned users have viewer role permissions for User Experience Analytics for web applications.

### Contains Roles

List of roles contained within the role.

-   portal\_analytics\_viewer
-   core\_ui\_analytics\_viewer
-   now\_experience\_analytics\_viewer

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

