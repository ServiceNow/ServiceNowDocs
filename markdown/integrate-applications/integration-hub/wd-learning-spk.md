---
title: Workday Learning Spoke
description: The Workday HR spoke is built by Bristlecone, Inc. Manage approvals, courses, and user in the Workday Learning instance from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday Learning Spoke

The Workday HR spoke is built by Bristlecone, Inc. Manage approvals, courses, and user in the Workday Learning instance from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Workday Learning spoke v1.1.4 is the latest version.

## Supported versions

This spoke was built for Workday Learning v36.0, but may be compatible with later versions.

## Spoke requirements

-   Register Integration System User.

    **Note:** While filling account information details, ensure that you select the **Do Not Allow UI Sessions** check box.

-   Workday REST and Report-as-a-Service \(RAAS\) API works with OAuth 2.0 to authorize access to resources in your Workday tenant. To use OAuth 2.0, you must register your client in the tenant, using the Register API Client task.

    Record and save these values while registering your client:

    -   Client ID
    -   Client Secret
    -   Workday REST API Endpoint
    -   Token Endpoint
    -   Authorization Endpoint
-   Create a security group and assign it to the integration system user and provide these permissions.

    |Operation|Domain Security Policy|Domain Security Policies Inheriting Permission|Functional Areas|
    |---------|----------------------|----------------------------------------------|----------------|
    |View Only|Worker Data: Public Worker Reports| |Staffing|
    |Get Only|Worker Data: Public Worker Reports| |Staffing|
    |Get Only|Manage: Learning Content| |Learning Core|
    |View Only|Reports: Learning Record| |Learning Core|
    |Get Only|Reports: Learning Record| |Learning Core|
    |View Only|Person Data: Learning| |Learning Core|
    |Get Only|Person Data: Learning| |Learning Core|
    |View Only|Business Process Reporting| |System|
    |View Only|Reports: Learning Record| |Learning Core|
    |Get Only|Reports: Learning Record| |Learning Core|
    |Get and Put|Manage: Learning Course Enrollments| |Learning Core|
    |View and Modify|Business Process Administration|Business Process Delegation|System|
    |Get only|Set up: Skills and Experience| |Worker Profile and Skills|

    |Operation|Business Process Type|Functional Area|
    |---------|---------------------|---------------|
    |Initiate \(Enroll In Learning Content \(Web Service\)\)|Enroll in Content|Learning Core|


## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - SOAP \(com.glide.hub.action\_step.soap\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow Flow Designer - Dynamic Outputs \(com.glide.hub.dynamic\_outputs\)
-   Complex Object \(com.glide.cobject\)
-   System Import Data Source \(glide.system\_import\_data\_source\)
-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The Workday Learning spoke provides a sample flow, Trigger Workday Learning Integration. This flow in turn triggers the subflows to automate tasks. To customize the sample flow, copy it to the required application scope.

## Spoke subflows

The Workday Learning spoke provides sample subflows to demonstrate automating Workday Learning tasks. To customize a sample subflow, copy it to the required application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Assign Course to Workday Learning|Assigns learning courses to the ServiceNow users.|
|Pull Courses from Workday Learning|Retrieves details of the learning courses and maps courses from Workday Learning to ServiceNow.|
|Pull User Activity from Workday Learning|Retrieves user course activity data from Workday Learning and saves it in the ServiceNow instance.|
|Track Approval for Workday Learning|Retrieves details of learning todos from Workday Learning and saves it in the ServiceNow instance.|
|Workday Learning User Mapping|Maps users between Workday Learning and ServiceNow instance.|

## Spoke actions

The Workday Learning spoke provides actions to automate Workday tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Approval Management|Look up Approvals|Retrieves approval items from the inbox.|
|Course Management|Create Assignment|Creates an enrollment in the Learning Content.|
|Look up Assignment|Retrieves details of the learning assignments.|
|Look up Blended Courses Stream|Retrieves details of the blended courses.|
|Look up Course Offerings Stream|Retrieves details of the blended course offerings.|
|Look up Digital Courses Stream|Retrieves details of the digital courses.|
|Look up Enrollment|Retrieves details of the self learning enrollments.|
|Look up Lessons Stream|Retrieves details of the standalone lessons.|
|Look up Programs Stream|Retrieves details of the learning programs.|
|User Management|Look up Users Stream|Retrieves worker details such as, personal data, employment data, email data, worker reference data, and so on.|
|Skills management|Look up Skills Stream|Retrieves details of the skills required for the learning program.|

## Spoke module

The Workday Learning spoke provides Workday Learning application that has these modules:

|Module|Description|
|------|-----------|
|Report Configuration|Enables you to create a record to specify the RAAS report configurations. Only one record can be created in this module.|
|Profile Sync Configuration|Enables you to specify the Workday tenant timezone.|
|Data Sources|
|Sync User Activity|Saves the details of the user course activity as an attachment. These details are retrieved by the Look up Assignment action.|
|Self Enrollment Activity|Saves the details of the user course self enrollment as an attachment. These details are retrieved by the Look up Enrollment action.|
|Track Approval|Saves the details of the todo approvals as an attachment. These details are retrieved by the Look up Approvals actions.|
|Scheduled Imports|
|Sync User Activity|Enables handling of the transformation errors while synchronizing the user activity.|
|Self Enrollment Activity|Enables handling of the transformation errors while synchronizing the self enrollment activity.|
|Track Approval|Enables handling of the transformation errors while synchronizing the approvals.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Workday Learning spoke](../task/wd-learning-setup.md#).

