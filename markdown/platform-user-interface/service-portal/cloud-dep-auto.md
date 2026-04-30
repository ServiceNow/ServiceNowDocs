---
title: Cloud Deployment Automation
description: Automates the deployment and provisioning of the AWS CloudFormation services using Service Catalog or Service Portal.
locale: en-US
release: yokohama
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Configure a catalog in Service Portal, Create a portal, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Cloud Deployment Automation

Automates the deployment and provisioning of the AWS CloudFormation services using Service Catalog or Service Portal.

## Request apps on Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Spoke dependencies

You must activate and set up the [AWS CloudFormation spoke](https://www.servicenow.com/docs/access?context=aws-cloudformation&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) to use this application.

## Catalog items and flows

The Cloud Deployment Automation provides catalog items and flows to automate tasks. When a catalog item is submitted, the associated flow is triggered and the task is performed. To customize a flow, create a copy of it in a new application scope. Available catalog items and flows include:

|Catalog Item or Flow|Description|
|--------------------|-----------|
|Create Stack|Creates a stack in AWS CloudFormation account.|
|Create and Execute Change Set|Creates and executes a change set in AWS CloudFormation account.|
|Create Stack Set|Creates a stack set in AWS CloudFormation account.|
|Delete Stack|Deletes a stack in AWS CloudFormation account.|
|Delete Stack Set|Deletes a stack set in AWS CloudFormation account.|
|Update Stack Set|Updates a stack set in AWS CloudFormation account.|

## Subflows

The Cloud Deployment Automation provides subflows to demonstrate automating tasks. To customize a subflow, create a copy of it in a new application scope. Available subflows include:

|Subflow|Description|
|-------|-----------|
|Create Event|Creates an event if automation fails.|
|Create Incident|Creates an incident if automation fails.|
|Dynamic Flow Template|Subflow template to create event and incident.|
|Fetch Approvers and Assignees|Retrieves details of approvers \(groups and users\), assignee, and assignment group for the requested item, catalog task, and incident from the decision tables.|
|Get Stack Set Operation Result Status Reason|Retrieves the AWS CloudFormation stack set operation result status reason.|
|Get Stack Set Operation Status|Retrieves the operation status of the AWS CloudFormation stack set.|
|Get Stack Status|Retrieves the status of the AWS CloudFormation stack.|

## Actions

The Cloud Deployment Automation provides an action, Change Array.Object Internal Names to change an array of objects to another array of objects based upon the key value pair.

## Decision tables

The Cloud Deployment Automation application uses decision tables to save the required information. The decision tables include:

|Decision table|Description|
|--------------|-----------|
|CDA Requested Item User Approval Policy|Policy used to assign a requested item to the relevant user for approval.|
|CDA Requested Item Group Approval Policy|Policy used to assign a requested item to the relevant group for approval.|
|CDA Incident User Assignment Policy|Policy used to assign an incident to the relevant user.|
|CDA Incident Group Assignment Policy|Policy used to assign an incident to the relevant group.|
|CDA Failed Automation Flow Policy|Policy used to choose between creating an incident or an event when an automation failure occurs.|
|CDA Catalog Task User Assignment Policy|Policy used to assign a catalog task to the relevant user.|
|CDA Catalog Task Group Assignment Policy|Policy used to assign a catalog task to the relevant group.|

## User roles

The Cloud Deployment Automation application provides the sn\_cloud\_dpmt\_atmn.cloud\_deployment\_automation\_user role. Users with this role can view cloud deployment automation catalog items.

**Note:** User must have the sn\_cloud\_dpmt\_atmn.cloud\_deployment\_automation\_user \_mgmt\_user, ITIL, and Catalog Admin roles to create and submit catalog items.

## System properties

The Cloud Deployment Automation application provides system properties that you can configure as per your requirement.

|System property|Description|
|---------------|-----------|
|sn\_cloud\_dpmt\_atmn.exclude\_aws\_regions|List of additional regions that should be excluded from those mentioned in the CloudDeploymentAutomationUtils script include.|
|sn\_cloud\_dpmt\_atmn.include\_aws\_regions|List of additional regions that should be included to those mentioned in CloudDeploymentAutomationUtils script include.|
|sn\_cloud\_dpmt\_atmn.flow\_loop\_limit|Number of hours that flows should run in loop before they exit.|

Navigate to **System Properties** &gt; **All Properties** to configure the values of these properties.

