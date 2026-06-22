---
title: Configure a JWT provider
description: Configure a JWT provider on the ServiceNow AI Platform to configure an OAuth application profile to authenticate using certificates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/configure-jwt-provider.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [OAuth profile to use certificates, Reading email using Microsoft Graph, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Configure a JWT provider

Configure a JWT provider on the ServiceNow AI Platform to configure an OAuth application profile to authenticate using certificates.

## Before you begin

Upload a Java Key Store certificate. Attach a JKS certificate containing the certificate uploaded on Microsoft Azure to your instance to use when enabling the JWT client authentication. For more information, see [Upload Java Key Store certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/JWT-Bearer-token-support.md).

Create a JWT signing key to assign to your Java KeyStore \(JKS\) certificate. For more information, see [Configure a JWT signing key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/JWT-Bearer-token-support.md).

Role required: admin

## Procedure

1.  Add a JWT provider to your ServiceNow instance and fill in the claim values.

<table id="table_swt_kjj_wtb"><thead><tr><th>

Claim Name

</th><th>

Claim Value

</th></tr></thead><tbody><tr><td>

aud

</td><td>

https://login.microsoftonline.com/\{tenantId\}/oauth2/v2.0/token**Note:** Tenant ID is the directory ID copied from Microsoft Azure.

</td></tr><tr><td>

iss

</td><td>

Client ID copied from Microsoft Azure

</td></tr><tr><td>

sub

</td><td>

Client ID copied from Microsoft Azure

</td></tr></tbody>
</table>    For more information, see [Create a JWT provider with a JWT signing key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/JWT-Bearer-token-support.md).

2.  From the JWT Provider record menu, select **Copy sys\_id** and copy the JWT provider sys\_id.


## What to do next

[Generate a SHA-1 thumbprint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/generate-thumbprint.md)

**Parent Topic:**[Configure an OAuth profile to use certificates for authentication with Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/configure-oauth-profile-using-certificates.md)

