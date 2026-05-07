---
title: Collaboration permissions for ServiceNow Studio
description: Collaboration permissions determine what delegated developers can do when working on an app in ServiceNow Studio. They can be set by an admin or the app owner.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, ServiceNow Studio, Developing your application, Building applications]
---

# Collaboration permissions for ServiceNow Studio

Collaboration permissions determine what delegated developers can do when working on an app in ServiceNow Studio. They can be set by an admin or the app owner.

For more information, see [Collaborating on apps using ServiceNow Studio](../concept/manage-app-collab-servicenow-studio.md).

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

**Parent Topic:**[ServiceNow Studio reference](../concept/servicenow-studio-reference.md)

