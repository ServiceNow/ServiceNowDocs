---
title: Amazon Connect Spoke
description: Manage and provide customer service across voice, chat, and tasks using your Amazon Connect account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Amazon Connect Spoke

Manage and provide customer service across voice, chat, and tasks using your Amazon Connect account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Amazon Connect spoke v1.2.0 is the latest version.

## Supported versions

This spoke was built for Amazon Connect API Version 2017-08-08, but may be compatible with later versions.

## Spoke requirements

-   User with full access to Amazon Connect.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

For more information about creating user in IAM and providing the required access, see [Understanding and Getting Your Security Credentials](https://docs.aws.amazon.com/general/latest/gr/aws-sec-cred-types.html) page on the [AWS Documentation](https://docs.aws.amazon.com/index.html) site.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Amazon Connect spoke provides actions to automate Amazon Connect tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_yrc_p4t_f4b"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="5">

Contact Flow Management

</td><td>

Create Contact Flow

</td><td>

Creates a contact flow for the specified Amazon Connect instance.

</td></tr><tr><td>

Get Contact Flow Details

</td><td>

Retrieves details of the specified contact flow.

</td></tr><tr><td>

Look up Contact Flows

</td><td>

Retrieves a list of contact flows.

</td></tr><tr><td>

Update Contact Flow Content

</td><td>

Updates content of the specified contact flow.

</td></tr><tr><td>

Update Contact Flow Name

</td><td>

Updates name of the specified contact flow.

</td></tr><tr><td rowspan="8">

Contact Management

</td><td>

Resume Contact Recording

</td><td>

Resumes recording the call when a contact is being recorded and the recording has been suspended using suspend contact recording. Only voice recordings are supported at this time.

</td></tr><tr><td>

Start Contact Recording

</td><td>

Starts recording the contact when an agent joins the call. Only voice recordings are supported at this time.

</td></tr><tr><td>

Start Outbound Voice Contact

</td><td>

Places an outbound call to a contact and initiates the contact flow.

</td></tr><tr><td>

Stop Contact

</td><td>

Ends the specified contact.

</td></tr><tr><td>

Stop Contact Recording

</td><td>

Stops recording the call. If you use stop contact recording to stop recording an ongoing call, you can't use restart the contact recording. Only voice recordings are supported at this time.

</td></tr><tr><td>

Suspend Contact Recording

</td><td>

Suspends recording the call when a contact is being recorded.

</td></tr><tr><td>

Get Contact Attributes

</td><td>

Retrieves the contact attributes for the specified contact.

</td></tr><tr><td>

Update Contact Attributes

</td><td>

Creates or updates user-defined contact attributes associated with the specified contact.

</td></tr><tr><td rowspan="9">

Instance Management

</td><td>

Create Instance

</td><td>

Initiates an Amazon Connect instance with all the supported channels enabled.

</td></tr><tr><td>

Delete Instance

</td><td>

Deletes the specified instance.

</td></tr><tr><td>

Get Instance Details

</td><td>

Retrieves details of the specified instance.

</td></tr><tr><td>

Look up Hours of Operations

</td><td>

Retrieves a list of hours of operations.

</td></tr><tr><td>

Look up Instances

</td><td>

Retrieves a list of instances.

</td></tr><tr><td>

Look up Phone Numbers

</td><td>

Retrieves a list of phone numbers.

</td></tr><tr><td>

Look up Prompts

</td><td>

Retrieves a list of prompts.

</td></tr><tr><td>

Look up Queues

</td><td>

Retrieves a list of queues.

</td></tr><tr><td>

Look up Security Profiles

</td><td>

Retrieves a list of security profiles.

</td></tr><tr><td rowspan="2">

Metric Management

</td><td>

Get Current Metrics Data

</td><td>

Retrieves the real-time metric data from the specified Amazon Connect instance.

</td></tr><tr><td>

Get Metrics Data

</td><td>

Retrieves historical metric data from the specified Amazon Connect instance.**Note:**

-   The time must be specified using an interval of 5 minutes, such as 11:00, 11:05, and 11:10, and must be later than the start time timestamp.
-   The time range between the start and end time must be less than 24 hours.

</td></tr><tr><td rowspan="10">

Routing Policy Management

</td><td>

Associate Routing Profile Queues

</td><td>

Associates a set of queues with a routing profile.

</td></tr><tr><td>

Create Routing Profile

</td><td>

Creates a routing profile.

</td></tr><tr><td>

Disassociate Routing Profile Queues

</td><td>

Disassociates the specified set of queues from a routing profile.

</td></tr><tr><td>

Get Routing Profile Details

</td><td>

Retrieves details of the specified routing profile.

</td></tr><tr><td>

Look up Routing Profile Queues

</td><td>

Retrieves a list of routing profile queues.

</td></tr><tr><td>

Look up Routing Profiles

</td><td>

Retrieves a list of routing profiles.

</td></tr><tr><td>

Update Routing Profile Concurrency

</td><td>

Updates the specified routing profile concurrency.

</td></tr><tr><td>

Update Routing Profile Default Outbound Queue

</td><td>

Updates the specified routing profile default outbound queue.

</td></tr><tr><td>

Update Routing Profile Name

</td><td>

Updates the specified routing profile name.

</td></tr><tr><td>

Update Routing Profile Queues

</td><td>

Updates the properties associated with a set of queues for a routing profile.

</td></tr><tr><td rowspan="3">

Tag Management

</td><td>

Add Tags to Resource

</td><td>

Associates a set of tags with the specified resource.

</td></tr><tr><td>

Look up Tags for Resource

</td><td>

Retrieves all tags that are associated with the specified resource.

</td></tr><tr><td>

Remove Tag from Resource

</td><td>

Removes the association of tag from resource.

</td></tr><tr><td rowspan="13">

User Management

</td><td>

Create User

</td><td>

Creates a user account for the specified Amazon Connect instance.

</td></tr><tr><td>

Delete User

</td><td>

Deletes the specified user.

</td></tr><tr><td>

Get User Details

</td><td>

Retrieves details of the specified user.

</td></tr><tr><td>

Get User Hierarchy Group

</td><td>

Retrieves details of the user hierarchy group.

</td></tr><tr><td>

Get User Hierarchy Structure

</td><td>

Retrieves details of the user hierarchy structure.

</td></tr><tr><td>

Look up User Hierarchy Groups

</td><td>

Retrieves a list of user hierarchy groups.

</td></tr><tr><td>

Look up Users

</td><td>

Retrieves the list of users.

</td></tr><tr><td>

Update User Hierarchy

</td><td>

Updates the specified user hierarchy.

</td></tr><tr><td>

Update User Identity Information

</td><td>

Updates the specified user identify information.

</td></tr><tr><td>

Update User Phone Configuration

</td><td>

Updates details of the specified user phone configuration.

</td></tr><tr><td>

Update User Routing Profile

</td><td>

Updates the specified user routing profile.

</td></tr><tr><td>

Update User Security Profiles

</td><td>

Updates details of the specified user security profiles.

</td></tr><tr><td>

Look up Agent Status

</td><td>

Retrieves a list of agent statuses.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Amazon Connect spoke](../task/setup-amzn-connect.md).

