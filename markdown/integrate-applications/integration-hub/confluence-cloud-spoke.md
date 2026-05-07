---
title: Confluence Cloud Spoke
description: The Confluence Cloud spoke provides actions to manage groups, group members, and search content in your Confluence Atlassian account.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Confluence Cloud Spoke

The Confluence Cloud spoke provides actions to manage groups, group members, and search content in your Confluence Atlassian account.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Confluence Cloud spoke v2.0.1 is the latest version.

## Supported versions

This spoke was built for the Confluence Cloud REST API.

## Spoke requirements

Atlassian site admin account

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Confluence Cloud spoke provides actions to automate Confluence Cloud tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_x3t_dvq_n4b"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account Management

</td><td>

Look up Accessible Resources

</td><td>

Retrieves sites with scopes that are granted by the OAuth token.

</td></tr><tr><td rowspan="3">

Content Management

</td><td>

Look up Pages Stream

</td><td>

Retrieves a list of pages in a Confluence space.

 Inputs:

-   Page size: Limit number of pages returned per request.
-   Query \(Optional\): Use query input to filter status of pages \(for example, `status=archived`\).

Values include: current, archived, deleted, and trashed.


</td></tr><tr><td>

Look up Spaces Stream

</td><td>

Retrieves a list of Confluence spaces.

 Inputs: Page size.

 Number of Space entries expected to be fetched per page.

</td></tr><tr><td>

Search Content

</td><td>

Retrieves the list of content based on the provided query.

</td></tr><tr><td rowspan="3">

Group Management

</td><td>

Look up Groups

</td><td>

Retrieves all groups in the Atlassian account, including default groups.

</td></tr><tr><td>

Look up Members By Group ID

</td><td>

Retrieves all active users within the specified group.

</td></tr><tr><td>

Remove Member From Group By Group ID

</td><td>

Removes a user from the specified group.

</td></tr><tr><td rowspan="2">

User Management

</td><td>

Look up Group Memberships For User

</td><td>

Retrieves information about the groups that the user is a member of.

</td></tr><tr><td>

Report Personal Data

</td><td>

Reports a user’s personal data for the specified apps.

</td></tr></tbody>
</table>**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Spoke module

The Confluence Cloud spoke adds the Confluence Cloud application to your instance and includes these modules:

|Module|Description|
|------|-----------|
|Confluence Groups|Enables you to specify the groups that have access to Confluence products. By specifying these groups, you can manage the users within only these groups using the Confluence Cloud spoke.|

Data accessed through these spoke modules is stored in these tables:

<table id="table_ajt_dvq_n4b"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Confluence Groups

</td><td>

Displays the list of groups that have access to Confluence products.

</td><td>

-   Group Name
-   Group ID

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Confluence Cloud spoke](../task/setup-confluence-cloud.md#).

