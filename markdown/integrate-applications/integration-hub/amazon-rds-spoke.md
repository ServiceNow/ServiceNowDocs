---
title: Amazon RDS Spoke
description: Integrate ServiceNow instance with Amazon Relational Database Service \(RDS\). Manage the process of performing various operations like set up, operate, and scale on Amazon RDS using this spoke.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Amazon RDS Spoke

Integrate ServiceNow instance with Amazon Relational Database Service \(RDS\). Manage the process of performing various operations like set up, operate, and scale on Amazon RDS using this spoke.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Amazon RDS spoke v1.0.5 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported Versions

This spoke was built for API version 2014-09-01 and 2014-10-31, but may be compatible with later versions.

## Spoke Requirements

-   User with full access to Amazon RDS.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

## Spoke flows and subflows

This spoke has no flows and subflows.

## Spoke actions

The Amazon RDS spoke provides actions to automate Amazon RDS tasks when events occurs in ServiceNow. Available actions include:

<table id="table_jtl_k43_glb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="2">

Account Management

</td><td>

List Account Attributes

</td><td>

Retrieves the list of attributes of an account.

</td></tr><tr><td>

List Certificates

</td><td>

Retrieves the list of certificates of an account.

</td></tr><tr><td>

DB Engines Management

</td><td>

List DB Engines

</td><td>

Retrieves the list of available database \(DB\) engines.

</td></tr><tr><td>

Default

</td><td>

Generate Random Password

</td><td>

Generates a random password.

</td></tr><tr><td rowspan="10">

DB Instance Management

</td><td>

Create DB Instance

</td><td>

Creates an instance of DB.

</td></tr><tr><td>

Create DB Instance Read Replica

</td><td>

Creates a read replica of a DB instance.

</td></tr><tr><td>

Delete DB Instance

</td><td>

Deletes an existing provisioned DB instance.**Note:** When you delete a DB instance, all the automated backups of that instance are also deleted and cannot be recovered.

</td></tr><tr><td>

List DB Instances

</td><td>

Retrieves the list of provisioned DB instances.

</td></tr><tr><td>

List Reserved DB Instances

</td><td>

Retrieves the list of reserved DB instances.

</td></tr><tr><td>

Promote DB Instance Read Replica

</td><td>

Promotes a read replica of a DB instance to standalone DB instance.

</td></tr><tr><td>

Reboot DB Instance

</td><td>

Reboots a DB instance.

</td></tr><tr><td>

Restore DB Instance From DB Snapshot

</td><td>

Creates a DB instance from a DB snapshot.

</td></tr><tr><td>

Start DB Instance

</td><td>

Starts a DB instance.

</td></tr><tr><td>

Stop DB Instance

</td><td>

Stops a DB instance.

</td></tr><tr><td rowspan="4">

DB Snapshots Management

</td><td>

Create DB Snapshot

</td><td>

Creates a snapshot of a DB instance.

</td></tr><tr><td>

Delete DB Snapshot

</td><td>

Deletes a snapshot of a DB instance.

</td></tr><tr><td>

List DB Snapshots

</td><td>

Retrieves the list of snapshots of a DB instance.

</td></tr><tr><td>

Update DB Snapshot

</td><td>

Updates a snapshot of a DB instance.

</td></tr><tr><td rowspan="6">

Event Management

</td><td>

Create Event Subscription

</td><td>

Creates an RDS event notification subscription.

</td></tr><tr><td>

Delete Event Subscription

</td><td>

Deletes an event notification subscription.

</td></tr><tr><td>

List Event Categories

</td><td>

Retrieves a list of categories for the specified or all event source types.

</td></tr><tr><td>

List Event Subscriptions

</td><td>

Retrieves a list of all subscription descriptions of a customer account.

</td></tr><tr><td>

List Events

</td><td>

Retrieves a list of events of the RDS resources.

</td></tr><tr><td>

Update Event Subscription

</td><td>

Updates an existing event notification subscription.

</td></tr><tr><td rowspan="13">

Groups Management

</td><td>

Create DB Parameter Group

</td><td>

Creates a DB parameter group.

</td></tr><tr><td>

Create DB Subnet Group

</td><td>

Creates a DB subnet group. **Note:** A DB subnet group must contain at least one subnet in at least two Availability Zones \(AZ\) in the Amazon Web Services \(AWS\) region.

</td></tr><tr><td>

Create Option Group

</td><td>

Creates an option group.

</td></tr><tr><td>

Delete DB Parameter Group

</td><td>

Deletes the specified DB parameter group. **Note:** Before deleting the DB parameter group, ensure that DB parameter group is not associated with any DB instances.

</td></tr><tr><td>

Delete DB Subnet Group

</td><td>

Deletes a DB subnet group.

</td></tr><tr><td>

Delete Option Group

</td><td>

Deletes an existing option group.

</td></tr><tr><td>

List DB Parameter Groups

</td><td>

Retrieves a list of DB parameter groups.

</td></tr><tr><td>

List DB Subnet Groups

</td><td>

Retrieves a list of DB subnet group descriptions. **Note:** If a DB subnet group name is specified, the list contains descriptions of only the specified DB subnet group.

</td></tr><tr><td>

List Option Groups

</td><td>

Retrieves a list of option groups.

</td></tr><tr><td>

Reset DB Parameter Group

</td><td>

Modifies the parameters of a DB parameter group to the engine or system default values.

</td></tr><tr><td>

Update DB Parameter Group

</td><td>

Updates the parameters of the specified DB parameter group.

</td></tr><tr><td>

Update DB Subnet Group

</td><td>

Updates an existing DB subnet group. **Note:** A DB subnet group must contain at least one subnet in at least twos availability zones \(AZs\) in the Amazon Web Services \(AWS\) region.

</td></tr><tr><td>

Update Option Group

</td><td>

Updates an existing option group.

</td></tr><tr><td rowspan="2">

Logs Management

</td><td>

List DB Log Files

</td><td>

Retrieves a list of all the log files of a DB instance.

</td></tr><tr><td>

View DB Log File

</td><td>

Displays a part of or an entire specified log file. **Note:** The size of the log file must not exceed 1 MB.

</td></tr><tr><td rowspan="3">

Tags Management

</td><td>

Add Tags To RDS Resource

</td><td>

Adds tags to RDS resource.

</td></tr><tr><td>

List Tags For RDS Resource

</td><td>

Retrieves a list of tags of RDS resource.

</td></tr><tr><td>

Remove Tags From RDS Resource

</td><td>

Removes the tags from an RDS resource.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Amazon RDS spoke](../task/setup-amazon-rds.md#).

