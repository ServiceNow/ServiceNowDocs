---
title: Customized app collaboration permissions in Creator Studio
description: When you customize collaboration permissions, you can choose more granular actions and parts of the app that users can work with in Creator Studio.
locale: en-US
release: zurich
product: Creator Studio
classification: creator-studio
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Collaboration, Administer, Creator Studio, Building no-code applications, Developing your application, Building applications]
---

# Customized app collaboration permissions in Creator Studio

When you customize collaboration permissions, you can choose more granular actions and parts of the app that users can work with in Creator Studio.

Use these permissions when managing collaboration, either as an admin or app owner. For more information, see the following topics:

-   [Manage Creator Studio collaboration permissions on the ServiceNow AI Platform](../task/manage-creator-studio-collaboration.md)
-   [Manage collaborators for an app in Creator Studio](../task/creator-studio-manage-collaborators.md)

## File types custom collaboration permissions

|Permission|Description|Owner default setting|Editor default setting|
|----------|-----------|---------------------|----------------------|
|All File Types|Grants access to work with all types of files, including additional file types not granted by the other options.|Yes|Yes|
|Integrations|Grants access to web service APIs, REST APIs, data sources, and Integration Hub - Import.|Yes|Yes|
|Reporting|Grants access to reports and scheduled reports.|Yes|Yes|
|Mobile builders|Grants access to build mobile experiences, such as with Mobile App Builder.|Yes|Yes|
|UI Builder|Grants access to work with UI Builder to build out more complex interfaces.|Yes|Yes|
|Workflow|Grants access to Workflow Editor and Activity Creator.|Yes|Yes|
|Service Portal|Grants access to work with Service Portal editors and tools.|Yes|Yes|
|Workflow Studio|Grants access to the Workflow Studio design environment to create flows and actions.|Yes|Yes|
|Service Catalog|Grants access to work with catalog-related file types such as catalog items, record producers, and variables to add catalog items to apps.|Yes|Yes|
|Tables &amp; forms|Grants access to model and layout-related file types such as table columns, form layout, and list layout.|Yes|Yes|
|Decision Tables|Grants access to work with decision tables to create decision logic based on multiple if-else rules.|Yes|Yes|
|Playbooks|Grants access to work with the Playbooks design environment to create processes. Editing activity subflows or actions requires the **Flow Designer** permission.|Yes|Yes|
|Notifications|Grants access to create automatic email notifications and work with email templates.|Yes|Yes|

## Security/Entitlement custom collaboration permissions

**Manage access control** grants access to security management files, such as Access Control Lists and roles.

The default setting for both owners and editors is selected.

## Programming tools custom collaboration permissions

**Allow scripting** grants access to script fields, such as those in Business Rule, UI Action, and Client Script.

The default setting for both owners and editors is de-selected.

## Application management custom collaboration permissions

|Permission|Description|Owner default setting|Editor default setting|
|----------|-----------|---------------------|----------------------|
|Delete application|Grants access to delete the app.|Yes|No|
|Manage collaborators|Grants access to change the developers and their permissions to collaborate on an app.|Yes|No|
|Source control|Grants access to work with source control tool integrations.|No|No|
|Invite collaborators|Grants access to invite developers to collaborate on an app.|Yes|Yes|

## Deployment custom collaboration permissions

|Permission|Description|Owner default setting|Editor default setting|
|----------|-----------|---------------------|----------------------|
|Upgrade app|Grants access to upgrade applications.|No|No|
|Submit for deployment|Grants access to request deployment for an app.|Yes|No|
|Publish app to repo|Grants access to publish the app to your repo.|No|No|
|Publish to app store|Grants access to publish the app to your app store.|No|No|

**Parent Topic:**[Administering collaboration in Creator Studio](../concept/creator-studio-admin-collab-tasks.md)

