---
title: Gremlin Spoke
description: Simulate outages and manage attacks using Gremlin instance from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Gremlin Spoke

Simulate outages and manage attacks using Gremlin instance from your ServiceNow instance.

**Important:**

Starting with the Yokohama release, Gremlin Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Spoke Generator provides the latest experience for this functionality.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Gremlin spoke v1.0.3 is the latest version.

## Supported versions

This spoke was built for Gremlin version v1, but may be compatible with later versions.

## Spoke requirements

-   Set up clients as per your requirement.
-   Admin access to the Gremlin dashboard.
-   Team in your Gremlin account for integration with ServiceNow instance. For more information about creating teams, see [Teams](https://www.gremlin.com/docs/users-and-teams/teams/).
-   Team ID and API Key of the team. Copy and record these value for later use. For more information about accessing these values, see the [Signature-based Authentication](https://www.gremlin.com/docs/infrastructure-layer/authentication/) section.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Gremlin spoke provides actions to automate Gremlin tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_u1p_kh2_hfb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="5">

Attack Management

</td><td>

Create Attack

</td><td>

Creates an attack on the Gremlin platform.

</td></tr><tr><td>

Get Attack Details

</td><td>

Retrieves details about an attack.

</td></tr><tr><td>

Get Attack Executions

</td><td>

Retrieves a list of executions associated with an attack.

</td></tr><tr><td>

Halt All Attacks

</td><td>

Idempotently halts all active attacks across the Gremlin platform.

</td></tr><tr><td>

Look up Attacks

</td><td>

Lists all attacks on the Gremlin platform.**Note:**

-   By default, this action can retrieve data up to 5 MB. You can configure the **glide.pf.rest.response\_payload\_max\_size** property to retrieve data up to 10 MB. If the data in the response is more 10 MB, an error is displayed.
-   As data up to 10 MB only can be retrieved, you can also specify number of records that should be retrieved in the input field, **Number of records to return**.

</td></tr><tr><td rowspan="4">

Attack Schedule Management

</td><td>

Create Attack Schedule

</td><td>

Creates an attack schedule on the Gremlin platform.

</td></tr><tr><td>

Delete Attack Schedule

</td><td>

Deletes the specified attach schedule.

</td></tr><tr><td>

Get Attack Schedule Details

</td><td>

Retrieves details about the specified attack schedule.

</td></tr><tr><td>

Look up Active Attack Schedules

</td><td>

Lists all the attack schedules on the Gremlin platform.

</td></tr></tbody>
</table>**Note:**

-   Time zone that is considered in the spoke actions, is same as the time zone of your ServiceNow instance.
-   Based on your Gremlin license, if you don't have access to certain Gremlin functionality, you can't use the associated spoke actions in your ServiceNow instance as well.
-   For some arguments that take `True` or `False` as input, the actual value that the Gremlin platform considers, might be different from the value you have provided.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Create Connection and Credential record for the Gremlin spoke](../task/create-conn-cred-gremlin.md).

