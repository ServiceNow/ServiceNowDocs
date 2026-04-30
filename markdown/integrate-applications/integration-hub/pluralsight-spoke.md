---
title: Pluralsight Spoke
description: Manage users, learning, courses, and so on in the Pluralsight Skills account from your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Pluralsight Spoke

Manage users, learning, courses, and so on in the Pluralsight Skills account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Pluralsight spoke v1.2.0 is the latest version.

## Supported versions

This spoke was built for Pluralsight GraphQL API version v1, but may be compatible with other future API versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The Pluralsight spoke provides actions to automate Pluralsight tasks when events occurs in your ServiceNow instance. Available actions include:

<table id="table_ny4_jvb_h4b"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Course Management

</td><td>

Look up Courses

</td><td>

Retrieves details of the specified Pluralsight courses.

</td></tr><tr><td rowspan="3">

Learning Management

</td><td>

Look up Learning Status for Course

</td><td>

Retrieves the learning status of the specified Pluralsight course.

</td></tr><tr><td>

Look up Learning Status for User

</td><td>

Retrieves the learning status for the specified Pluralsight user.

</td></tr><tr><td>

Look up Learning Status Data Stream

</td><td>

Retrieves the learning status of the specified course in Pluralsight.

</td></tr><tr><td rowspan="3">

Skill Management

</td><td>

Look up Skill Assessment Results

</td><td>

Retrieves the skill assessment results in Pluralsight.**Note:**

-   Pluralsight Enterprise Plan is required to use this action.
-   The action output, **Attempt Number** starts with **0** and this value is synchronised with value from Pluralsight.

</td></tr><tr><td>

Look up Skill Assessments

</td><td>

Retrieves the list of all available skill assessments in Pluralsight that can be taken by a user.

</td></tr><tr><td>

Look up Skill IQ Summary

</td><td>

Retrieves the skill IQ summary in Pluralsight.

</td></tr><tr><td rowspan="4">

User Management

</td><td>

Create User

</td><td>

Creates a user in Pluralsight.**Note:** API key must have the write permission to perform this action.

</td></tr><tr><td>

Deactivate User

</td><td>

Removes a user’s license from plan in Pluralsight.**Note:** API key must have the write permission to perform this action.

</td></tr><tr><td>

Invite User

</td><td>

Invites the specified user to a plan in Pluralsight.**Note:** API key must have the write permission to perform this action.

</td></tr><tr><td>

Look up Users

</td><td>

Retrieves details of the users in Pluralsight.

</td></tr></tbody>
</table>See [Set up the Pluralsight spoke](../task/setup-pluralsight-spk.md) for information about setting up the Pluralsight spoke.

