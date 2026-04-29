---
title: Configure Adobe Experience Manager as a Cloud Service for external content indexing
description: Create Service Credentials in Adobe Cloud Manager to allow the Adobe Experience Manager as a Cloud Service external content connector to access nodes and assets in your source system.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Adobe Experience Manager as a Cloud Service external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure Adobe Experience Manager as a Cloud Service for external content indexing

Create Service Credentials in Adobe Cloud Manager to allow the Adobe Experience Manager as a Cloud Service external content connector to access nodes and assets in your source system.

## Before you begin

You need an Adobe Cloud Manager account with Adobe IMS Org administrator privileges. This account must be a member of the **AEM Administrators** IMS Product Profile on **AEM Author**. The **AEM Assets API Users service** option must be selected for the **AEM Administrators** IMS Product Profile.

Role required: none

## About this task

The Adobe Experience Manager as a Cloud Service external content connector retrieves assets from nodes in your Adobe Experience Manager as a Cloud Service source system.

To allow the connector to access your Adobe Experience Manager as a Cloud Service source system, you must create a Technical Account in Adobe Cloud Manager. Your connector admin can use the Service Credentials from this Technical Account to configure the Adobe Experience Manager as a Cloud Service external connector for proper connection to your source system.

## Procedure

1.  Create a Technical Account in Adobe Cloud Manager.

    1.  Log in to [https://my.cloudmanager.adobe.com/](https://my.cloudmanager.adobe.com/) with your Adobe IMS Org administrator credentials.

    2.  In the My Programs console, select the Program that contains the Adobe Experience Manager as a Cloud Service environment you want the connector to access.

    3.  Navigate to **…** &gt; **Developer Console**.

    4.  Select the **Integrations** tab, then select the **Technical Accounts** tab.

    5.  Select **Create new technical account**.

    Adobe Cloud Manager creates your new Technical Account and initializes its Service Credentials.

2.  Download the Service Credentials for your new Technical Account as a JSON-format file.

    1.  On the Technical Accounts tab, select the arrow icon to expand the private key entry for your new Technical Account.

        The private key name varies. As an example, the private key entry name for your new Technical Account might be `PRIVATE-KEY-1873000081275`.

    2.  In the expanded private key entry, select the **…** &gt; **View** link for the private key.

        Adobe Cloud Manager displays the Service Credentials JSON for your new Technical Account.

    3.  In the displayed Service Credentials, select the download icon ![](../image/adobe-cloud-manager-download-icon.png).

    4.  When prompted, download the JSON-format Service Credentials file to a secure location.

        **Important:** Your external content connector admin needs this JSON-format Service Credentials file when configuring the Adobe Experience Manager as a Cloud Service external content connector.


## What to do next

Provide the following items to your connector admin:

-   The hostname for your Adobe Experience Manager as a Cloud Service tenant.

    **Note:** As an example, if the URL for your tenant is `https://example.adobeaemcloud.com`, your tenant hostname is `example`.

-   The JSON-format Service Credentials file that you copied in step [2.d](configure-adobe-expmgr-cs-external-content-indexing.md#download-json-creds-step).

Your connector admin needs these items to configure an Adobe Experience Manager as a Cloud Service external content connector to retrieve assets from your Adobe Experience Manager as a Cloud Service source system.

For details on creating and configuring an Adobe Experience Manager as a Cloud Service external content connector, see [Create an Adobe Experience Manager as a Cloud Service external content connector](create-ext-cont-connector-adobe-expmgr-cs.md).

**Parent Topic:**[Adobe Experience Manager as a Cloud Service external content connector](../concept/adobe-expmgr-cs-external-content-connector.md)

