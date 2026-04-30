---
title: Configure the SharePoint Graph Root Site Subscription connection and credential alias record
description: Integrate the ServiceNow instance and Microsoft SharePoint Online by creating a custom OAuth application in Microsoft SharePoint Online to authenticate ServiceNow requests.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Microsoft SharePoint Online Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Configure the SharePoint Graph Root Site Subscription connection and credential alias record

Integrate the ServiceNow instance and Microsoft SharePoint Online by creating a custom OAuth application in Microsoft SharePoint Online to authenticate ServiceNow requests.

## Before you begin

-   Request Integration Hub subscription
-   Activate Microsoft SharePoint Online spoke
-   Role required: admin

## About this task

If you intend to use the Create Root Site Subscription action and configure **SharePointGraphRootSiteSubscription** connection and credential alias record, you must create another tenant.

## Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connections &amp; Credential Aliases**.

2.  Open the record, **SharePointGraphRootSiteSubscription**.

3.  Click the **Create New Connection &amp; Credential** related link.

4.  On the form, fill these details.

    |Field|Description|
    |-----|-----------|
    |OAuth Entity Name|Name to identify the OAuth application registry record.|
    |OAuth Client ID|Client ID in this format: `<ClientID>@<TenantID>`.|
    |OAuth Client Secret|Client Secret you created during the Microsoft SharePoint Online account configuration.|
    |OAuth Token URL|Token URL in this format: `https://login.microsoftonline.com/<tenant-id>/oauth2/v2.0/token`|

    **Note:** You may change default values as per your requirement.

5.  Click **Create and Get OAuth Token**.


