---
title: Microsoft Exchange Online setup for Journey Accelerator
description: By integrating the Journey Accelerator scheduling feature with the Microsoft Office 365 calendar function, users can schedule plans and to-do tasks.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
---

# Microsoft Exchange Online setup for Journey Accelerator

By integrating the Journey Accelerator scheduling feature with the Microsoft Office 365 calendar function, users can schedule plans and to-do tasks.

**Note:** If an administrator intends to use the Microsoft Office 365 scheduling capabilities with Journey Accelerator, the administrator must install and configure the related Microsoft plugins and integrations before installing Journey Accelerator.

The Journey Accelerator scheduling feature enables users to schedule Microsoft Office 365 calendar events directly from Journey Accelerator plans and to-do tasks.

If you plan to use the scheduling feature, you must install and configure these plugins and integrations before you install Journey Accelerator. The embedded scheduling feature includes all plugins, integration APIs, and actions.

Some integrations and related plugins require activation by ServiceNow® personnel. Journey Accelerator uses an embedded Microsoft Exchange Online spoke with limitations for use with Journey Accelerator. The use beyond these embedded limitations may require that you get additional licensing or subscriptions.

## Journey Accelerator v2

-   **[Microsoft AD Spoke](https://www.servicenow.com/docs/access?context=microsoft-ad-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) \[com.sn.ad.spoke\]**

    Provides communication between Journey Accelerator and Microsoft Active Directory to manage objects such as users, groups, and computers.

-   **[Microsoft Azure AD spoke](https://www.servicenow.com/docs/access?context=microsoft-azure-ad-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US) \[com.sn.azure\_ad.spoke\]**

    Provides security requirements to Journey Accelerator so that users, security groups, and office groups are appropriately managed.

-   **Microsoft Exchange Online spoke v2.0.1 \[sn\_ex\_online\_spke\]**

    The Microsoft Exchange Online spoke enables creation and management of calendar events and mail in Microsoft Exchange Online.


## Journey Accelerator v3 and later

-   **Microsoft Exchange Online Spoke V3.0.0**

    The Microsoft Exchange Online spoke enables creation and management of calendar events and mail in Microsoft Exchange Online.

-   **Retry Handler Framework**

    Framework that retries a failed HTTP request when the API rate limits are exceeded and the 429 Too Many Requests status code is returned. The retry-after time HTTP header is used to retry the request again after that specified retry-after time.


## Set these Journey Accelerator system properties

Follow the instructions for setting up the spokes respective to your Journey Accelerator version. After spoke setup is complete, navigate to **sys\_properties.list** in ServiceNow and set up the following properties for the Journey Accelerator app.

-   sn\_ja.calendar\_provider\_option: Select exchangeOnline
-   sn\_ja.ex\_online\_dummy\_account\_id: Insert `<outlook dummy account for querying meeting times>`
-   sn\_ja.ex\_online\_service\_account\_id: Insert `<outlook service account or delegator for calendar management>`
-   sn\_ja.ex\_online\_notification\_url: Insert `<webhook URL from Microsoft Exchange Online Spoke>`

**Note:** When using Microsoft Exchange Online spoke v.2.0.2 with Retry Handler Framework, the scripted rest API for the retry handler framework is used as the webhook URL.

For detailed steps, see [Update system properties for Microsoft Exchange Online in the Journey Accelerator app](../task/ja-update-system-properties-1.md)

**Parent Topic:**[Journey Accelerator integrations](ja-integrations.md)

**Related topics**  


[Request IntegrationHub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)

