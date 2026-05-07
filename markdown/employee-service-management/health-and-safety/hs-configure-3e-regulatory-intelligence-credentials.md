---
title: Configure OAuth authentication for the 3E Regulatory Intelligence API
description: Configure the 3E Regulatory credentials alias with the Client ID and Client Secret required to authenticate with the 3E Regulatory Intelligence API.
locale: en-US
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [3E Regulatory Intelligence, 3E, Integration with third-party services, Health and Safety, Employee Service Management]
---

# Configure OAuth authentication for the 3E Regulatory Intelligence API

Configure the 3E Regulatory credentials alias with the **Client ID** and **Client Secret** required to authenticate with the 3E Regulatory Intelligence API.

## Before you begin

Role required: admin

## About this task

The 3E regulatory intelligence integration uses OAuth 2.0 client credentials to authenticate with the 3E API. The 3E Regulatory Credentials record references an OAuth entity profile that stores the **Client ID** and **Client Secret** from your 3E subscription. An OAuth access token must be obtained and validated before regulatory list retrieval can function. If the token expires, a banner notification on the credential record prompts you to request a new one. For more information on connections, credentials, and aliases, see [Explore credentials, connections, and aliases](https://www.servicenow.com/docs/access?context=credentials-connections-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US). For more information on configuring 3E regulatory application registry, see [Configure the application registry for 3E Regulatory Intelligence](hs-configure-app-register-3e-reg-intelligence.md).

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections and Credential Aliases**.

2.  Open the **3E Regulatory Credentials** \[sn\_hs\_spoke\_3e.3E\_Credentials\] record.

3.  In the **Credentials** column, open the **3E Regulatory Credentials** record.

4.  Verify that the **OAuth Entity Profile** field references the correct profile for your 3E Regulatory Intelligence subscription.

5.  Under **Related Links**, select **Get OAuth Token**.

    The system contacts the 3E authorization server using the **Client ID** and **Client Secret** stored in the OAuth Entity Profile and retrieves an access token. The token refreshes automatically on subsequent syncs.


## What to do next

-   Verify the configuration by navigating to a chemical substance record and triggering a Sync regulatory list. For more information, see [Sync regulatory list regulations for a chemical substance](hs-sync-regulatory-list-chemical-substance.md).
-   A successful sync populates the Regulatory tab with regulations fetched from the 3E server. If the sync fails, verify that the OAuth Entity Profile is configured correctly with valid 3E subscription credentials.

**Parent Topic:**[3E Regulatory Intelligence](../concept/hs-3e-regulatory-intelligence.md)

