---
title: UKG Spoke
description: Manage time off requests in Kronos from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# UKG Spoke

Manage time off requests in Kronos from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

UKG spoke v3.3.0 is the latest version.

## Supported versions

This spoke was built for Kronos version v1, but may be compatible with later versions.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Complex Object \(com.glide.cobject\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Flow Designer - Dynamic Inputs \(com.glide.hub.dynamic\_inputs\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Spoke flows

The UKG spoke provides sample flows to demonstrate automating the Kronos tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Kronos - Create Manager Time Off Request|Creates the time of request for a manager or employee.|
|Kronos - Get New Refresh And Access Token|Retrieves access token for Kronos and generates a new refresh token periodically.|
|Kronos - Refresh The Access Token|Refreshes the access token for Kronos.|
|Kronos - Retrieve And Update Manager Time Off Request Status|Retrieves status of the time off request status and updates the details of the associated request item.|
|Kronos - Time Off Details House Keeping|Deletes the time off requests based on the provided criteria. By default, the flow deletes time off requests that have been approved 7 days ago.|

Every flow triggers an associated subflow.

## Spoke subflows

The Kronos spoke provides sample subflows to demonstrate automating Kronos tasks. To customize a sample subflow, copy it to a new application scope. Available sample subflows include:

|Subflow|Description|
|-------|-----------|
|Kronos - Get Kronos Token|Uses the details provided during spoke setup to retrieve a valid refresh token from Kronos.|
|Kronos - Create Manager Time Off Request|Creates the time off request and saves the information in your ServiceNow instance.|
|Kronos - Manager Time Off Request|Creates the time off request for a manager or employee.|
|Kronos - Retrieve Manager Time Off Request Status Update|Retrieves status of the time off request status and updates the details of the associated request item.|
|Kronos - Time Off Request Housekeeping|Deletes the time off requests based on the provided criteria. By default, the subflow deletes time off requests that have been approved 7 days ago.|
|Kronos - Report Missed Punches as Employee|This subflow creates a task which allows the employee's manager to punch the employee's missing entry.|

## Spoke actions

The UKG spoke provides actions to automate Kronos tasks when events occurs in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Authentication Management|Get Kronos Refresh Token|Retrieves the Refresh Token for Kronos.|
|Get Kronos Token|Retrieves the Token for Kronos.|
|Persons|Create Persons|Creates records for one or more persons.|
|Retrieve Person by ID|Retrieves the details of a person for the specified record ID.|
|Retrieve Persons|Retries the record details of a list of persons based on the search criteria.|
|Update Persons|Updates the records of one or more persons.|
|Scheduling|Retrieve Manager Schedule|Retrieves the schedule of a list of employees.|
|Default|Add Timestamp|Adds or records a timestamp for a punch transaction of an employee.|
|Approve Timecard Employee|Approves the employee timecard for the specified range of dates.|
|Approve Timecard Manager|Adds manager approval for the specified employee's timecard.|
|Look up Shift Cover Requests as Manager|Retrieves one or more shift cover requests matching specified search criteria.|
|Look up Open Shifts Requests Manager|Retrieves a list of Open Shift Requests based on the Employee ID or Person Number.|
|Look up Self Schedule Requests Manager|Retrieves a list of Self Schedule requests based on the Employee ID or Person Number.|
|Look up Shift Swap Requests Manager|Retrieves a list of swap requests based on the Employee ID or Person Number.|
|Look up Manager Availability Requests|Retrieves all availability requests for the given criteria.|
|Retrieve Employee Timecard Request|Retrieves the timecard details of the specified employee.|
|Retrieve Employee Timecards Request|Retrieves the details of a list of timecards for the specified employees or for the specified Hyperfind details.|
|Retrieve Manager Timecard|Retrieves the timecard of the specified manager.|
|Retrieve Manager Timecards|Retrieves the details of a list of timecards for the specified mangers or the specified Hyperfind details.|
|Retrieve Timecard Approvals Employee|Retrieves a list of employee timecard approvals for the specified date range.|
|Retrieve Timecard Approvals Manager|Returns a list of manager timecard approvals for the specified date range.|
|Update Timecard|Updates the timecard of the specified employee.|
|Metadata Retrieval|Get Accrual Codes|Retrieves a list of accrual code types according to the user's access rights.|
|Look Up Cost Centers|Retrieves a list of available cost centers.|
|Look Up Jobs|Retrieves a list of available jobs.|
|Look Up Labor Categories|Retrieves a list of available categories.|
|Look Up Labor Category Entries|Retrieves a list of available labor category entries.|
|Look Up Work Rules|Retrieves a list of available work rules.|
|Retrieve Hyperfind Queries|Retrieves a list of Hyperfind queries.|
|Retrieve Licenses|Retrieves a list of licenses.|
|Retrieve Pay Rules|Retrieves a list of pay rules.|
|Retrieve Symbolic Period ID|Retrieves the specified symbolic period.|
|Retrieve All Pay Codes|Retrieves all the play code in Kronos.|
|Retrieve Employee Request Subtype|Retrieves a list of request subtypes associated with the required Person Number.|
|Retrieve Manager Request Subtype By Employee ID|Retrieves a list of request subtypes associated with the required Employee ID.|
|Retrieve Manager Request Subtype By Person Number|Retrieves a list of request subtypes associated with the required Person Number. The action output is necessary for subsequent actions such as, the Retrieve Employee Accrual Balance action from manager’s perspective.|
|Retrieve Manager Symbolic Amount Qualifiers By Employee ID|Retrieves different types of Retrieve Manager Symbolic Amount Qualifiers By Employee ID, such as half day, full day, and so on, based on Employee ID.|
|Retrieve Manager Symbolic Amount Qualifiers By Person Number|Retrieves different types of Retrieve Manager Symbolic Amount Qualifiers By Employee ID, such as half day, full day, and so on, based on Person Number.|
|Retrieve Symbolic Periods|Retrieves all the symbolic periods.|
|Scheduling Management|Create Employee Time Off Request|Creates a time off request based on the provided inputs.|
|Create Manager Time Off Requests|Creates a time off request based on the provided inputs.|
|Look up Employee Schedule|Retrieves the schedule of the employee.|
|Retrieve Employee Accrual Balance|Retrieves details of the different types of employee accrual balance, such as PTO, sick days, and so on.|
|Retrieve Employee Time Off Requests|Retrieves details of the time off requests based on the specified search criteria.|
|Retrieve Manager Accrual Balance By Employee ID|Retrieves details of the different types of manager accrual balance using Employee ID.|
|Retrieve Manager Accrual Balance By Person Number|Retrieves details of the different types of manager accrual balance using Person Number.|
|Retrieve Manager Time Off Requests By Employee ID|Retrieves details of the time off requests based on the specified search criteria and Employee ID.|
|Retrieve Manager Time Off Requests By Person Number|Retrieves details of the time off requests based on the specified search criteria and Person Number.|
|Update Employee TimeOff Request|Updates the state of an employee time off request.|
|Update Manager Time Off Requests|Updates the state of a manager time off request.|
|Timekeeping|Get Employee Accruals by Person Number|Retrieves different types of employee accrual balances.|
|Retrieve Timecard Approvals Manager|Retrieves a list of timecard approvals within the specified date range.|

## Spoke module

The Kronos spoke adds a Kronos application to your ServiceNow instance. The Kronos application has these modules.

|Module|Description|
|------|-----------|
|Credentials|Details of the Kronos users with permissions to perform the required actions.|
|Time Off Request Details|Details of the time off requests, along with the status.|
|Time Off Request Details Staging Tables|Details of the time off requests from the staging tables.|

## Kronos spoke account requirements

The Kronos spoke requires registering an OAuth 2.0 application in your Kronos account to generate OAuth 2.0 tokens for the Kronos spoke. Record the generated Client ID, Client Secret, and Application key for later use.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

For information about setting up the spoke, see [Set up the UKG spoke](../task/setup-kronos.md#).

