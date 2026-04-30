---
title: Amazon Route 53 Spoke
description: Integrate ServiceNow instance with Amazon Route 53. Manage domain registrations, Domain Name System \(DNS\) routing, and health checking from your ServiceNow instance. Also reuse this short description in the release notes.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Amazon Route 53 Spoke

Integrate ServiceNow instance with Amazon Route 53. Manage domain registrations, Domain Name System \(DNS\) routing, and health checking from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Supported versions

This spoke was built for Amazon Route 53 API version 2013-04-01, but may be compatible with later versions.

## Spoke version

Amazon Route 53 spoke v1.0.2 is the latest version.

## Spoke requirements

-   User with full access to Amazon Route 53 account.
-   Access Key ID and Secret Access Key of the user. Record these values for later use.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   Complex Object \(com.glide.cobject\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Amazon Route 53 Spoke provides actions to automate Amazon Route 53 tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_bs1_2qq_qmb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="5">

Domain Management

</td><td>

Check Domain Availability

</td><td>

Checks and returns the availability of a domain name. **Note:** If a domain name is in pending state, you must check the availability of the domain name again, until the status is processed

</td></tr><tr><td>

Get Domain Details

</td><td>

Retrieves detailed information about a specified domain that is associated with the current AWS account.

</td></tr><tr><td>

Look up Domain Suggestions

</td><td>

Retrieves a list of suggested domain names.

</td></tr><tr><td>

Look up Domains

</td><td>

Retrieves all the domain names registered with Amazon Route 53 for the current AWS account.

</td></tr><tr><td>

View Billing

</td><td>

Retrieves all the domain related billing records for the current AWS account for a specified period.

</td></tr><tr><td rowspan="9">

Hosted Zone Management

</td><td>

Create Hosted Zone

</td><td>

Creates a new public or private hosted zone.

</td></tr><tr><td>

Delete Hosted Zone

</td><td>

Deletes a hosted zone.

</td></tr><tr><td>

Get Change

</td><td>

Retrieves the current status of a change batch request.

</td></tr><tr><td>

Get Hosted Zone

</td><td>

Retrieves information about a specified hosted zone.

</td></tr><tr><td>

Get Hosted Zone Count

</td><td>

Retrieves total number of hosted zones for the account.

</td></tr><tr><td>

Get Hosted Zone Limit

</td><td>

Retrieves the specified limit for a specified hosted zone.

</td></tr><tr><td>

Look up Hosted Zones

</td><td>

Retrieves a list of associated public and private hosted zones.

</td></tr><tr><td>

Look up Hosted Zones By Name

</td><td>

Retrieves a list of the hosted zones in alphabetical order.

</td></tr><tr><td>

Update Hosted Zone Comment

</td><td>

Updates the comment for a specified hosted zone.

</td></tr><tr><td rowspan="8">

Record Set Management

</td><td>

Delete GeoLocation Record Set

</td><td>

Deletes a GeoLocation resource record set that contains authoritative DNS information for a specified domain name or subdomain name.

</td></tr><tr><td>

Delete Simple Record Set

</td><td>

Deletes a simple resource record set that contains authoritative DNS information for a specified domain name or subdomain name.

</td></tr><tr><td>

Delete Weighted Record Set

</td><td>

Deletes a weighted resource record set that contains authoritative DNS information for a specified domain name or subdomain name.

</td></tr><tr><td>

Look up Record Sets

</td><td>

Retrieves a list of resource record sets in a specified hosted zone.

</td></tr><tr><td>

Test DNS Answer

</td><td>

Retrieves the value that Amazon Route 53 returns in response to a DNS request for a specified record name and type.

</td></tr><tr><td>

Upsert Geolocation Record Set

</td><td>

Creates a GeoLocation resource record set or updates an existing GeoLocation resource record set that contains authoritative DNS information for a specified domain name or subdomain name.

</td></tr><tr><td>

Upsert Simple Record Set

</td><td>

Creates a simple reocord set or updates an existing simple resource record set that contains authoritative DNS information for a specified domain name or subdomain name.

</td></tr><tr><td>

Upsert Weighted Record Set

</td><td>

Creates a weighted resource record set or updates an existing weighted resource record set that contains authoritative DNS information for a specified domain name or subdomain name.

</td></tr><tr><td rowspan="6">

Tag Management

</td><td>

Add Tags For Domain

</td><td>

Assigns a set of tags to a domain.

</td></tr><tr><td>

Add Tags For Hosted Zone

</td><td>

Assigns a set of tags to a hosted zone.

</td></tr><tr><td>

Look up Tags For Domain

</td><td>

Retrieves a list of tags that are associated with the specified domain.

</td></tr><tr><td>

Look up Tags For Hosted Zone

</td><td>

Retrieves a list of tags that are associated to the specified domain.

</td></tr><tr><td>

Remove Tags From Domain

</td><td>

Removes tags that are associated to a domain.

</td></tr><tr><td>

Remove Tags From Hosted Zone

</td><td>

Removes tags that are associated to a hosted zone.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the Amazon Route 53 spoke](../task/setup-amazon-route53.md#).

