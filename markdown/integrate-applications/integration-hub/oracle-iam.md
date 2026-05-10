---
title: Oracle Cloud IAM Spoke
description: Manage user identities and user access in Oracle Infrastructure Identity and Access Management \(IAM\) from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Oracle Cloud IAM Spoke

Manage user identities and user access in Oracle Infrastructure Identity and Access Management \(IAM\) from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Oracle Cloud IAM spoke v1.1.3 is the latest version.

## Supported versions

This spoke was built for Oracle Cloud IAM 20160918, but may be compatible with later versions.

## Spoke requirements

Oracle Cloud account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Oracle Cloud IAM spoke provides actions to automate Oracle Cloud IAM tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Compartment Management|Bulk Delete Resources|Deletes multiple resources from the specified compartment in a batch.|
|Bulk Move Resources|Moves multiple resources from one compartment to another compartment in a batch.|
|Create Compartment|Creates a child compartment in the specified parent compartment.|
|Get Compartment|Retrieves details of the specified compartment.|
|Look up Compartments|Retrieves a list of compartments in the specified tenancy.|
|Move Compartment|Moves the specified child compartment to a different parent compartment in the same tenancy.|
|Recover Compartment|Recovers a deleted compartment and changes its state to active.|
|Update Compartment|Updates the specified compartment.|
|Group Management|Create Group|Creates a group in the specified tenancy.|
|Delete Group|Deletes the specified group.|
|Get Group|Retrieves information about the specified group.|
|Look up Groups|Retrieves a list of groups in the specified tenancy.|
|Update Group|Updates the specified group.|
|OCI Metadata|Get Tenancy|Retrieves information about the specified tenancy.|
|Look up Available Domains|Retrieves a list of availability domains in the specified tenancy.|
|Look up Regions|Retrieves a list of all the regions offered by Oracle Cloud Infrastructure.|
|Policy Management|Create Policy|Create a policy in the specified compartment.|
|Delete Policy|Deletes the specified policy.|
|Get Policy|Retrieves information of the specified policy.|
|Look up Policies|Retrieves a list of policies in the specified compartment.|
|Update Policy|Updates the specified policy.|
|User Management|Add User to Group|Adds the specified user to the specified group.|
|Create User|Creates a user.|
|Delete User|Deletes the specified user.|
|Get User|Retrieves the details of the specified user.|
|Look up User Group Membership|Retrieves a list of the user group memberships in the specified tenancy.|
|Look up Users|Retrieves a list of the users in the specified tenancy.|
|Remove User from Group|Removes a user from a group by deleting the corresponding user group membership.|
|Update User|Updates details of the specified user.|
|Update User Capabilities|Updates capabilities of the specified user.|
|Update User State|Unblocks the specified user.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

For information about setting up the spoke, see [Set up the Oracle Cloud IAM spoke](../task/setup-oracle-iam.md#).

