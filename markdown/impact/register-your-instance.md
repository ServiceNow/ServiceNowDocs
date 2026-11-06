---
title: Register your instance
description: Register each participating ServiceNow instance in the My SN Instances table before configuring any instance-to-instance integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/register-your-instance.html
release: australia
topic_type: task
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Register your instance

Register each participating ServiceNow instance in the My SN Instances table before configuring any instance-to-instance integration.

## Before you begin

Before registering, gather the following for each instance:

-   The exact instance name matching the `instance_name` system property \(typically the subdomain — for example, `companyname` from `companyname.service-now.com`\).
-   The full instance URL in the format `https://instancename.service-now.com`. Omit `www.`, trailing slashes, and any path after the domain.
-   The environment type: Development, Production, or Test. Only one instance in your stack may be designated Production.

Role required: Scan Engine Admin \(sn\_se.scan\_engine\_admin\)

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** and open the **My SN Instances** related list tab.

2.  Select **New** for each instance and populate the following fields.

<table id="table_hhb_fjv_djc"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Instance Name

</td><td>

Must match the `instance_name` system property. To find the value, open `stats.do` in the instance and check the instance name.

</td></tr><tr><td>

Instance URL

</td><td>

`https://instancename.service-now.com` Select the lock icon next to the field to enter the URL.

</td></tr><tr><td>

Environment

</td><td>

Development, Production, or Test. This value determines which Scan Engine options appear on the instance. Only Development instances show the manual definition sync actions, and only one instance in the stack can be Production.

</td></tr><tr><td>

Authentication Type

</td><td>

-   Basic: See [Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-basic-auth-method.md)
-   OAuth:
    -   [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method.md)
    -   [Configure the OAuth authentication method production instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method-prod.md)


</td></tr><tr><td>

API Credential Config

</td><td>

Appears when Authentication Type is Basic. Select the Basic authentication record for this instance.

</td></tr><tr><td>

OAuth Application Registry

</td><td>

Appears when Authentication Type is OAuth. Select the OAuth provider registry record.

</td></tr><tr><td>

OAuth User Profile

</td><td>

Appears when Authentication Type is OAuth. Select the OAuth user profile for the integration account.

</td></tr></tbody>
</table>3.  Promote or export the My SN Instances list to all instances that will use Scan Engine integrations.

4.  On each target instance, open the imported production record and select **Validate Connection**.

    Connection Status updates to `Connection Valid` on success.


## What to do next

If validation fails, resolve the root cause before retrying. Repeated failed attempts can trigger the account lockout policy. Refer to [Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/validate-instance-connection.md) for additional information.

-   **[Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method.md)**  
Set up OAuth authentication for instance-to-instance Scan Engine integrations using several stages, an integration user account, an OAuth2 configuration record, and provider and client application registries.
-   **[Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-basic-auth-method.md)**  
Confirm an integration user, create a Basic authentication record, then connect your instances using basic authentication. Basic authentication is supported but OAuth is recommended for production environments.
-   **[Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/validate-instance-connection.md)**  
Validate the connection between registered instances to confirm that authentication and My SN Instances configuration are correct before enabling integrations.
-   **[Recover from account lockout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/recover-from-account-lockout.md)**  
Unlock the integration user account and clear the password reset flag after repeated failed validation attempts trigger the account lockout policy.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md)

