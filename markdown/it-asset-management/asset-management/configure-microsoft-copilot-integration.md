---
title: Configure Microsoft Copilot integration
description: Integrate with a Copilot account to import usage data from Copilot.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/configure-microsoft-copilot-integration.html
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-10-19"
reading_time_minutes: 1
breadcrumb: [Add a Microsoft Copilot integration, Integrating with AI providers, Configure, AI Cost Management, IT Asset Management, Asset Management]
---

# Configure Microsoft Copilot integration

Integrate with a Copilot account to import usage data from Copilot.

## Before you begin

You must have the following from Copilot to create the integration:

-   Copilot Tenant ID
-   Copilot Client ID
-   Copilot Client secret

Role required: ai\_cost\_admin

## About this task

Create an integration for each Copilot account that you want to monitor.

## Procedure

1.  Navigate to **All** &gt; **AI Cost Management** &gt; **Home**.

2.  From the navigation panel of the AI Cost Management application, navigate to **Settings** &gt; **Integrations**.

3.  Select **Add integration** and then select **Copilot**.

4.  In the Add Microsoft Copilot account window, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Name**|Name of the Copilot account to use for the integration. You can use any name, but using the same account name as your Copilot account makes reconciling records between Copilot and AI Cost Management easier.|
    |**Tenant ID**|The Copilot tenant ID used for this account.|
    |**Client ID**|Copilot client ID associated with this account.|
    |**Client Secret**|Copilot client secret associated with the client ID.|

5.  Select **Add**.


## Result

The integration is added to the list of available integrations. After the integration successfully connects, the AI Cost Management application begins retrieving the user and seat data from Copilot for the configured account.

## What to do next

You now must configure seat cost information. See [Configure Subscription Cost for Microsoft Copilot](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/configure-subscription-cost-for-microsoft-copilot.md).

**Note:** If you later want to modify any details of the existing integration, select the Edit icon \(\[Omitted image "edit-icon-task-settings-page.png"\]\) next to the account name in the list of available integrations. In the Edit Microsoft Copilot account window, modify the integration details as needed and then select **Update**. You can only modify the name, Client ID, and Client secret. If you want to use a different tenant name, you must create an additional integration.

