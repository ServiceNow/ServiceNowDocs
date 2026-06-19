---
title: Create an OAuth API script
description: Create and duplicate an OAuth API script for application registry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/oauth-api-script.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [OAuth profile to use certificates, Reading email using Microsoft Graph, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Create an OAuth API script

Create and duplicate an OAuth API script for application registry.

## Before you begin

Generate a SHA -1 thumbprint. For more information see [Generate a SHA-1 thumbprint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/generate-thumbprint.md).

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

[Register an application as an OAuth provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/microsoft-graph.md).

**Parent Topic:**[Configure an OAuth profile to use certificates for authentication with Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/configure-oauth-profile-using-certificates.md)

