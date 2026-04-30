---
title: Cornerstone Spoke
description: Manage employee records, approvals, and employee learning in your Cornerstone instance from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Cornerstone Spoke

Manage employee records, approvals, and employee learning in your Cornerstone instance from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Cornerstone spoke v1.4 is the latest version.

## Supported versions

This spoke was built for Cornerstone version v2, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke flows

The Cornerstone spoke provides a sample flow in the draft state to demonstrate automating the Cornerstone tasks. The sample flow, Cornerstone - Pull Todos Details, retrieves the list of Todos for the required user. Ensure that this user is added to your ServiceNow instance. The retrieved records can be accessed by navigating to the TO DO Lists module in the Cornerstone application of your instance.

To customize the sample flow, copy it to a new application scope.

## Spoke subflows

The Cornerstone spoke provides sample subflows in the draft state to demonstrate automating Cornerstone tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Cornerstone - Get Certificate Transcript Details|Retrieves the certificate information of the required employee.|
|Cornerstone - Get Transcripts|Retrieves the transcript information of the required employee.|
|Cornerstone - Remove Dangling To Do|Deletes the dangling Todo records. Some of the retrieved Certificate records may not have values set for the **Status** and **Launch URL** fields. The Cornerstone - Remove Dangling To Do action deletes such todo records.|

## Spoke actions

The Cornerstone spoke provides actions to automate Cornerstone tasks when events occurs in ServiceNow. Available actions include:

|Category|Action|Description|Permission Required|OAuth 2.0 Scope|
|--------|------|-----------|-------------------|---------------|
|Core Management|Look up Approval Details Stream|Retrieves information about the pending approvals.|Request Items - View, Manage Employee Relationships|approval:read|
|Look up Organizational Units Stream|Retrieves the list of organization units based on organization unit type.|No permission required.|ou:read|
|Global Search Stream|Searches for the required people, training, certification, and so on.|No permission required.|globalsearch:read|
|Employee Management|Create Employee|Creates an employee record and retrieves core employee data from Cornerstone.|Employee API - Edit|No OAuth scope required.|
|Get Custom Fields For Employee Stream|Retrieves custom fields for an employee from Cornerstone.|Employee API - View/View - Constrainable|No OAuth scope required.|
|Look up Employees Stream|Retrieves core data of the required employees in Cornerstone.|Employee API - View/View - Constrainable|No OAuth scope required.|
|Update Employee|Updates details of the required employee in Cornerstone.|Employee API -Edit|No OAuth scope required.|
|Learning Management|Look up Approvals Stream|Retrieves the pending approvals of the manager or approver.|No permission required.|approval:read|
|Look up Assigned Trainings|Retrieves details of the trainings assigned to a user.|No permission required.|transcript:read|
|Look up Catalog Search Stream|Retrieves details of the required training.|Course Catalog - View|training:read|
|Look up Certification Transcripts Stream|Retrieves certification transcript information of the required user.|No permission required.|certification:read|
|Look up Inbox Items|Retrieves all items in the required user’s inbox as shown on the welcome page.|No permission required.|inbox:read|
|Look up Learning Object|Retrieves the learning objects from Cornerstone. The supported learning object types are, Curriculum, Event, Session, Material, Test, Video, and Online Course.|No permission required.|training:read|
|Look up Sessions Stream|Retrieves details of the upcoming sessions.|No permission required.|transcript:read|
|Look up Suggested Trainings Stream|Retrieves details of the required and suggested learning objects that have been added to user's transcripts.|No permission required.|transcript:read|
|Look up Tasks|Retrieves all the incomplete tasks assigned to the user.|No permission required.|task:read|
|Look up Transcripts Stream|Retrieves the transcript records of the required user.|No permission required.|transcript:read|
|Create Assignment|Creates a standard assignment.|Assignment Tool-Standard/Email Settings-View/Bypass User Payment|learningassignment:create|
|Look up Assignment Details|Looks up assignment details based on Assignment ID.|Assignment Tool - Standard|learningassignment:read|
|Reporting on Learning Module Management|Look up Tasks From Reporting Data Stream|Retrieves the main view to get training form user tasks.|Reporting API|Reporting API|
|Look up Trainings From Reporting Stream|Retrieves the main view to get training data.|Reporting API|Reporting API|
|Look up Transcripts From Data Exporter Data Stream|Retrieves the main view to get all user transcript related data.|transcript\_core|Reporting API|
|Look up Training Local From Reporting Data Stream|Retrieves the main view to get the training's local data.|Reporting API|Reporting API|

## Spoke module

The Cornerstone spoke adds a Cornerstone application to your ServiceNow instance. The Cornerstone application has the TO DO Lists module. List of Todos that the sample flow, Cornerstone - Pull Todos Details, retrieves for the specified user, can be accessed here.

## Cornerstone spoke account requirements

If you want to use the default settings and permissions provided along with the spoke, you can install the ServiceNow tile on the Cornerstone Marketplace. For more information about registering an application, see [Register an OAuth Application](https://help.csod.com/help/csod_0/Content/Edge/Integration_Center/API_Management_Page/Register_an_OAuth_Application.htm?Highlight=register%20an%20application) in Cornerstone Online Help. Record the generated Client ID and Client Secret for later use.

If you want to configure and customise the spoke as per your requirement and provide additional permissions, register an OAuth 2.0 application in your Cornerstone account to generate OAuth 2.0 tokens for the Cornerstone spoke. For more information, see [API Management](https://help.csod.com/help/csod_0/Content/Edge/Integration_Center/API_Management_Page/API_Management.htm?tocpath=Edge%2FInfrastructure%2FTools%7CAPIs%7CAPI%20Management%20Page%7C_____1) in the Cornerstone online help . Record the generated Client ID and Client Secret for later use.

## Connection and credential alias requirements

Integration hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Cornerstone spoke](../task/setup-cornerstone.md#).

