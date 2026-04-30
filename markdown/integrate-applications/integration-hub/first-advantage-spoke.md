---
title: First Advantage Spoke
description: Manage and track the background verifications of candidates using First Advantage from your ServiceNow instance. Manage users, accounts, candidates, invites, and orders in First Advantage from your ServiceNow instance.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# First Advantage Spoke

Manage and track the background verifications of candidates using First Advantage from your ServiceNow instance. Manage users, accounts, candidates, invites, and orders in First Advantage from your ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## IntegrationHub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

First Advantage spoke v1.8.0 is the latest version.

## Supported versions

This spoke was built for First Advantage API version v1.1, but may be compatible with later versions.

## Spoke requirements

-   First Advantage account
-   API key

    **Note:** Contact the First Advantage team to obtain the API key.

-   Account ID

    **Note:** Contact the First Advantage team to obtain the Account ID.


## Spoke flows

The First Advantage spoke provides sample flows to demonstrate automating the First Advantage tasks. To customize a sample flow, copy it to a new application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|First Advantage - Candidate Background Verification using Invite|Initiates background check of the candidate using invite. Sends a request to the candidate to complete an application. For information about creating a case, see [Create a case in First Advantage from ServiceNow](../task/create-fadv-case-1.md).|
|First Advantage - Candidate Background Verification using Order|Initiates background check of the candidate using order. An order record is created and request to provide essential details is sent to the candidate. For information about creating a case, see [Create a case in First Advantage from ServiceNow](../task/create-fadv-case-1.md).|
|First Advantage - \(Order As\) Candidate Background Verification using Order|Initiates background check of the candidate using order and places order on behalf of the required user.|
|First Advantage - \(Order As\) Candidate Background Verification using Invite|Initiates background check of the candidate using invite and places order on behalf of the required user.|

## Spoke subflows

The First Advantage spoke provides a sample subflow to demonstrate automating First Advantage tasks. To customize the sample subflow, copy it to a new application scope. Available sample subflow is, Get Packages. The subflow retrieves packages in First Advantage and stores the details in the Packages table.

## Spoke actions

The First Advantage spoke provides actions manage accounts, candidates, invites, orders, and users when events occur in ServiceNow. Available actions include:

|Category|Action|Description|
|--------|------|-----------|
|Account Management|Get Account Details|Retrieves details of the First Advantage account.|
|Get Account Packages|Retrieves the details of all the packages in an account.|
|Get Account Profiles|Retrieves the details of all profiles in an account.|
|Get Account Users|Retrieves the details of all users in an account.|
|Candidate Management|Create New Candidate|Creates a candidate profile for background verification.|
|Get Candidate By Candidate ID|Retrieves the details of the required candidate.|
|Get Documents For A Specific Candidate|Retrieves the documents associated with the required candidate.|
|Get Monitoring Product Details For A Specific Candidate|Retrieves the details of the monitoring product for the required candidate.|
|Update Candidate Details|Updates the details of a candidate profile.|
|Invite Management|Create Invite|Create an invite for the candidate to fill the application.|
|Get Invite Status By Applicant ID|Retrieves the latest status of the invite for the required applicant.|
|Get Invite View Link By Application ID|Retrieves a secure link to access the profile that the candidate must complete.|
|Order Management|Create Order|Creates a First Advantage screening order.|
|Get Order Report By Order ID|Retrieves the completed order report for the required order.|
|Get Order Status By Order ID|Retrieves the latest order status for the required order.|
|User Management|Activate User|Activates the required user.|
|Create User|Creates a user profile.|
|Deactivate User|Deactivates the required user.|
|Update User Password|Updates the password of the required user.|
|Update User Profile|Updates information in the profile of the required user.|

## Spoke module

The First Advantage spoke adds a First Advantage spoke module to your ServiceNow instance. The First Advantage spoke synchronizes and stores information about First Advantage cases, tasks, employee tasks, order tasks, and packages.

The First Advantage spoke includes these modules:

|Module|Description|
|------|-----------|
|Accounts|Enables you to view the details of all accounts available in First Advantage. To view the account details, you must set up the spoke and synchronise the accounts.|
|FADV Webhook Client Details|Enables you to set up First Advantage webhook by providing key for the First Advantage webhook client.|
|Create New First Advantage Case|Enables you to initiate the background check of the required candidate using invite or order from ServiceNow.|
|First Advantage Cases|Enables you to view list of all First Advantage cases created using invite and order.|
|Packages|Enables you to view the details of all packages available in First Advantage. To view the package details, you must set up the spoke and synchronise the packages.|
|Order Tasks|Enables you to view list of all First Advantage order records.|
|Employee Tasks|Enables you to view list of all First Advantage cases created using invite.|

The First Advantage spoke includes the these tables:

-   First Advantage Task \[sn\_fadv\_spoke\_first\_advantage\_task\]
-   First Advantage Employee Task \[sn\_fadv\_spoke\_first\_advantage\_employee\_task\_table\]
-   Packages \[sn\_fadv\_spoke\_packages\]
-   FADV Webhook Client Details \[sn\_fadv\_spoke\_webhook\_client\_details\]

|Table|Description|
|-----|-----------|
|First Advantage Task|Details of all the First Advantage order records.|
|First Advantage Employee Task|Details of all the First Advantage invite records.|
|Packages|First Advantage packages that are synchronized with ServiceNow®.|
|FADV Webhook Client Details|Client details to set up the First Advantage webhook.|

## Spoke user roles

-   First Advantage admin
-   First Advantage user

Only users with the First Advantage admin role can view the **FADV Webhook Client Details** module.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up the First Advantage spoke](../task/setup-first-adv.md#).

