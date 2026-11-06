---
title: Set up Password Reset integration with Google Directory
description: Enables end users to reset their Google passwords using Password Reset and Google Directory spoke.Customize the default credential store records and password reset processes to integrate Password Reset with Google Directory.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
---

# Set up Password Reset integration with Google Directory

Enables end users to reset their Google passwords using Password Reset and Google Directory spoke.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Integration Hub subscription

This application requires an Integration Hub or Workflow Data Fabric subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Application version

Password Reset integration with Google Directory 1.0.3 is the latest version.

## Dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   Google Directory spoke v 1.3.1 or higher
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the application implementation.

## Subflows

The Password Reset integration with Google Directory application provides these subflows that automate the Password Reset tasks:

|Subflow|Description|
|-------|-----------|
|Password Connection Test|Tests connection to Google Directory.|
|Password Lock State|Checks the lock status of the specified user account in Google Directory.|
|Password Reset|Resets the password of the specified Google Directory user.|
|Password Unlock|Unlocks the required user account in Google Directory.|

## Actions

The Password Reset integration with Google Directory provides the Get Configuration Variables for Google Directory Reset Process action to retrieve the user name of the required Google Directory user and the details of all variables.

## Set up the Password Reset integration with Google Directory

Customize the default credential store records and password reset processes to integrate Password Reset with Google Directory.

### Before you begin

-   Request Integration Hub subscription.
-   Activate Password Reset
-   Activate and set up the Google Directory spoke.
-   Activate Password Reset integration with Google Directory.
-   Role required: password\_reset\_admin

### Procedure

1.  Navigate to **Password Reset** &gt; **Credential Stores**.

2.  Open the record for Password Reset integration with Google Directory.

    For example, **Sample Google Directory Credential Store** .

3.  Customize the default record as per your requirement.

    For more information, see [Configure the connection to a credential store for the Password Reset processes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/password-reset/t_CreateACredentialStore.md).

4.  Navigate to **Password Reset** &gt; **Processes**.

5.  Customize the default records, **Sample Service-Desk Process for Google Directory** and **Sample Employee Self-Service Process for Google Directory**, as per your requirement.

    For more information, see [Configure your Password Reset process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/password-reset/t_CreateAPasswordResetProcess.md).

    **Note:** Google Directory doesn't support password change. Hence, the **Password change** check box on the process records isn’t supported in this integration.


