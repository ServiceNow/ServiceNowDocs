---
title: Configure Content Service setup using AI
description: Use the AI conversational experience to opt in to the Software Asset Management Content Service. The AI conversational experience walks you through the opt-in decision, the software asset data types that you share with ServiceNow, and the confirmation of your choices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/configure-content-service-otto.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure SAM using AI, Configure SAM using Configuration Console, Configuration Console for Software Asset Management, Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Configure Content Service setup using AI

Use the AI conversational experience to opt in to the Software Asset Management Content Service. The AI conversational experience walks you through the opt-in decision, the software asset data types that you share with ServiceNow, and the confirmation of your choices.

## Before you begin

-   The Software Asset Management application must be installed on your ServiceNow instance. For details, see [Install Software Asset Management from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-sam-product-hub.md).
-   The ServiceNow Otto for Software Asset Management \(SAM\) application must be installed on your ServiceNow instance. For details, see [Install ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-now-assist-sam.md).
-   The ServiceNow Otto panel must be enabled on your ServiceNow instance. For details, see [Enable the ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-enable-now-assist-panel.md).
-   AI Search must be activated on your ServiceNow instance. For details, see the AI Search activation steps in [Install ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/install-now-assist-sam.md).

Role required: sam\_admin and sn\_ia\_config.ia\_user

## About this task

The Content Service setup item helps your organization share raw software installation data with ServiceNow®. In return, the Content Service supplies updates to the Normalization Library so that your instance receives improved normalization and content coverage.

## Procedure

1.  Navigate to **Admin** &gt; **Admin Home**.

2.  In the **Manage your products** section of the Admin Home page, select the **Software Asset Management** tile to open the Product Hub.

3.  In the Configure your product section, select **Configure**.

4.  Navigate to **Software foundations** &gt; **Content service setup**.

    The Content service setup page opens with the **Otto automation available** badge.

5.  Select **Configure with AI** in the header of the Configuration Console.

    ServiceNow Otto opens as a side panel and starts the Otto-guided flow for Content service setup.

6.  Review the summary of the Software Asset Management Content Service in ServiceNow Otto and to opt in and select **Yes**.

    ServiceNow Otto opts your company in to the Content Service and lists the default software asset data types.

7.  Select one of the following options for the additional services.

    -   **Accept all**: Opt in to all the additional services.
    -   **Skip**: Skip all the additional services.
    -   Select the individual service name to opt in that specific service.
8.  When the AI assistant asks whether to mark the step as configured, select one of the following options:

    -   **Mark as configured**: Mark the step as complete immediately.
    -   **Mark later**: Mark the step as complete later and return to the Configuration Console to complete this action manually.
    The Configuration Summary page updates the setup status to reflect the completed item.


**Parent Topic:**[Configure Software Asset Management using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)

**Related topics**  


[Configure Software Asset Management using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)

