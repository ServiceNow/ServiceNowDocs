---
title: Cornerstone Spoke
description: Manage employee records, approvals, and employee learning in your Cornerstone instance from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-24"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Cornerstone Spoke

Manage employee records, approvals, and employee learning in your Cornerstone instance from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Cornerstone spoke v1.3.2 is the latest version

## Supported versions

This spoke was built for Cornerstone version v1, but may be compatible with later versions.

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

|Category|Action|Description|
|--------|------|-----------|
|Core Management|Look up Approval Details|Retrieves information about the pending approvals.|
|Look up Organizational Unit|Retrieves the list of organization units based on organization unit type.|
|Global Search|Searches for the required people, training, certification, and so on.|
|Employee Management|Create Employee|Creates an employee record and retrieves core employee data from Cornerstone.|
|Get Custom Fields For Employee|Retrieves custom fields for an employee from Cornerstone.|
|Look up Employees|Retrieves core data of the required employees in Cornerstone.|
|Update Employee|Updates details of the required employee in Cornerstone.|
|Learning Management|Look up Approvals|Retrieves the pending approvals of the manager or approver.|
|Look up Assigned Trainings|Retrieves details of the trainings assigned to a user.|
|Look up Catalog Search|Retrieves details of the required training.|
|Look up Certification Transcripts|Retrieves certification transcript information of the required user.|
|Look up Certifications From Reporting Data Stream|Retrieves the main view to get the certification data.|
|Look up Inbox Items|Retrieves all items in the required user’s inbox as shown on the welcome page.|
|Look up Learning Object|Retrieves the learning objects from Cornerstone. The supported learning object types are, Curriculum, Event, Session, Material, Test, Video, and Online Course.|
|Look up Sessions|Retrieves details of the upcoming sessions.|
|Look up Suggested Training|Retrieves details of the required and suggested learning objects that have been added to user's transcripts.|
|Look up Tasks|Retrieves all the incomplete tasks assigned to the user.|
|Look up Transcripts|Retrieves the transcript records of the required user.|
|Create Assignment|Creates a standard assignment.|
|Look up Assignment Details|Looks up assignment details based on Assignment ID.|
|Reporting on Learning Module Management|Look up Tasks From Reporting Data Stream|Retrieves the main view to get training form user tasks.|
|Look up Trainings From Reporting|Retrieves the main view to get training data.|
|Look up Transcripts From Reporting Data Stream|Retrieves the main view to get all user transcript related data.|
|Look up Training Local From Reporting Data Stream|Retrieves the main view to get the training's local data.|
|Look up Certifications From Reporting Data Stream|Retrieves the main view to get all user certifications related data.|

## Spoke module

The Cornerstone spoke adds a Cornerstone application to your ServiceNow instance. The Cornerstone application has the TO DO Lists module. List of Todos that the sample flow, Cornerstone - Pull Todos Details, retrieves for the specified user, can be accessed here.

## Cornerstone spoke account requirements

If you want to use the default settings and permissions provided along with the spoke, you can install the ServiceNow tile on the Cornerstone Marketplace. For more information about registering an application, see [https://help.csod.com/help/csod\_0/Content/Edge/Integration\_Center/Edge\_-\_Getting\_Started.htm?tocpath=Edge%2FInfrastructure%2FTools%7CEdge%20Marketplace%7C\_\_\_\_\_3](https://help.csod.com/help/csod_0/Content/Edge/Integration_Center/Edge_-_Getting_Started.htm?tocpath=Edge%2FInfrastructure%2FTools%7CEdge%20Marketplace%7C_____3) in Cornerstone OnDemand Help. Record the generated Client ID and Client Secret for later use.

If you want to configure and customise the spoke as per your requirement and provide additional permissions, register an OAuth 2.0 application in your Cornerstone account to generate OAuth 2.0 tokens for the Cornerstone spoke. For more information about registering an application, see [API Management](https://help.csod.com/help/csod_0/Content/Edge/Integration_Center/API_Management_Page/API_Management.htm?tocpath=Edge%2FInfrastructure%2FTools%7CAPIs%7CAPI%20Management%20Page%7C_____1) in the Cornerstone online help . Record the generated Client ID and Client Secret for later use.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Cornerstone spoke](../task/setup-cornerstone.md#).

