---
title: Salesforce Spoke
description: The Salesforce spoke is built by Bristlecone, Inc. Access and manage data in the Account, Contact, Case, Lead, Opportunity, Order, and User objects of your Salesforce instance from the ServiceNow instance.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Salesforce Spoke

The Salesforce spoke is built by Bristlecone, Inc. Access and manage data in the Account, Contact, Case, Lead, Opportunity, Order, and User objects of your Salesforce instance from the ServiceNow instance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Salesforce spoke v2.4.3 is the latest version.

## Supported version

This spoke was built for the Salesforce API version v64.0, but may be compatible with later versions.

## Spoke requirements

-   Salesforce account
-   Salesforce admin credentials
-   Salesforce connected app configured to integrate with ServiceNow
-   Salesforce connected app details such as, consumer key and consumer secret.
-   Integration Hub subscription

**Note:** For users who have installed Salesforce spoke v1, you can't upgrade from Salesforce spoke v1 to Salesforce spoke v1.2 directly. To upgrade, you must uninstall the Salesforce spoke v1 and then, install the Salesforce spoke v1.2.

You must also note that, Salesforce spoke v1 is certified on New York and Salesforce spoke v1.2 is certified on Orlando and Paris.

## Spoke subflows

The Salesforce spoke provides subflows to access and manage data in the Salesforce Account, Case, Contract, and Opportunity objects.

|Subflow|Description|
|-------|-----------|
|Account Subflow|Processes data in the account object when the Salesforce webhook is triggered.|
|Case Subflow|Processes data in the case object when the Salesforce webhook is triggered.|
|Contract Subflow|Processes data in the contract object when the Salesforce webhook is triggered.|
|Opportunity Subflow|Processes data in the opportunity object when the Salesforce webhook is triggered.|
|Salesforce Subflow|Processes data in any Salesforce object when the Salesforce webhook is triggered.|

## Spoke actions

The Salesforce spoke provides actions to access and manage data in the Salesforce , Account, Contact, Case, Lead, Opportunity, Order, and User objects.

<table id="table_xtv_cwt_g3b"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Account Management

</td><td>

Create Account

</td><td>

Creates an account in Salesforce.

</td></tr><tr><td>

Look up Accounts

</td><td>

Retrieves all the account details based on the specified SOQL query.

</td></tr><tr><td>

Look up Records for Account

</td><td>

Retrieves all the records for an account based on the given relationship name.

</td></tr><tr><td rowspan="9">

Record Management

</td><td>

Create Record

</td><td>

Creates a record in Salesforce.**Note:** Ensure that you use relevant actions to create records for Account, Contact, Case, Lead, Opportunity, Order, and User.

</td></tr><tr><td>

Delete Record

</td><td>

Deletes a record in Salesforce.

</td></tr><tr><td>

Get Record Details

</td><td>

Retrieves the specific record in Salesforce by Record ID.

</td></tr><tr><td>

Look up Attachment from Records

</td><td>

Retrieves an attachment from a record if it was uploaded using the Salesforce Classic view.

</td></tr><tr><td>

Look up Contracts

</td><td>

Retrieves all the contract details based on the specified SOQL query.

</td></tr><tr><td>

Look up Related Records

</td><td>

Retrieves all the records for the specified object name associated with their given relationship name.

</td></tr><tr><td>

Subflow Helper Action

</td><td>

Parses the subflow's JSON input and generates an array of object.

</td></tr><tr><td>

Update Record

</td><td>

Updates a record in Salesforce.

</td></tr><tr><td>

Look up Document from Record

</td><td>

Retrieves a document from a record if it was uploaded using the Salesforce Lightning view.

</td></tr><tr><td>

Case Management

</td><td>

Create Case

</td><td>

Creates a case in Salesforce.

</td></tr><tr><td>

Lead Management

</td><td>

Create Lead

</td><td>

Creates a lead in Salesforce.

</td></tr><tr><td rowspan="27">

Metadata Retrieval

</td><td>

Metadata - Check Service Cloud Feature

</td><td>

Checks whether Salesforce Service Cloud is enabled on the target Salesforce instance. To use this action, perform the steps outlined in the Create a Salesforce CRM integration profile section in [Integrating with Salesforce CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-salesforce-crm.md).

</td></tr><tr><td>

Metadata - Get Account Types

</td><td>

Retrieves all the available account types in Salesforce.

</td></tr><tr><td>

Metadata - Get Creatable Fields

</td><td>

Retrieves a list of creatable fields in a required standard or custom Salesforce table.

</td></tr><tr><td>

Metadata - Get Creatable Objects

</td><td>

Retrieves a list of creatable objects in Salesforce.

</td></tr><tr><td>

Metadata - Get Deletable Objects

</td><td>

Retrieves a list of deletable objects in Salesforce.

</td></tr><tr><td>

Metadata - Get Updatable Fields

</td><td>

Retrieves a list of updatable fields in a required standard or custom Salesforce table.

</td></tr><tr><td>

Metadata - Get Updatable Objects

</td><td>

Retrieves a list of updatable objects in Salesforce.

</td></tr><tr><td>

Metadata - Get Account Fields

</td><td>

Retrieves a list of fields in the Salesforce Account object.

</td></tr><tr><td>

Metadata - Get Case Origin Values

</td><td>

Retrieves a list of case origins in Salesforce. The value field of the case origin from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get Case Priorities

</td><td>

Retrieves a list of case priorities in Salesforce. The value field of the case priority from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get Case Reasons

</td><td>

Retrieves a list of case reasons in Salesforce. The value field of the case reason from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get Case Status Values

</td><td>

Retrieves a list of case status values in Salesforce. The value field of the case status from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get Industries for Accounts

</td><td>

Retrieves all the industries available for accounts in Salesforce.

</td></tr><tr><td>

Metadata - Get Industries for Lead

</td><td>

Retrieves a list of industries in the Salesforce Lead object. The value field of the industry from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get Lead Status

</td><td>

Retrieves a list of lead status values in Salesforce. The value field of the lead status from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get Objects

</td><td>

Retrieves all the available object names in Salesforce.

</td></tr><tr><td>

Metadata - Get Opportunity Stages

</td><td>

Retrieves a list of opportunity stages in Salesforce. The value field of the opportunity stage from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get Opportunity Types

</td><td>

Retrieves a list of opportunity types in Salesforce. The value field of the opportunity type from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get Order Status Values

</td><td>

Retrieves a list of order status values in Salesforce. The value field of the order status from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get Organization Type

</td><td>

Retrieves the organization type of the Salesforce instance. To use this action, perform the steps outlined in the Create a Salesforce integration profile section in [Integrating with Salesforce](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-salesforce-crm.md).

</td></tr><tr><td>

Metadata - Get Record Fields

</td><td>

Retrieves all the record fields for the specified table name.

</td></tr><tr><td>

Metadata - Get Relationship Fields

</td><td>

Retrieves all the relationship fields for the specified object name.

</td></tr><tr><td>

Metadata - Get Relationship Names

</td><td>

Retrieves all the relationship names for the specified object name.

</td></tr><tr><td>

Metadata - Get User Email Encodings

</td><td>

Retrieves a list of email encodings in the Salesforce User object. The value field of the email encoding from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get User Languages

</td><td>

Retrieves a list of languages in the Salesforce User object. The value field of the user language from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get User Locales

</td><td>

Retrieves a list of locales in the Salesforce User object. The value field of the user locale from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Metadata - Get User Time Zones

</td><td>

Retrieves list of time zones in the Salesforce User object. The value field of the time zone from the Salesforce response body is mapped to the name field in JSON output.

</td></tr><tr><td>

Opportunity Management

</td><td>

Create Opportunity

</td><td>

Creates an opportunity in Salesforce.

</td></tr><tr><td>

Order Management

</td><td>

Create Order

</td><td>

Creates an order in Salesforce.

</td></tr><tr><td rowspan="2">

License Management

</td><td>

Look up User Licenses Stream

</td><td>

Retrieves user subscription information that is available in Salesforce. To use this action, perform the steps outlined in the Create a Salesforce CRM integration profile section in [Integrating with Salesforce CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-salesforce-crm.md).

</td></tr><tr><td>

Look up Usage Based Entitlements Stream

</td><td>

Retrieves the consumption usage details for the resources.To use this action, perform the steps outlined in the Create a Salesforce CRM integration profile section in [Integrating with Salesforce CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-salesforce-crm.md).

</td></tr><tr><td rowspan="5">

User Management

</td><td>

Create User

</td><td>

Creates a user in Salesforce.

</td></tr><tr><td>

Look up User Profiles

</td><td>

Retrieves a list of user profiles in Salesforce. The name and ID fields of the user profiles from the Salesforce response body are mapped to the label and name fields respectively in the JSON output.

</td></tr><tr><td>

Look up User Roles

</td><td>

Retrieves a list of user roles in Salesforce. The name and ID fields of the user profiles from the Salesforce response body are mapped to the label and name fields respectively in the JSON output.

</td></tr><tr><td>

Look up Users

</td><td>

Retrieves user attributes for Salesforce users. To use this action, perform the steps outlined in the Create a Salesforce CRM integration profile section in [Integrating with Salesforce CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-salesforce-crm.md).

</td></tr><tr><td>

Remove User

</td><td>

Reclaims a user account in Salesforce. To use this action, perform the steps outlined in the Create a Salesforce CRM integration profile section in [Integrating with Salesforce CRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/integrate-with-salesforce-crm.md).

</td></tr></tbody>
</table>## Salesforce account requirements

The Salesforce spoke requires configuring your Salesforce account to generate an OAuth 2.0 JWT Bearer Grant token.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r-credentials.md).

For information about setting up the spoke, see [Set up the Salesforce spoke](../task/setup-sf-spk.md#).

## MID Server requirements

These actions use REST calls, which can run on an instance or MID Server. Use the connection record associated with the Salesforce alias to configure where actions run as well as set MID Server selection attributes. For more information, see [MID server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-landing.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](../task/config-adv-mid-settings-for-oauth-on-mid.md).

