---
title: Create an OAuth API script
description: Create and duplicate an OAuth API script for application registry.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure client credential flow for SMTP OAuth2 using certificate-based authentication, Send email using client credential flow, Advanced email setup, Configure email administration, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an OAuth API script

Create and duplicate an OAuth API script for application registry.

## Before you begin

Generate an SHA-1 thumbprint. For more information, see [Generate a SHA-1 thumbprint](generate-thumbprint.md).

Generate a sys\_id when you configure a JWT provider. For more information, see [Configure a JWT provider](config-jwt-credential-flow.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Select and open **EmailCertificateOAuthTemplate**.

3.  Duplicate the script by changing the name in the **Name** field, select **Insert and Stay** from the record menu.

    **Note:** The name must begin with **OAuth** to create an OAuth script.

    The script is copied and created with a different name.

4.  In the copied script, enter the JWT provider sys\_id and SHA-1 thumbprint.

5.  Select **Update**.


## What to do next

[Register an OAuth Provider](register-oauth-cred-flow.md).

**Parent Topic:**[Configure client credential flow for SMTP OAuth2 using certificate-based authentication](config-credential-flow-certificate.md)

