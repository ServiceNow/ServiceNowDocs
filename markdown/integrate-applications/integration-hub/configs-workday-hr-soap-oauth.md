---
title: Configurations to use Workday HR SOAP OAuth
description: Configure your ServiceNow instance to perform Workday HR SOAP based actions with OAuth 2.0.Register Workday HR spoke as the API client in your Workday account and generate client ID, client secret.Configure the system properties to enable OAuth 2.0 for SOAP APIs based actions for Workday HR spoke.Provide the base URL of your Workday HR instance in the Connection Details \[connection\_details\] table. Spoke actions based on the SOAP API, use these details for the action execution.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configurations to use Workday HR SOAP OAuth

Configure your ServiceNow instance to perform Workday HR SOAP based actions with OAuth 2.0.

**Note:** If you are migrating from basic auth to OAuth 2.0 for SOAP based actions, ensure to remove the basic authentication configurations before the migration.

## Generate client ID and client secret for Workday HR spoke

Register Workday HR spoke as the API client in your Workday account and generate client ID, client secret.

### Before you begin

Role required: admin

### Procedure

1.  Log into your Workday tenant.

2.  Navigate to Search and enter `Register API Client for Integrations` task. ![Search for Register API Client for Integrations task in Workday](../image/wkdy-hr-reg-api-client-integ.png)

3.  On the Register API Client for Integrations form, fill in the details.

    |Field|Description|
    |-----|-----------|
    |Client Name|Client name of the app. For example, enter `Workday HR spoke`.|
    |Non-expiring Refresh Tokens|Option to enable refresh tokens that do not expire.|
    |Scope \(Functional Areas\)|Select the required functional areas.|
    |Include Workday Owned Scope|Option to select Workday owned scope.|

    ![Fields in Register API Client for integrations screen](../image/wkday-reg-api-client-screen.png)

4.  Click **OK**.

    Client ID and Client Secret are generated after the registration is successful.![Client ID and client secret generated after API client registration](../image/wkday-fin-client-id-sec-generated.png)

5.  Click the ellipsis button after the specified client name.![Navigating Manage Refresh Tokens for Integrations option](../image/wkday-mng-refresh-token-nav.png)

6.  Select **API Client** &gt;**Manage Refresh Tokens for Integrations**.

7.  Select your Workday Account and click **OK**.

    Delete or Regenerate Refresh Token screen displays.

8.  Select **Generate New Refresh Token** option and click **OK**.![Refresh token generated in Workday account](../image/wkday-fin-refresh-tkn.png)


### Result

A new refresh token is generated. Copy and store the refresh token for configuring system property.

## Configure system properties for Workday HR spoke

Configure the system properties to enable OAuth 2.0 for SOAP APIs based actions for Workday HR spoke.

### Before you begin

-   [Generate client ID and client secret for Workday HR spoke](configs-workday-hr-soap-oauth.md#)
-   Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the **Application** column, search for `Workday HR Spoke`.

3.  Open the **sn\_workday\_hr\_spke.glide.hub.clientid** system property.

4.  Enter the Client ID generated from the Workday account in the **Value** field and click **Update**.

5.  Open the **sn\_workday\_hr\_spke.glide.hub.clientsecret** system property.

6.  Enter the Client secret generated from the Workday account in the **Value** field and click **Update**.

7.  Open the **sn\_workday\_hr.glide.hub.refreshtoken** system property.

8.  Enter the refresh token generated from the Workday account in the **Value** field and click **Update**.

9.  Open the **sn\_workday\_hr\_spke.glide.hub.tokenurl** system property.

10. Enter the token URL generated from the Workday account in the **Value** field and click **Update**.


### Result

The required system properties are configured for the Workday HR spoke.

## Provide the Workday HR base URL

Provide the base URL of your Workday HR instance in the Connection Details \[connection\_details\] table. Spoke actions based on the SOAP API, use these details for the action execution.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Workday HR Spoke** &gt; **Connection Details**.

2.  Click the **Show List** related list.

3.  Click **New**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Base URL|Base URL of the Workday instance or tenant name. Enter the base URL in this format `https://<workday_host_url>/ccx/service/<workday_tenant_name>`|
    |Version|Version of the API. For example, enter `v33.2`.|
    |Webservice Type|Type of web service. Select `SOAP`.|

5.  Click **Save**.


