---
title: Configure OAuth authentication for the 3E Protect API
description: Configures the 3E Credentials record and obtains the OAuth access token required to authenticate with the 3E Protect API.
locale: en-US
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [3E Protect, 3E, Integration with third-party services, Health and Safety, Employee Service Management]
---

# Configure OAuth authentication for the 3E Protect API

Configures the 3E Credentials record and obtains the OAuth access token required to authenticate with the 3E Protect API.

## Before you begin

Role required: admin

## About this task

The 3E Protect integration uses OAuth 2.0 client credentials to authenticate with the 3E API. The 3E Credentials record references an OAuth Entity Profile that stores the client ID and secret from your 3E subscription. An OAuth access token must be obtained and validated before SDS retrieval and chemical data requests can function. If the token expires before an automatic refresh occurs, a banner notification on the credential record prompts you to request a new one. For more information on configuring 3E Protect application registry, [Configure the application registry for the 3E service provider](../../hs-environmental-management/task/hs-configure-application-registry-3E.md).

## Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Connections and Credential Aliases**.

2.  Open the **3E Credentials** \[sn\_hs\_spoke\_3e.3E\_Credentials\] record.

3.  In the **Credentials** column, open the **3E Credentials** record.

4.  Verify that the **OAuth Entity Profile** field references the correct profile for your 3E Regulatory Intelligence subscription.

5.  Under **Related Links**, select **Get OAuth Token**.

    The system contacts the 3E authorization server using the client ID and secret stored in the OAuth Entity Profile and retrieves an access token. The token refreshes automatically on subsequent syncs.


## What to do next

-   Verify the configuration by navigating to a chemical record and triggering an sync request. For more information, see [Sync chemical information with the 3E database](../../hs-environmental-management/task/hs-sync-chemical-data-with-3E.md).
-   A successful request populates the chemical record with hazard identification, ingredient data, and SDS documents retrieved from the 3E server. If the request fails, verify that the OAuth Entity Profile is configured correctly with valid 3E subscription credentials.

**Parent Topic:**[3E Protect](../concept/hs-3e-protect.md)

