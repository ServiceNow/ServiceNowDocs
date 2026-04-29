---
title: Adobe Sign Spoke
description: Automate the process of sending a legal document to an individual or list of recipients for digital signature using Adobe Sign. For example, automate employee onboarding and offboarding, or sending non-disclosure agreements, legal agreements, and statements of work for digital signature. Use ServiceNow data in document templates and enable users to upload documents for signature as needed.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2025-10-14"
reading_time_minutes: 12
breadcrumb: [Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Adobe Sign Spoke

Automate the process of sending a legal document to an individual or list of recipients for digital signature using Adobe Sign. For example, automate employee onboarding and offboarding, or sending non-disclosure agreements, legal agreements, and statements of work for digital signature. Use ServiceNow data in document templates and enable users to upload documents for signature as needed.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This spoke requires an Integration Hub subscription. For more information, see [Legal schedules - IntegrationHub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Spoke version

Adobe Sign spoke v2.8.0 is the latest version.

## Spoke dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require an appropriate license if used outside the spoke implementation. For information on licenses, contact your account manager.

## Supported versions

This spoke was built for Adobe Sign API version v6, but may be compatible with later versions.

## Key features

Adobe Sign spoke enables a flow designer to:

-   Automate the process of sending a legal document to an individual or list of recipients for digital signature.
-   Copy and customize sample flows for sending transient documents or Adobe Sign library documents for digital signature.
-   Discover and synchronize the Adobe Sign documents.
-   Pause a flow until an agreement or document is signed. A scripted REST API webhook waits for the recipient to sign the document.
-   Use values from a signed document in a flow.
-   Manage the life cycle of documents in Adobe Sign from the ServiceNow instance.

## Spoke requirements

-   Adobe Sign account
-   Adobe Sign account admin credentials to perform the required account specific tasks in Adobe Sign
-   Adobe Sign group admin credentials to perform the required group specific tasks in Adobe Sign.

    **Note:** Account admin or group admin can add users to the groups. These users can access information specific to their group only.

-   Adobe Sign application configured to integrate with ServiceNow
-   Adobe Sign application details such as application ID and client secret.
-   ServiceNow admin credentials to create and synchronise the required Adobe Sign groups with ServiceNow.

    **Note:**

    -   This is the default admin role that is created when the Adobe Sign spoke is activated.
    -   ServiceNow admin has access to information about all Adobe Sign groups synchronized with ServiceNow and all tables part of the Adobe Sign spoke.
    -   User role specific to the group is created in ServiceNow, when the group is created in the ServiceNow instance. Group users have access to information specific to their Adobe Sign groups only and can view only the group-specific data from the tables that are part of the Adobe Sign spoke.
-   Integration Hub subscription

See the [Adobe Sign development](https://www.adobe.io/apis/documentcloud/sign/docs.html) documentation for instructions on creating and configuring custom applications.

## Spoke flows

The Adobe Sign spoke provides sample flows to demonstrate automating the Adobe Sign tasks. To customize a sample flow, copy it to the required application scope. Available sample flows include:

|Flow|Description|
|----|-----------|
|Adobe Sign - Send NDA Demo|Sends a statement of work for digital signature using a Adobe Sign library document when a Service Catalog request is created by the **Adobe Sign - Statement of Work Demo** item. Before using this flow, activate the **Adobe Sign - Statement of Work Demo** catalog item.|
|Adobe Sign - Statement of Work Demo|Sends a non-disclosure agreement for digital signature using a Adobe Sign library document when a Service Catalog request is created by the **Adobe Sign - Statement of Work Demo** item. Before using this flow, activate the **Adobe Sign - Statement of Work Demo** catalog item.|

The Adobe Sign spoke adds catalog items for use with the Adobe Sign spoke sample flows. Before triggering an Adobe Sign spoke sample flow, activate these catalog items.

|Catalog item|Description|
|------------|-----------|
|Adobe Sign - Statement of Work Demo|Sends a statement of work for digital signature using a Adobe Sign library document.|
|Adobe Sign - Send NDA Demo|Sends a non-disclosure agreement for digital signature using a Adobe Sign library document.|

## Spoke subflows

The Adobe Sign spoke provides a sample subflow to demonstrate automating Adobe Sign tasks. To customize the sample subflow, copy it to a new application scope. Available sample subflow is, Get Documents Per Group. The subflow retrieves documents relevant to an Adobe Sign group and stores them in the AdobeSign Documents table.

## Spoke actions

The Adobe Sign spoke provides actions to automate Adobe Sign tasks when events occur in ServiceNow. Available actions include:

<table id="table_vsb_ptb_pcc"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="11">

Document Management

</td><td>

Attach Agreement Audit Trail to ServiceNow Record

</td><td>

Downloads the agreement audit trail for the specified agreement from Adobe Sign and attaches it to a ServiceNow record.

</td></tr><tr><td>

Attach Agreement Document to ServiceNow Record

</td><td>

Downloads the agreement document for the specified agreement from Adobe Sign and attaches it to a ServiceNow record.

</td></tr><tr><td>

Attach Signed Agreement to a ServiceNow Record

</td><td>

Downloads an Adobe Sign document and attaches it to the relevant ServiceNow agreement record.

</td></tr><tr><td>

Convert Transient to Library Document

</td><td>

Converts a transient document to a library document. Ensures that the document is available in the library for more than the stipulated transient 7-day purging period.

</td></tr><tr><td>

Look up Agreement Documents

</td><td>

Retrieves the agreement documents for the specified agreement.

</td></tr><tr><td>

Look up Agreement ID

</td><td>

Retrieves the agreement ID from the ServiceNow Agreement table.

</td></tr><tr><td>

Look up Agreements Stream

</td><td>

Retrieves the list of agreements.

</td></tr><tr><td>

Look up Library Document ID

</td><td>

Retrieves the library document ID from the ServiceNow Documents table.

</td></tr><tr><td>

Look up Library Documents Stream

</td><td>

Retrieves the list of library documents.

</td></tr><tr><td>

Set Agreement Field

</td><td>

Creates a list of fields for a draft agreement.

</td></tr><tr><td>

Upload Attachment as Transient Document

</td><td>

Uploads an attachment to Adobe Sign as a transient document. The transient document is available for a period of 7 days.

</td></tr><tr><td rowspan="7">

MegaSigns Management

</td><td>

Cancel MegaSigns

</td><td>

Cancels a MegaSigns that are already out for signature.

</td></tr><tr><td>

Check MegaSigns Status

</td><td>

Checks the status of a MegaSigns record.

</td></tr><tr><td>

Create Draft MegaSigns

</td><td>

Creates a MegaSigns record in the draft state.

</td></tr><tr><td>

Download Participants and Merge Fields for Document

</td><td>

Downloads a sample CSV file for a given library document that contains information about the MegaSigns participants and form fields.

</td></tr><tr><td>

Look up MegaSigns Stream

</td><td>

Retrieves the list of all MegaSigns records.

</td></tr><tr><td>

Send MegaSigns

</td><td>

Finalises the draft and sends the MegaSigns attachment out for signature.

</td></tr><tr><td>

Wait for Signature of MegaSigns from Adobe Sign

</td><td>

Waits for the Adobe Sign webhook till all the participants sign or cancel the document.

</td></tr><tr><td rowspan="18">

Signature Management

</td><td>

Add Participant to Agreement

</td><td>

Builds a participant list iteratively over time and adds a participants to the local ServiceNow agreement record.

</td></tr><tr><td>

Add Participant to Agreement with Email OTP Authentication

</td><td>

Adds a new participant to an agreement and verify their identity using an email one-time password \(OTP\). The participants will get the OTP in an email and need to enter it before they can sign or approve the document. This extra step keeps your agreements secure by making sure only the right people can access them.

</td></tr><tr><td>

Add Participant to Agreement with Password Authentication

</td><td>

Adds a new participant to an agreement and verify their identity using a predefined password. The participant must enter the correct password before they can view, sign, or approve the document. This extra step keeps your agreements secure by making sure that only the person who knows the password can proceed with the agreement.**Note:** The Scheduler To Remove Participant Password scheduled job when activated will automatically delete the passwords that are stored for the last 30 days. For more information, see Spoke scheduled job section.

</td></tr><tr><td>

Add Participant to Agreement with Phone Authentication

</td><td>

Adds a new participant to an agreement and verify their identity using a one-time password \(OTP\) in an SMS. The participants will get the OTP in an SMS to the specified phone number and need to enter it before they can sign or approve the document. This extra step keeps your agreements secure by making sure only the right people can access them.

</td></tr><tr><td>

Add Participant Reminders to Agreement

</td><td>

Creates one or more reminders for the specified participants associated with the specified agreement.

</td></tr><tr><td>

Cancel Agreement

</td><td>

Cancels an agreement that has been sent for signature.

</td></tr><tr><td>

Check Agreement Status

</td><td>

Retrieves the status of an agreement.

</td></tr><tr><td>

Create Draft Agreement

</td><td>

Creates an agreement in the draft state in Adobe Sign and draft record in the ServiceNow Agreement table.

</td></tr><tr><td>

Finalize Draft and Send Agreement

</td><td>

Sends a draft agreement to the participant list for a signature.**Note:** You need to use the **Create Draft Agreement** and **Set Agreement Field** actions before using this action.

</td></tr><tr><td>

Generate Embedded Sending URL

</td><td>

Generates a URL that enables you to embed the agreement sender view on Adobe Sign.

</td></tr><tr><td>

Look up Agreement Events

</td><td>

Retrieves the events information for the specified agreement.

</td></tr><tr><td>

Look up Draft Agreement

</td><td>

Retrieves the draft agreement's information and Etag details, which are required while finalising the draft agreement.

</td></tr><tr><td>

Look up Form Field Value from an Agreement

</td><td>

Retrieves value of the required field from an existing agreement in Adobe Sign.

</td></tr><tr><td>

Look up Signing URL

</td><td>

Retrieves an embedded signing URL. This is useful for scenarios involving in-person signing.

</td></tr><tr><td>

Send Agreement

</td><td>

Sends one or more documents, along with its sequence, for signature to one or more participants.

</td></tr><tr><td>

Update Form Fields and Send Agreement

</td><td>

Allows participants to update or modify the form fields on an agreement before sending it for signature.

</td></tr><tr><td>

Wait for Signature from Adobe Sign

</td><td>

Waits for the participant to sign or reject the document in Adobe Sign. Then updates the signing status in ServiceNow.

</td></tr><tr><td>

Wait for Signature from Adobe Sign

</td><td>

Waits for the Adobe Sign webhook until the participant has either signed or rejected the document. Updates the status in the ServiceNow Agreement table.

</td></tr><tr><td rowspan="4">

User Management

</td><td>

Activate a User

</td><td>

Activates an existing user in Adobe Sign.

</td></tr><tr><td>

Deactivate a User

</td><td>

Deactivates an existing user in Adobe Sign.

</td></tr><tr><td>

Look up User ID by Email

</td><td>

Retrieves the user ID of an existing user in Adobe Sign.

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves the list of all users.

</td></tr><tr><td rowspan="3">

Webhook Management

</td><td>

Create Webhook

</td><td>

Creates a webhook to notify the signing events in Adobe Sign.

</td></tr><tr><td>

Look up Webhooks Stream

</td><td>

Retrieves the list of webhooks.

</td></tr><tr><td>

Remove Webhook

</td><td>

Removes a webhook from Adobe Sign.

</td></tr></tbody>
</table>## Spoke module

The Adobe Sign spoke adds a Adobe Sign module to your ServiceNow instance. The Adobe Sign spoke synchronizes and stores information about groups, documents, and agreements in ServiceNow. The Adobe Sign spoke includes the these tables.

-   Agreements \[sn\_adobesign\_spoke\_agreement\]
-   Documents \[sn\_adobesign\_spoke\_adobe\_sign\_documents\]
-   Groups \[sn\_adobesign\_spoke\_adobesign\_group\_details\]
-   Client Details \[sn\_adobesign\_spoke\_client\_details\]

<table id="table_sdt_wkh_xhb"><thead><tr><th>

Table

</th><th>

Description

</th><th>

Fields

</th></tr></thead><tbody><tr><td>

Agreements

</td><td>

Adobe Sign agreements from the synchronized Adobe Sign groups and accounts. Records in the Agreements table are updated with the signing status only when webhook is configured for the Adobe Sign account.

</td><td>

-   Name
-   Agreement ID
-   Declined Reason
-   Status
-   Participants Info
-   Form Fields Info
-   Next Signer
-   Group Name

</td></tr><tr><td>

Documents

</td><td>

Adobe Sign documents from the synchronized Adobe Sign groups and accounts. To synchronize accounts, see [Synchronize Adobe Sign with ServiceNow](../task/setup-adobe-sign.md#). The Get Documents Per Group subflow retrieves a list of documents in each Adobe Sign group. **Note:** Access to the documents is based on the group user roles.

</td><td>

-   Document ID
-   Document Owner
-   Document Last Modified
-   Group
-   Document Name
-   Document Type

</td></tr><tr><td>

Groups

</td><td>

Adobe Sign groups that are synchronized with ServiceNow. Administrator creates groups in the ServiceNow instance and provides the required details to synchronize with Adobe Sign.**Note:** User role is created when an Adobe Sign group is created in the ServiceNow instance. Users with the group-specific role can access the documents and agreements relevant to the Adobe Sign group.

</td><td>

-   Group Name
-   Group ID
-   Connection Alias

</td></tr><tr><td>

Client Details

</td><td>

Credentials of the Adobe Sign groups that are synchronized with ServiceNow.

</td><td>

-   Client ID
-   Name
-   Authentication Key

</td></tr><tr><td>

MegaSigns

</td><td>

Adobe Sign MegaSigns from the synchronized Adobe Sign groups and accounts. Records in the MegaSigns table are updated with the signing status only when webhook is configured for the Adobe Sign account.

</td><td>

-   Status
-   Signed Participants
-   Number of Pending Signatures
-   Name
-   MegaSigns ID
-   Group Name

</td></tr></tbody>
</table>## Spoke scheduled job

To delete the passwords related to Add Participant to Agreement with Password Authentication action which are stored over the last 30 days, you can use the Scheduler To Remove Participant Password scheduled job. You can also change when the scheduler runs.

To set this up, navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs** &gt; **Scheduler To Remove Participant Password** and activate the scheduled job.

## Groups and user roles

Create a group in your ServiceNow instance to synchronize the group with the corresponding group in Adobe Sign.

User role specific to the group is created in ServiceNow, when the group is created in the ServiceNow instance. For example, a HR group user role, sn\_adobesign\_spoke.HR, is created when the HR group is created in ServiceNow. ServiceNow admin can assign these group user roles to users and control access to the group-specific information such as:

-   Documents and agreements
-   Connection and credential aliases
-   Credential records
-   Application registries
-   Data in tables of the Adobe Sign spoke

To run flows and subflows, group users must also have these roles:

-   connection\_admin
-   credential\_admin
-   flow\_designer
-   oauth\_admin
-   script\_debugger
-   view\_changer

Only ServiceNow admin has access to information about all Adobe Sign groups that are synchronised with the ServiceNow instance.

## Adobe Acrobat Sign account requirements

The Adobe Sign spoke requires creating a custom app on your Adobe Sign account to generate OAuth 2.0 tokens.

## Connection and credential alias requirements

Integration Hub uses aliases to manage connection and credential information. Using an alias eliminates the need to configure multiple credentials and connection information profiles when using multiple environments. If the connection or credential information changes, you don't need to update any actions that use the connection. For more information, see [Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Note:** A connection and credential alias is specific to a group in Adobe Sign.

A sample connection and credential alias is provided for demonstration purpose. ServiceNow admin must create an alias for each Adobe Sign group to synchronize that group with the ServiceNow instance. For example, you can have different connection and credential alias records one for each BU in your organization such as HR, Legal, Finance and so on. For information about setting up the spoke, see [Synchronize Adobe Sign group with ServiceNow](../task/setup-adobe-sign.md#).

