---
title: Jamf Spoke
description: Manage users, mobile devices, groups, and computers in the Jamf account from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Jamf Spoke

Manage users, mobile devices, groups, and computers in the Jamf account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Jamf spoke v1.4.0 is the latest version.

## Supported versions

This spoke was built for Jamf Classic and Pro APIs, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST\(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and need appropriate licenses, if used outside the spoke implementation. For information on the licenses, contact your account manager.

## Spoke subflows

The Jamf spoke provides sample subflows to demonstrate automating tasks. To customize a sample subflow, copy it to the required application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Configure Group|Enables a CSD agent to create and configure the target group in Jamf portal.|
|Create Software Configuration|Enables a CSD Agent to create the software configuration record of the specified Jamf application.|
|Discover and Store Data|Discovers the data from the Jamf server and updates the records in Application, Group, and Policy tables.|
|Look up Application Details|Retrieves the additional details for applications and updates the respective records in the application table.|
|Deploy Application|Adds the provided user or device to the given group in the Jamf Server.|
|Revoke Application|Removes the provided user or device from the given group in the Jamf Server.|
|Look up Configuration Data|Retrieves configuration data for the specified requested item or software configuration record.|

**Note:** These subflows are available only when the [Client Software Distribution 2.0 application](csd-app-2-1.md) is installed.

## Spoke actions

The Jamf spoke provides actions to automate tasks when events occur in your ServiceNow instance. Available actions include:

<table id="table_asv_h1l_zrb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="11">

Computer Management

</td><td>

Look up Application by ID

</td><td>

Retrieves details of an application by ID in Jamf.

</td></tr><tr><td>

Look up Applications Stream

</td><td>

Retrieves all the applications.

</td></tr><tr><td>

Look up Computer by Serial Number

</td><td>

Retrieves details of computer by serial number in Jamf.

</td></tr><tr><td>

Look up Computers Stream

</td><td>

Retrieves general and hardware details of all the computers.

</td></tr><tr><td>

Look up Package by ID

</td><td>

Retrieves details of package by ID in Jamf.

</td></tr><tr><td>

Look up Packages Stream

</td><td>

Retrieves all the packages.

</td></tr><tr><td>

Look up Policies Stream

</td><td>

Retrieves all the policies.

</td></tr><tr><td>

Look up Policy by ID

</td><td>

Retrieves details of policy by ID in Jamf.

</td></tr><tr><td>

Add Computer Group to Mac Application

</td><td>

Adds a target computer group to a Mac application given the current scope of the application.

</td></tr><tr><td>

Add User Group to Mac Application

</td><td>

Adds a target user group to a Mac application given the current scope of the application.

</td></tr><tr><td>

Remove Computer Group from Mac Application

</td><td>

Removes a target computer group from a Mac application given the current scope of the application.

</td></tr><tr><td rowspan="2">

Data Management**Note:** These actions are available only when the [Client Software Distribution 2.0 application](csd-app-2-1.md) is installed.

</td><td>

Look up Configuration Data

</td><td>

Retrieves the configuration data for the specified requested item or software configuration record.

</td></tr><tr><td>

Prepare Software Data

</td><td>

Prepares the software data for the specified requested item that can be used for deployment or revocation.

</td></tr><tr><td rowspan="22">

Group Management

</td><td>

Add Computer to Static Group

</td><td>

Adds an existing computer to a static group in Jamf.

</td></tr><tr><td>

Add Mobile Device to Static Group

</td><td>

Adds an existing mobile device to a static group in Jamf.

</td></tr><tr><td>

Add User to Static Group

</td><td>

Adds an existing user to a static group in Jamf.

</td></tr><tr><td>

Create Static Computer Group

</td><td>

Creates a static computer group with the given name on the server.

</td></tr><tr><td>

Create Static Mobile Device Group

</td><td>

Creates a static mobile device group with the given name on the server.

</td></tr><tr><td>

Create Static User Group

</td><td>

Creates a static user group with the given name on the server.

</td></tr><tr><td>

Delete Computer Group

</td><td>

Deletes the given computer group from the server.

</td></tr><tr><td>

Delete Mobile Device Group

</td><td>

Deletes the given mobile device group from the server.

</td></tr><tr><td>

Delete User Group

</td><td>

Deletes the given user group from the server.

</td></tr><tr><td>

Is Computer in Group

</td><td>

Checks if an existing computer is a member of the specified group in Jamf.

</td></tr><tr><td>

Is Mobile Device in Group

</td><td>

Checks if an existing mobile device is a member of the specified group in Jamf.

</td></tr><tr><td>

Is User in Group

</td><td>

Checks if an existing user is a member of the specified group in Jamf.

</td></tr><tr><td>

Look up Computer Group by ID

</td><td>

Retrieves details of computer group by ID in Jamf.

</td></tr><tr><td>

Look up Computer Groups Stream

</td><td>

Retrieves all the computer groups.

</td></tr><tr><td>

Look up Target Groups

</td><td>

Retrieves the target group details associated with given application.

</td></tr><tr><td>

Look up Mobile Device Group by ID

</td><td>

Retrieves details of mobile device group by ID in Jamf.

</td></tr><tr><td>

Look up Mobile Device Groups Stream

</td><td>

Retrieves all the mobile device groups.

</td></tr><tr><td>

Look up User Group by ID

</td><td>

Retrieves details of user group by ID in Jamf.

</td></tr><tr><td>

Look up User Groups Stream

</td><td>

Retrieves all the user groups.

</td></tr><tr><td>

Remove Computer from Static Group

</td><td>

Remove an existing computer from a static group in Jamf.

</td></tr><tr><td>

Remove Mobile Device from Static Group

</td><td>

Remove an existing mobile device from a static group in Jamf.

</td></tr><tr><td>

Remove User from Static Group

</td><td>

Remove an existing user from a static group in Jamf.

</td></tr><tr><td rowspan="4">

Mobile Device Management

</td><td>

Look up Mobile Device Application by ID

</td><td>

Retrieves details of mobile device application by ID from Jamf.**Note:** Configure the system property **com.glide.attachment.max\_get\_size** to customize the size of attachment that can be retrieved. The default value is 5 MB.

</td></tr><tr><td>

Look up Mobile Device Applications Stream

</td><td>

Retrieves all the mobile device applications.

</td></tr><tr><td>

Look up Mobile Device by Serial Number

</td><td>

Retrieves details of mobile device by serial number in Jamf.

</td></tr><tr><td>

Look up Mobile Devices Stream

</td><td>

Retrieves details of all the mobile devices.

</td></tr><tr><td rowspan="3">

User Management

</td><td>

Look up User by ID

</td><td>

Retrieves details of user by ID in Jamf.

</td></tr><tr><td>

Look up User by Name

</td><td>

Retrieves details of user by user name in Jamf.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves all the users.

</td></tr><tr><td rowspan="2">

Software Management

</td><td>

Look up Computer Application Scope

</td><td>

Retrieves scope of a given computer application from the server.

</td></tr><tr><td>

Look up Mobile Device Application Scope

</td><td>

Retrieves scope of a given mobile device application from the server.

</td></tr><tr><td rowspan="5">

Mobile Device Management

</td><td>

Remove Mobile Device Group from Mobile Device Application

</td><td>

Removes a target mobile device group from a mobile device application given the current scope of the application.

</td></tr><tr><td>

Add Mobile Device Group to Mobile Device Application

</td><td>

Adds a target mobile device group to a mobile device application given the current scope of the application.

</td></tr><tr><td>

Add User Group to Mobile Device Application

</td><td>

Adds a target user group to a mobile device application given the current scope of the application.

</td></tr><tr><td>

Remove Mobile Device Group from Mobile Device Application

</td><td>

Removes a target mobile device group from a mobile device application given the current scope of the application.

</td></tr><tr><td>

Remove User Group from Mobile Device Application

</td><td>

Removes a target user group from a mobile device application given the current scope of the application.

</td></tr></tbody>
</table>## Spoke module

The Jamf spoke adds the Jamf application to your instance. The application includes these modules and data accessed through the spoke modules is stored in the respective tables:

|Module|Description|Table|
|------|-----------|-----|
|Applications|Displays the list of applications from the Jamf server.|Application \[sn\_jamf\_spoke\_application\]|
|Groups|Displays the list of groups from the Jamf server.|Group \[sn\_jamf\_spoke\_group\]|
|Configurations|Stores software configuration details for the applications.|Configuration \[sn\_jamf\_spoke\_sf\_config\]|
|Policies|Displays the list of policies from the Jamf server.|Policy \[sn\_jamf\_spoke\_policy\]|
|Server Instances|Stores details of the provider servers.|Server Instance \[sn\_jamf\_spoke\_server\]|

**Note:** These modules and tables are available only when the [Client Software Distribution 2.0 application](csd-app-2-1.md) is installed.

Another table is Jamf Credential \[sn\_jamf\_spoke\_jamf\_credential\] is available that stores details of the credential records. This table is available along with the Jamf spoke and doesn't require installation of the [Client Software Distribution 2.0 application](csd-app-2-1.md).

## Spoke triggers

Use triggers in the Jamf spoke to subscribe to the required events. The endpoint enables webhooks to connect with your ServiceNow instance. You can configure the flows to execute only when the specified trigger conditions are met. The supported events are:

|Category|Trigger|Description|
|--------|-------|-----------|
|Computer Management|Computer Inventory Completed|Trigger initiates when a managed computer submits inventory.|
|Group Management|Smart Group Computer Membership Change|Trigger initiates when a managed computer joins or leaves the membership of a smart computer group.|
|Mobile Device Management|Mobile Device Inventory Completed|Trigger initiates when a device completes the Update Inventory MDM command.|

For information about setting up the triggers for the Jamf spoke, see [Set up triggers for the Jamf spoke](../task/jamf-setup-triggers.md#). For more information about inbound integration, see [Conditional and event-driven inbound integration](../../integrationhub/concept/conditional-and-event-driven-inbound-integration.md).

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Jamf spoke](../task/setup-jamf-spk.md).

