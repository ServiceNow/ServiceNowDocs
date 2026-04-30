---
title: SurveyMonkey Spoke
description: Manage surveys, responses, collectors, and so on in the SurveyMonkey account from your ServiceNow instance.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# SurveyMonkey Spoke

Manage surveys, responses, collectors, and so on in the SurveyMonkey account from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

SurveyMonkey spoke v2.0.6 is the latest version.

## Supported versions

This spoke was built for SurveyMonkey API version v3, but may be compatible with later versions.

## Spoke requirements

Admin access to [SurveyMonkey API Developer Portal](https://developer.surveymonkey.com/).

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the spoke implementation.

## Spoke actions

The SurveyMonkey spoke provides actions to automate SurveyMonkey tasks when events occurs in your ServiceNow instance. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Collector Management|Create Collector|Creates a collector for the given survey. Public app users need access to the Create/Modify Collectors scope.|
|Delete Collector|Deletes the specified collector. Public app users need access to the Create/Modify Collectors scope.|
|Get Collector Details|Retrieves details of the specified collector. Public app users need access to the View Collectors scope.|
|Look up Collectors Stream|Retrieves details of collectors in the specified survey.|
|Contact Management|Add Contacts to Contact List|Creates multiple contacts in a contact list. Public app users need access to the Create/Modify Contacts scope.|
|Create Contact List|Creates a contact list. Public app users need access to the Create/Modify Contacts scope.|
|Delete Contact List|Deletes the specified contact list. Public app users need access to the Create/Modify Contacts scope.|
|Look up Contact Lists|Retrieves all contact lists. Public app users need access to the View Contacts scope.|
|Look up Contacts in Contact List|Retrieves all contacts in a contact list. Public app users need access to the View Contacts scope.|
|Update Contact List|Modifies a contact list. Public app users need access to the Create/Modify Contacts scope.|
|Folder Management|Create Folder|Creates a folder.|
|Look up Folders|Retrieves the available folders.|
|Response Management|Look up Survey Responses|Retrieves a list of responses. Public app users need access to the View Responses scope.|
|Look up Survey Trends|Retrieves the answer counts within the specified time period. Public app users need access to the View Response Details scope.|
|Survey and Question Management|Create Question|Creates a question on the survey page. Public app users need access to the Create/Modify Surveys scope.|
|Create Survey|Creates an empty survey. Public app users need access to the Create/Modify Surveys scope.|
|Delete Question|Deletes the specified question. Public app users need access to the Create/Modify Surveys scope.|
|Delete Survey|Deletes the specified survey. Public app users need access to the Create/Modify Surveys scope.|
|Get Survey Details|Retrieves a list of full responses, including answers to all questions. Public app users need access to the View Response Details scope.|
|Look up Questions|Retrieves all questions in the specified survey.|
|Look up Survey Pages|Retrieves details of the page. Public app users need access to the View Surveys scope.|
|Look up Surveys|Retrieves a list of surveys owned by or shared with the authenticated user. Public app users need access to the View Surveys scope.|
|Update Question|Updates details of the specified question. Public app users need access to the Create/Modify Surveys scope|
|Update Survey|Modifies title, nickname, or language of the specified survey. Public app users need access to the Create/Modify Surveys scope.|
|Team Management|Look up Team Activity Stream|Retrieves activity data for the specified team.|
|Look up Team Member Details|Retrieves details of the specified team member.|
|Look up Team Members Stream|Retrieves details of all members in the specified team.|
|Look up Teams Stream|Retrieves details of all teams that the authenticated user account belongs to.|
|User Management|Get User Details|Retrieves the current user’s account details including their plan. Public app users need access to the View Users scope.|

**Note:** This spoke has a Look up User action and Software Asset Management related actions only.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the SurveyMonkey spoke](../task/setup-surmonkey-dec.md).

