---
title: Create an OAuth API script
description: Create and duplicate an OAuth API script for application registry.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OAuth profile to use certificates, Read email using Microsoft Graph, Read or send emails using Microsoft Graph, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create an OAuth API script

Create and duplicate an OAuth API script for application registry.

## Before you begin

Generate a SHA -1 thumbprint. For more information see [Generate a SHA-1 thumbprint](generate-thumbprint.md).

Ensure you have the Email - Support for Email Processing by Microsoft Graph API plugin \(com.glide.email.graph\) installed.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Select and open **GraphCertificateOAuthTemplate**.

3.  Duplicate the script by changing the name in the **Name** field,select **Insert and Stay** from the record menu.

    **Note:** The name should begin with **OAuth**.

    The script is copied and created with a different name.

4.  In the script, enter the JWT provider sys\_id and SHA -1 thumbprint.

5.  Select **Update**.


## What to do next

[Register an application as an OAuth provider](microsoft-graph.md#).

**Parent Topic:**[Configure an OAuth profile to use certificates for authentication with Microsoft Azure](configure-oauth-profile-using-certificates.md)

