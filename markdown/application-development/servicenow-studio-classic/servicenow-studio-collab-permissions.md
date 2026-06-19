---
title: Collaboration permissions for ServiceNow Studio
description: Collaboration permissions determine what delegated developers can do when working on an app in ServiceNow Studio. Admins or app owners set these permissions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/servicenow-studio-collab-permissions.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: reference
last_updated: "2026-05-29"
reading_time_minutes: 2
breadcrumb: [Reference, ServiceNow Studio, Developing your application, Building applications]
---

# Collaboration permissions for ServiceNow Studio

Collaboration permissions determine what delegated developers can do when working on an app in ServiceNow Studio. Admins or app owners set these permissions.

For more information, see [Collaborating on apps using ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/manage-app-collab-servicenow-studio.md).

## File types custom collaboration permissions

|Permission|Description|Owner default setting|Editor default setting|
|----------|-----------|---------------------|----------------------|
|All File Types|Access to all file types, including additional file types not granted by the other options.|Yes|Yes|
|Integrations|Access to web service APIs, REST APIs, data sources, and Integration Hub - Import.|Yes|Yes|
|Reporting|Access to reports and scheduled reports.|Yes|Yes|
|Mobile builders|Access to build mobile experiences, such as with Mobile App Builder.|Yes|Yes|
|UI Builder|Access to UI Builder to build complex interfaces.|Yes|Yes|
|Workflow|Access to Workflow Editor and Activity Creator.|Yes|Yes|
|Service Portal|Access to Service Portal editors and tools.|Yes|Yes|
|Workflow Studio|Access to the Workflow Studio design environment to create flows and actions.|Yes|Yes|
|Service Catalog|Access to catalog-related file types such as catalog items, record producers, and variables to add catalog items to apps.|Yes|Yes|
|Tables &amp; forms|Access to model and layout-related file types such as table columns, form layout, and list layout.|Yes|Yes|
|Decision Tables|Access to decision tables to create decision logic based on multiple if-else rules.|Yes|Yes|
|Playbooks|Access to the Playbooks design environment to create processes. Editing activity subflows or actions requires the **Flow Designer** permission.|Yes|Yes|
|Notifications|Access to create automatic email notifications and work with email templates.|Yes|Yes|

## Security/Entitlement custom collaboration permissions

**Manage access control** grants access to security management files, such as Access Control Lists and roles.

The default setting for both owners and editors is selected.

## Programming tools custom collaboration permissions

**Allow scripting** grants access to script fields, such as those in Business Rule, UI Action, and Client Script.

The default setting for both owners and editors is de-selected.

## Application management custom collaboration permissions

|Permission|Description|Owner default setting|Editor default setting|
|----------|-----------|---------------------|----------------------|
|Delete application|Access to delete the app.|Yes|No|
|Manage collaborators|Access to change the developers and their permissions to collaborate on an app.|Yes|No|
|Source control|Access to source control tool integrations.|No|No|
|Invite collaborators|Access to invite developers to collaborate on an app.|Yes|Yes|

## Deployment custom collaboration permissions

|Permission|Description|Owner default setting|Editor default setting|
|----------|-----------|---------------------|----------------------|
|Upgrade app|Access to upgrade applications.|No|No|
|Submit for deployment|Access to request deployment for an app.|Yes|No|
|Publish app to repo|Access to publish the app to your repo.|No|No|
|Publish to app store|Access to publish the app to your app store.|No|No|

**Parent Topic:**[ServiceNow Studio reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/servicenow-studio-reference.md)

