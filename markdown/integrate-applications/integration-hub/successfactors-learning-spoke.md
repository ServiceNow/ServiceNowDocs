---
title: SuccessFactors Learning Spoke
description: SuccessFactors Learning spoke can be used retrieve all learning-related information such as user data, course data, syncing user activity, retrieving assignments/enrollments, etc.Also reuse this short description in the release notes.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-10"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# SuccessFactors Learning Spoke

SuccessFactors Learning spoke can be used retrieve all learning-related information such as user data, course data, syncing user activity, retrieving assignments/enrollments, etc.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

## Supported versions

This spoke was built for version 1.5, but may be compatible with later versions.

## Key features

SuccessFactors Learning enables a flow designer to:

-   Retrieve learning information
-   User data
-   Course data
-   Syncing user activity

## Spoke requirements

-   -   
## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   TBD
-   TBD

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke flows

The SuccessFactors Learning provides sample flows to demonstrate automating the Learning tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
| | |
| | |

## Spoke subflows

The SuccessFactors Learning provides sample subflows to demonstrate automating Learning tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Look up users|Retrieve user related information.|
|Look up courses|Retrieve course related information.|

## Spoke actions

The SuccessFactors Learning provides actions to automate Learning tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_or3_2vk_zdc"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Meta data retrieval

</td><td>

Get access token

</td><td>

Retrieves access token from SuccessFactors Learning.

</td></tr><tr><td>

User management

</td><td>

Look up users

</td><td>

Retrieves user details from SuccessFactors Learning.

</td></tr><tr><td rowspan="5">

Course management

</td><td>

Look up courses

</td><td>

Retrieves courses details from SuccessFactors Learning.

</td></tr><tr><td>

Look up user activities

</td><td>

Retrieves user activities from SuccessFactors Learning.

</td></tr><tr><td>

Track approvals

</td><td>

Retrieves approvals from SuccessFactors Learning.

</td></tr><tr><td>

Look up enrollment

</td><td>

: Retrieves enrollment details from SuccessFactors Learning.

</td></tr><tr><td>

Create assignment enrollment

</td><td>

Create assignment enrollment into SuccessFactors Learning.

</td></tr></tbody>
</table>## Spoke module

Data accessed through these spoke modules is stored in these tables:

|Table|Description|Fields|
|-----|-----------|------|
|| | |
| | | |

## Spoke user roles

The SuccessFactors Learning provides these user roles to control access to data:

|User role|Description|
|---------|-----------|
| | |
| | |

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.



