---
title: Guidewire Spoke
description: Integrate a ServiceNow instance with your Guidewire account to look up insurance customer and policy information, and manage claims. Also reuse this short description in the release notes.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Guidewire Spoke

Integrate a ServiceNow instance with your Guidewire account to look up insurance customer and policy information, and manage claims.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Subscription information

This spoke requires a subscription. Contact your ServiceNow account manager or sales representative for subscription details. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf)

## Supported versions

This spoke was built for Guidewire application programming interface \(API\) version Elysian \(2022.05\), but may be compatible with later versions. This spoke also supports APIs on Guidewire Cloud InsuranceSuite.

## Key features

Guidewire spoke application enables a flow designer to build workflows from actions which call the Guidewire InsuranceSuite cloud APIs. These actions can be called from any subflows within the insurance applications which provide real-time integration with Guidewire. Manage ClaimCenter, PolicyCenter, and ContactManager actions that:

-   Create, cancel, submit, validate, update, and close claims.
-   Manage customer contact details.
-   Retrieve policies associated with the customer.
-   Delete or change claim details.
-   Add notes to claims.

## Spoke requirements

Guidewire account

## Spoke dependencies

Ensure that these dependent plugins are installed:

-   ServiceNow Integration Hub Runtime \(com.glide.hub.integration.runtime\)
-   ServiceNow Integration Hub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow Integration Hub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)

**Note:** If used outside the spoke implementation, some of these plugins are licensable features and need appropriate licenses.

## Spoke actions

The Guidewire spoke provides actions to trigger Guidewire's cloud InsuranceSuite processes when events happen in your ServiceNow instance. This spoke integrates with most APIs from Guidewire's ContactManager, PolicyCenter, and ClaimCenter relevant to auto and property insurance claims. You can extend and customize the available actions for your business needs.

**Note:**

-   Across all Guidewire actions included in this spoke, only a subset of the fields from Guidewire responses are parsed into the action outputs. This spoke returns the entire Guidewire JSON response.
-   Streaming actions retrieve records individually instead of the entire list simultaneously.

Available actions include the following.

|Category|Action|Description|
|--------|------|-----------|
|Contact Management|Look up Companies in Contacts Stream|Retrieves a stream of company contact records from Guidewire's ContactManager based on search parameters.|
|Look up Company Contact from Contact Manager by Contact ID|Retrieves the details of a company contact record using its Contact ID from Guidewire's ContactManager.|
|Look up Contact Manager Typelist|Enumerates the available values for a specific Typelist in ContactManager. The Typelist name is provided in the description of each field that uses a Typelist enumeration.|
|Look up Person Contact from Contact Manager by Contact ID|Retrieves the details of a person contact record using its Contact ID from Guidewire's ContactManager.|
|Look up Persons in Contacts Stream|Retrieves a list of person contact records from Guidewire's ContactManager based on search parameters.|

|Category|Action|Description|
|--------|------|-----------|
|Policy Management|Bind and Issue Policy Transaction|Initiates validation of data to make coverage become effective, and triggers the creation of a binding document.|
|Initiate Policy Cancellation|Begins the cancellation process by selecting the specified policy and providing the necessary information and reason for cancellation.|
|Look up Company Account by Account ID|Retrieves information about a company's account, including all of its policies, and other interactions, based on its account ID.|
|Look up Company Accounts Stream|Retrieves a stream of all company account records from the Guidewire system that match the input criteria. Information retrieved may include details such as the company's name, contact information, and other relevant information.|
|Look up Insurance Policies Stream|Retrieves a list of insurance policies from the Guidewire PolicyCenter application. Retrieved information can include policy numbers, effective dates, expiration dates, coverages, endorsements, and other relevant information.|
|Look up Insurance Policy by Policy ID|Retrieves information about an insurance policy based on its policy ID. Information retrieved may include a policy's effective date, expiration date, policy limits, deductibles, endorsements, and other relevant information about provided coverage.|
|Look up Person Account by Account ID|Retrieves information about a person's account, including the IDs of all their policies and account details such as First Name, Last Name, and Preferred Currency, based on their account ID.|
|Look up Person Accounts Stream|Retrieves a stream of all person account records from the Guidewire system. Retrieved information may include details such as the person's name, contact information, policy details, and other relevant information.|
|Look up Policy Center Typelist|Enumerates the available values for a specific Typelist in PolicyCenter. The Typelist name is provided in the description of each field that uses a Typelist enumeration.|
|Look up Policy Contact by Contact ID|Retrieves the details of a policy contact record using its Contact ID from Guidewire's PolicyManager.|
|Look up Policy Document Content by Document ID|Retrieves the content of a specific policy document using its unique document ID.|
|Look up Policy Document Content by Policy ID Stream|Retrieves the policy content of all documents associated with the specified policy using the policy ID stream.|
|Look up Policy Locations by Policy ID|Retrieves a list of physical locations associated with a specified insurance policy, based on the policy ID, returning information such as the mailing address, billing address, and property address.|
|Look up Product by Product ID|retrieve information about the specific insurance product, based on the product ID.|
|Look up Product Coverables by Line ID Stream|Retrieves information about the coverages and options associated with a specific insurance product line, based on the line ID.|
|Look up Product Coverable Coverages on Line by Coverable ID Stream|Retrieves information about the various types of insurance coverage offered by an insurance product, by the ID assigned to each type of coverage within the product.|
|Look up Product Coverages by Line ID Stream|Retrieves information about product coverages associated with a specific line ID stream.|
|Look up Product Lines by Product ID Stream|Retrieves information about the product lines associated with the specific product, based on the product ID.|
|Quote Policy Transaction|Generates a quote for a policy transaction.|
|Withdraw Policy Transaction|Cancels or revoke a policy transaction that has been initiated or in progress.|

<table><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="43">

Claim Management

</td><td>

Cancel Draft Claim

</td><td>

Discards the draft claim and removes all information about the draft claim from the ClaimCenter database.

</td></tr><tr><td>

Close Claim

</td><td>

Updates the status of the claim to "closed" or "settled", and updates any associated financial transactions to reflect the final settlement of the claim.**Note:** In addition to updating the claim status, the "Close claim" action may also involve other related tasks. Tasks could include closing any associated activities or tasks, and generating final reports or documentation related to the claim. The details of this action can vary depending on the Guidewire application being used, as well as the particular business processes and workflows being followed by the insurance company.

</td></tr><tr><td>

Close Exposure on Claim

</td><td>

Closes the specified exposure, based on the exposure ID.

</td></tr><tr><td>

Create Check-Sets on Claim

</td><td>

Creates a set of checks and payment transactions for a claim.

</td></tr><tr><td>

Create Claim Contact

</td><td>

Creates a ClaimContact on the claim.

</td></tr><tr><td>

Create Document on Claim

</td><td>

Creates a document on the claim.

</td></tr><tr><td>

Create Draft Auto Claim with additional objects \(composite requests\)

</td><td>

 

</td></tr><tr><td>

Create Draft Claim

</td><td>

Creates a non-open draft claim with claim ID and claim number in the ClaimCenter database.

</td></tr><tr><td>

Create Exposure on Claim

</td><td>

Creates an exposure object for tracking potential payments on the given claim.

</td></tr><tr><td>

Create Fixed Property Incident on Claim

</td><td>

Creates an incident object that captures loss information about a fixed property.

</td></tr><tr><td>

Create Injury Incident on Claim

</td><td>

Creates an incident object for capturing single-injury loss information on the specified claim.

</td></tr><tr><td>

Create Minimal Draft Claim

</td><td>

Creates an insurance claim with minimal initial data required for the claim.

</td></tr><tr><td>

Create Note on Claim

</td><td>

Creates a note on an existing claim or activity.

</td></tr><tr><td>

Create Reserves on Claim

</td><td>

Creates financial reserves for a claim in the Guidewire ClaimCenter application based on the specified parameters. Parameters could include the type of loss, the severity of the claim, the estimated costs of repair or replacement, and other relevant factors.

</td></tr><tr><td>

Create Vehicle Incident on Claim

</td><td>

Creates an incident object that captures loss information about a vehicle.

</td></tr><tr><td>

Delete Check on Claim

</td><td>

Deletes an individual check, subject to business constraints, from the claim.

</td></tr><tr><td>

Delete Claim Contact

</td><td>

Deletes a Claim Contact from the specified claim.

</td></tr><tr><td>

Delete Document on Claim

</td><td>

Deletes a document from the claim.

</td></tr><tr><td>

Delete Exposure on Claim

</td><td>

Deletes an exposure object from the specified claim.

</td></tr><tr><td>

Delete Fixed Property Incident on Claim

</td><td>

Deletes a fixed property incident object from the specified claim.

</td></tr><tr><td>

Delete Injury Incident on Claim

</td><td>

Deletes an injury incident object from the specified claim.

</td></tr><tr><td>

Delete Vehicle Incident on Claim

</td><td>

Deletes a vehicle incident object from the specified claim.

</td></tr><tr><td>

Look up Claim by Claim ID

</td><td>

Retrieves detailed information about a claim from the ClaimCenter database, based on the claim ID.

</td></tr><tr><td>

Look up Claim Center Typelist

</td><td>

Enumerates the available values for a specific Typelist in ClaimCenter. The Typelist name is provided in the description of each field that uses a Typelist enumeration.

</td></tr><tr><td>

Look up Claims Stream

</td><td>

Retrieves claim records based on criteria entered.

</td></tr><tr><td>

Look up Contacts on Claim by Claim ID Stream

</td><td>

Retrieves contact information associated with the claim from the ClaimCenter database, based on the claim ID.

</td></tr><tr><td>

Look up Persons in Contacts Stream

</td><td>

Retrieves a stream of records of information about individuals associated with a specified policy or claim. This action searches the Guidewire system when one or more search criteria, such as an individual's name, email address, phone number, or policy number is specified. This action enables more efficient processing by the requesting system.

</td></tr><tr><td>

Look up Policy Coverages on Claim by Claim ID Stream

</td><td>

Retrieves the coverage details associated with the insurance policy.

</td></tr><tr><td>

Look up Policy Locations on Claim by ID Stream

</td><td>

Retrieves the physical locations associated with the insurance policy.

</td></tr><tr><td>

Look up Policy on Claim by Claim ID

</td><td>

Retrieves the policy information associated with the claim from the ClaimCenter database, based on the claim ID.

</td></tr><tr><td>

Look up Policy Vehicles on Claim by Claim ID Stream

</td><td>

Retrieves the vehicle risk units associated with an insurance policy.

</td></tr><tr><td>

Submit Claim

</td><td>

Submits the draft claim as an open claim with an open claim number assigned, and executes automated claim setup, including business rules.

</td></tr><tr><td>

Update Check on Claim

</td><td>

Updates the status of a check on a claim.

</td></tr><tr><td>

Update Claim

</td><td>

Updates the details of the claim, which may include the claimant's information, policy details, loss details, and claim status.

</td></tr><tr><td>

Update Claim Contact

</td><td>

Updates a claim contact for the specified claim.

</td></tr><tr><td>

Update Claim Using Composite Request

</td><td>

Updates a claim by combining multiple updates into a single composite request.

</td></tr><tr><td>

Update Document on Claim

</td><td>

Enables changing the content of a document associated with a claim, and updates the specified document.

</td></tr><tr><td>

Update Exposure on Claim

</td><td>

Updates an exposure object, the estimated loss amount/potential payments, on the specified claim.

</td></tr><tr><td>

Update Fixed Property Incident on Claim

</td><td>

Updates an existing incident associated with a fixed property on the specified insurance claim in Guidewire.

</td></tr><tr><td>

Update Injury Incident on Claim

</td><td>

Updates an incident injury object for capturing single-injury loss information on the specified claim.

</td></tr><tr><td>

Update Vehicle Incident on Claim

</td><td>

Updates an existing incident associated with an injury on the specified insurance claim.

</td></tr><tr><td>

Validate Claim

</td><td>

Checks if the specified claim meets certain criteria or requirements set by the insurer before it can be processed further in Guidewire.

</td></tr><tr><td>

Validate Exposure

</td><td>

Validates the exposure, based on the exposure ID, and return a response indicating whether the exposure is valid or not.

</td></tr></tbody>
</table>## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information, and OAuth credentials. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection.

For information about setting up the spoke, see [Set up Guidewire spoke](../task/set-up-guidewire-spoke.md#).

