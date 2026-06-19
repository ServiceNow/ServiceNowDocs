---
title: Configure the OAuth authentication method development instance
description: Set up OAuth authentication for instance-to-instance Scan Engine integrations using several stages, an integration user account, an OAuth2 configuration record, and provider and client application registries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/configure-oauth-auth-method.html
release: australia
product: Impact
classification: impact
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 3
breadcrumb: [Register your instance, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Configure the OAuth authentication method development instance

Set up OAuth authentication for instance-to-instance Scan Engine integrations using several stages, an integration user account, an OAuth2 configuration record, and provider and client application registries.

## About this task

OAuth requires a minimum of one provider record and two client records per connection direction. The provider is created on the instance that receives connections \(typically Production\); the client is created on the initiating instance \(typically Development\) and must also be present on the provider instance.

**Note:**

ServiceNow platform UI labels the outbound client record as consumer. This documentation uses the term client to align with standard OAuth terminology. The **OAuth API endpoint for clients** registry type is deprecated, use **Connect to a third-party OAuth Provider** instead.

## Before you begin

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\).

## Procedure

1.  Stage 1 — Confirm the integration user account
2.  Confirm that the integration user account exists in both development and production instances, has the required roles assigned, and that the account password is recorded in a secure location for use in later stages.

    If the account has not been created yet, complete [Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/task-create-integration-user.md) before continuing.

3.  Stage 2 — Create an OAuth2 configuration record in the Development instance
4.  Navigate to `sys_auth_profile_oauth2.list` and select **New**.

    If the username and password fields are not visible, customize the form to display them.

5.  Populate the **Name**, **Application** scope \(Scan Engine\), **Username** \(matching the integration user ID\), and **Password** fields.

6.  **Submit** the record.

    If this record is imported to another instance, re-enter the password on that instance before use.

7.  Stage 3 — Configure the provider on the Development instance
8.  Set the Application scope to **Scan Engine**.

9.  Navigate to **ALL** &gt; **System OAuth** &gt; **Inbound Integrations** &gt; **New integration**.

10. Select **O-Auth- Resource Owner Password Credentials Grant**.

11. Fill out the form only indicated as follows:

    |Field|Description|
    |-----|-----------|
    |Name|OAuth-Client-Dev|
    |Provider Name|Leave empty.|
    |Client ID|Copy the client id to a text file for later use.|
    |Client secret|Enter the password used for the integration account for alignment purposes.|
    |Comments|Leave empty.|
    |Active|True|
    |Auth scope|**useraccount**|
    |Advanced options \(optional\): Token Format|**Opaque**|

12. Select **Save**.

    The new OAuth Client-Dev account will be listed in the inbound integrations list.

13. Stage 4 - Create the OAuth Provider application registry
14. Navigate to **ALL** &gt; **System OAuth** &gt; **Application Registry** &gt; **New**.

15. Select **Connect to an OAuth Provider \(simplified\)- Outbound**.

    |Field|Value|
    |-----|-----|
    |Name|OAuth Provider - Dev|
    |Client ID|Enter or paste the client id from the O-Auth- Resource Owner Password Credentials Grant step.|
    |Client Secret|Enter the same password from the client integration account.|
    |Default Grant Type|Resource Owner Password Credentials|
    |Authorization URL|N/A|
    |Redirect URL|Select the redirect URL Ex: https://dev.servicenow.com/oauth\_redirect.do|
    |Token URL|Use the redirect URL with a suffix of "token", Ex: https://dev.servicenow.com/oauth\_token.do|

16. **Save** the record.

    \[Omitted image "scan-engine-oauth-client-record.png"\] Alt text: OAuth Provider-Dev client record.

17. For the OAuthAPI Script, select **OAuthUtil**.

18. **Save** the record.

19. Stage 5 - Set up the SN Instances
20. Navigate to **All** &gt; **Scan Engine** &gt; **My SN Instances**.

    If the My SN Instances record for this instance has not been created yet, complete [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md) before continuing.

21. Open the existing instance record and configure the OAuth-specific fields as follows.

    |Field|Value|
    |-----|-----|
    |Authentication Type|OAuth|
    |OAuth Application Registry|OAuth Provider-Dev|
    |OAuth User Profile|New: Use the same integration account name, username, and password.|

22. Select **Submit**.

23. Stage 6 - Validate connection
24. Save the record, then select **Validate Connection**.

    Connection Status updates to `Connection valid`.

    **Note:** If the Connection status returns an Error: User not setup on target instance, refer to the Key Management Framework setup step in [Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/validate-instance-connection.md).


-   **[Configure the OAuth authentication method production instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-oauth-auth-method-prod.md)**  
Export OAuth records from the development instance, import them into the production instance, correct Key Management Framework \(KMF\) credential encryption, and configure development-to-production authentication so that both instances can validate their connections to each other.

**Parent Topic:**[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md)

