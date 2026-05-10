---
title: Cisco Webex Teams Spoke
description: Manage Cisco Webex Teams from your ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Cisco Webex Teams Spoke

Manage Cisco Webex Teams from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Cisco Webex Teams spoke v2.3.6 is the latest version.

## Supported versions

This spoke was built for Cisco Webex Teams v1, but may be compatible with later versions.

## Spoke requirements

Cisco Webex Teams account.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Cisco Webex Teams Spoke provides actions to automate Cisco Web Teams tasks when events occur in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Membership Management|Create Membership|Creates membership and adds a member to a space using the specified email address. You can choose to make the member as the moderator of the space.|
|Delete Membership|Removes membership from a space for the specified member.|
|Get Membership|Retrieves details for a space membership.|
|Look up Membership|Retrieves a list of all space memberships.|
|Update Membership|Updates details of a space membership.|
|Message Management|Delete Message|Deletes the specified message.|
|Get Message Details|Retrieves details of the specified message.|
|Look up Direct Messages|Retrieves a list of messages in a direct space.|
|Look up Messages|Retrieves all messages in a space.|
|Post Direct Message|Posts a plain text or rich text message to a the specified email address. A file can be specified as an attachment to the message optionally.|
|Post Message to Space|Posts a plain text or rich text message to the specified space. A file can be specified as an attachment to the message optionally.|
|Space Management|Create Space|Creates a space.|
|Delete Space|Deletes the specified space.|
|Get Space Details|Retrieves details of the specified space.|
|Look up Spaces|Retrieves details of the spaces to which the authenticated user belongs.|
|Update Space|Updates details of the specified space.|
|Event Management|Look up Events Stream|Retrieves all events in an organization.|
|People Management|Update Person|Updates details of a person.|
|Delete Person|Deletes details of the specified person.|
|Look up Person Details|Retrieves details of a person.|
|Look up People Stream|Retrieves all people in an organization.|
|Organization Management|Look up Organizations|Retrieves all organizations visible to the authenticated user.|
|Meeting Management|Look up Meetings Stream|Retrieves a list of meetings.|
|License Management|Look up Licenses|Retrieves all licenses for an organization. If the organization ID is not specified, the default is the authenticated user's organization.|
|Look up Roles|Retrieves all authenticated user roles.|

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

You can use OAuth 2.0 or the custom Cisco Webex Credentials to authenticate requests. For information about setting up the spoke, see [Set up the Cisco Webex Teams spoke](../task/setup-cisco-teams.md#).

