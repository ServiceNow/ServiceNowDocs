---
title: Workfront Spoke
description: The Workfront spoke provides actions to view and analyze meaningful usage data for Workfront software subscriptions. Analyze usage for your Workfront account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workfront Spoke

The Workfront spoke provides actions to view and analyze meaningful usage data for Workfront software subscriptions. Analyze usage for your Workfront account to determine which licenses are stale so that you can reclaim these licenses and realize your potential savings.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Workfront v1.3.0 is the latest version.

## Supported versions

This spoke was built for Workfront v1.1.1, but may be compatible with later versions.

## Spoke requirements

Adobe Workfront administrator account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Workfront spoke provides actions to automate Workfront tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Document Management|Check in Documents|Checks in a checked-out document based on its ID.|
|Check out Documents|Checks out a checked-in document based on its ID.|
|Is Document Linked|Determines if the document is linked by its unique identifier.|
|Is Proof Auto Generation Enabled|Determines if proof is auto enabled for the corresponding ID.|
|Look up Documents Stream|Retrieves the details of all access levels.|
|Upload Attachment|Creates a document in a Workfront Instance.|
|Unlink Document|Unlinks a document from the Workfront.|
|Upload Attachment to Handle|Creates a new document on the Workfront instance.|
|Look up Proof Templates|Gets all proof template information.|
|Move Document|Moves a document to a project, task, or an issue.|
|Look up Proof Recipients|Returns the details of the recipients for the given template and proof stage ID.|
|Look up Proof Stages|Gets the stage information of the Proof ID.|
|Look up Total Documents Size|Determines the size of the documents.|
|Upload Attachment to Object|Creates or links the document to the Workfront Object after the 'Upload Attachment to Handle' action.|
|Look up Documents Stream|Retrieves a list of all documents.|
|Look up Templates Stream|Retrieves a list of all templates.|
|Finance Management|Look up Expenses Stream|Retrieves a list of all expenses.|
|Issue Management|Move Issue to another Project|Moves an issue to a project.|
|Move Issue to Task|Moves one or more issues from the Workfront.|
|Bulk Move of Issues|Moves bulk issues to a task.|
|Portfolio Management|Look up Portfolios Stream|Retrieves a list of all portfolios.|
|Program Management|Look up Programs Stream|Retrieves a list of all programs.|
|Project Management|Calculate Project Timeline|Calculates the timeline for a project based on its ID.|
|Calculate Project Finance|Calculates the finances for a project with the unique ID specified.|
|Set Project Budget|Sets the budget for the specific project with the unique ID specified.|
|Look up Issues Stream|Retrieves a list of all issues.|
|Look up Projects Stream|Retrieves a list of all projects.|
|Look up Tasks Stream|Retrieves a list of all tasks.|
|Record Management|Accept Object Work|Accepts work in Workfront for the recently created object.|
|Approve Approval of Object|Approves the request for the object's approval.|
|Assign Assignee to Object|Assigns a team, user, or role to a Workfront object.|
|Assign Multiple Assignees to Object|Assigns a Workfront object to multiple users, roles, or a team.|
|Calculate Object Data Extension|Calculates the data extension for the specified object.|
|Create Object|Creates an object in your Workfront instance.|
|Delete Object|Removes an object from the Workfront instance.|
|Look up Object by ID|Retrieves the details for the given object ID as an input.|
|Look up Object Count|Returns the current item count.|
|Recall Object Approval|Recalls the approval request for the Workfront object.|
|Reject Approval of Object|Rejects the approval request for the Workfront object.|
|Reject Object Work|Rejects the work action on the object.|
|Reply to Object Assignment|Responds to the assignment of an object.|
|Unassign User from Object|Unassigns a user from a Workfront object.|
|Update Object as Done|Updates an object as done in the Workfront.|
|Update Object as Not Done|Updates an object as not done in the Workfront.|
|Update Object by ID|Updates the object in the Workfront.|
|Report Management|Look up Filters Stream|Retrieves a list of all filters.|
|Look up Reports Stream|Retrieves a list of all reports.|
|Task Management|Bulk Copy of Tasks|Copies one or more tasks from the Workfront.|
|Bulk Move of Tasks|Moves one or more tasks from the Workfront.|
|Move Task|Moves a specific task to different project or task.|
|Template Management|Look up Task Templates|Gets all task template information.|
|Look up Project Templates|Gets all project template information.|
|User Management|API Inputs \(Metadata\)|Retrieves a list of fields for the specified object code that is used as dynamic input.|
|API Outputs \(Metadata\)|Retrieves a list of fields for the specified object code that is used as dynamic output.|
|Look up Access Levels Stream|Retrieves a list of all access levels for Workfront licenses.|
|Look up Users Stream|Retrieves a list of all users within an account.|
|Update User|Modifies details about the specified user.|
|Webhook Management|Look up Event Subscriptions Stream|Retrieves the details of all event subscriptions.|
|Look up Event Subscription by ID|Retrieves the details of the event subscription for the specified ID.|
|Create Event Subscription|Creates a new event subscription in your Workfront instance.|
|Delete Event Subscription|Removes a subscription from the Workfront instance.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the Workfront spoke](../task/setup-workfront.md#).

