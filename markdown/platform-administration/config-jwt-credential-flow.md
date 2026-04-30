---
title: Configure a JWT provider
description: Configure a JWT provider on the ServiceNow AI Platform to configure an OAuth application profile to authenticate using certificates.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure client credential flow for SMTP OAuth2 using certificate-based authentication, Send email using client credential flow, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure a JWT provider

Configure a JWT provider on the ServiceNow AI Platform to configure an OAuth application profile to authenticate using certificates.

## Before you begin

Upload a Java Key Store \(JKS\) certificate. Attach a JKS certificate containing the certificate uploaded on Microsoft Azure to your instance to use when enabling the JWT client authentication. For more information, see [Upload Java Key Store certificate](https://www.servicenow.com/docs/access?context=JWT-Bearer-token-support&version=xanadu&pubname=xanadu-platform-security&section=upload-jks-certificate&ft:locale=en-US).

Create a JWT signing key to assign to your JKS certificate. For more information, see [Configure a JWT signing key](https://www.servicenow.com/docs/access?context=JWT-Bearer-token-support&version=xanadu&pubname=xanadu-platform-security&section=configure-JWT-signing-key&ft:locale=en-US).

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

https://login.microsoftonline.com/\{tenantId\}/oauth2/v2.0/token**Note:** The tenant ID should be replaced with the directory ID copied from Microsoft Azure.

</td></tr><tr><td>

iss

</td><td>

Client ID copied from Microsoft Azure

</td></tr><tr><td>

sub

</td><td>

Client ID copied from Microsoft Azure

</td></tr></tbody>
</table>    For more information, see [Create a JWT provider with a JWT signing key](https://www.servicenow.com/docs/access?context=JWT-Bearer-token-support&version=xanadu&pubname=xanadu-platform-security&section=associate-jwt-provider-key&ft:locale=en-US).

2.  From the JWT Provider record menu, select **Copy sys\_id** and copy the JWT provider sys\_id.


## What to do next

[Generate SHA-1 thumbprint](generate-sha-1-thumbprint.md)

**Parent Topic:**[Configure client credential flow for SMTP OAuth2 using certificate-based authentication](config-credential-flow-certificate.md)

