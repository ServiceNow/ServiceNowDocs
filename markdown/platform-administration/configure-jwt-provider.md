---
title: Configure a JWT provider
description: Configure a JWT provider on the ServiceNow AI Platform to configure an OAuth application profile to authenticate using certificates.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OAuth profile to use certificates, Read email using Microsoft Graph, Read or send emails using Microsoft Graph, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a JWT provider

Configure a JWT provider on the ServiceNow AI Platform to configure an OAuth application profile to authenticate using certificates.

## Before you begin

Upload a Java Key Store certificate. Attach a JKS certificate containing the certificate uploaded on Microsoft Azure to your instance to use when enabling the JWT client authentication. For more information, see Upload Java Key Store certificate.

Create a JWT signing key to assign to your Java KeyStore \(JKS\) certificate. For more information, see Configure a JWT signing key.

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
</table>    For more information, see Create a JWT provider with a JWT signing key.

2.  From the JWT Provider record menu, select **Copy sys\_id** and copy the JWT provider sys\_id.


## What to do next

[Generate a SHA-1 thumbprint](generate-thumbprint.md)

**Parent Topic:**[Configure an OAuth profile to use certificates for authentication with Microsoft Azure](configure-oauth-profile-using-certificates.md)

