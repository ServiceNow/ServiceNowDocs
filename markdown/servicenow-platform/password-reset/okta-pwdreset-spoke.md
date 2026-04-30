---
title: Set up Password Reset integration with Okta
description: Enables end users to reset or change their Okta passwords using Password Reset and Okta spoke.Customize the default credential store records and password reset processes to integrate Password Reset with Okta.
locale: en-US
release: zurich
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Set up, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up Password Reset integration with Okta

Enables end users to reset or change their Okta passwords using Password Reset and Okta spoke.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Integration Hub subscription

This application requires an Integration Hub or Workflow Data Fabric subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

## Application version

Password Reset integration with Okta 1.1.2 is the latest version.

## Dependencies

If you’re having trouble installing the app, ensure that these dependent plugins are installed:

-   [Okta spoke v 4.1.3](https://www.servicenow.com/docs/access?context=okta-v2-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)
-   ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\)
-   ServiceNow IntegrationHub Action Step - REST \(com.glide.hub.action\_step.rest\)
-   ServiceNow IntegrationHub Runtime \(com.glide.hub.integration.runtime\)

**Note:** Some of these plugins are licensable features and require appropriate licenses, if used outside the application implementation.

## Subflows

The Password Reset integration with Okta application provides these subflows that automate the Password Reset tasks:

|Subflow|Description|
|-------|-----------|
|Password Change|Changes password of the required Okta user.|
|Password Connection Test|Tests connection to Okta.|
|Password Lock State|Checks the lock status of the specified user account in Okta.|
|Password Reset|Resets the password of the specified Okta user.|
|Password Unlock|Unlocks the required user account in Okta.|
|Send Email After Change Password|Sends a password change notification email to the user. This subflow is used in the Password Change subflow.|

## Actions

The Password Reset integration with Okta provides the Get Configuration Variables for Okta Reset Process action to retrieve the user name of the required Okta user and the details of all variables.

## Set up the Password Reset integration with Okta

Customize the default credential store records and password reset processes to integrate Password Reset with Okta.

### Before you begin

-   Request Integration Hub subscription.
-   Activate Password Reset
-   Activate and set up the Okta spoke.
-   Activate Password Reset integration with Okta.
-   Role required: password\_reset\_admin

### Procedure

1.  Navigate to **Password Reset** &gt; **Credential Stores**.

2.  Open the record for Password Reset integration with Okta.

    For example, **Sample Okta Credential Store**

3.  Customize the default record as per your requirement.

    For more information, see [Configure the connection to a credential store for the Password Reset processes](../task/t_CreateACredentialStore.md).

4.  Navigate to **Password Reset** &gt; **Processes**.

5.  Customize the default records, **Service-Desk Process for Okta** and **Employee Self-Service Process for Okta** , as per your requirement..

    **Note:** The **User must reset password** check box isn't supported in this integration. That is, you can't enforce users to reset their password upon first login after they reset password using the auto-generated password.

    For more information, see [Configure your Password Reset process](../task/t_CreateAPasswordResetProcess.md).


