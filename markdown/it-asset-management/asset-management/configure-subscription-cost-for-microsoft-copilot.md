---
title: Configure Subscription Cost for Microsoft Copilot
description: Configure monthly cost per seat for Copilot.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/asset-management/configure-subscription-cost-for-microsoft-copilot.html
release: australia
product: Asset Management
classification: asset-management
topic_type: task
last_updated: "2026-10-19"
reading_time_minutes: 1
breadcrumb: [Add a Microsoft Copilot integration, Integrating with AI providers, Configure, AI Cost Management, IT Asset Management, Asset Management]
---

# Configure Subscription Cost for Microsoft Copilot

Configure monthly cost per seat for Copilot.

## Before you begin

You must have created an integration with Microsoft Copilot. See [Configure Microsoft Copilot integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/configure-microsoft-copilot-integration.md) for more information.

Role required: ai\_cost\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Cost Management** &gt; **Home**.

2.  Navigate to **Settings** &gt; **Subscription costs**.

    The **Subscription costs** view shows all Copilot account integrations you have configured, with data populated from the initial connection to Copilot.

3.  Select the account to configure.

4.  In the **Edit subscription cost** window, enter the monthly cost per seat.

    The account now displays the cost per seat.


## Result

After you have entered the seat cost information, the AI Cost Management application begins aggregating and storing the seat cost and usage data from Copilot.

The Integrations page updates to show the status of importing usage data and user spend limits. Each time the import happens, this page updates to reflect the status of the last import as one of the following:

-   **In progress**: The import is currently happening.
-   **Success**: All imports are successful. When an import is successful, the timestamp updates to reflect the last successful sync.
-   **Error**: All imports failed.
-   **Partial success**: A portion of the imports failed.

Use the **Logs** link to view import logs. You can also check application logs for more information.

Track and monitor your spend and usage based on the data that you retrieve through the integration. For more details, see [View your AI spend and usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/view-ai-usage-spend.md).

**Note:** If you later want to modify the cost per seat, select the Edit icon next to the account name in the list of subscription costs. In the Edit subscription cost window, enter the new monthly cost per seat and then select **Update**. The changes will be reflected in the next 24 hours.

