---
title: Opt-in to the Hardware Asset Management Content Service
description: Opt in to the Hardware Asset Management Content Service to improve the normalization process by sharing hardware and consumable model data from your organization with ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/opt-in-hardware-normalization.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Opt-in to the Hardware Asset Management Content Service

Opt in to the Hardware Asset Management Content Service to improve the normalization process by sharing hardware and consumable model data from your organization with ServiceNow.

## Before you begin

Role required:

-   ham\_admin: for non domain separated instance
-   ham\_admin plus domain\_admin: for domain separated instance

## About this task

By opting in to the Hardware Asset Management Content Service, your data is securely shared with ServiceNow to build the content service repository. Adding to the content service allows more models be normalized automatically. These updates occur weekly.

The content updates are based on data from the hardware and consumable models, lifecycles, and custom hardware product models sent back to the Hardware Asset Management Content Service.

Any data that is retrieved by the content service remains anonymous and secure, following ServiceNow privacy policies. After the data has been reviewed, it is properly disposed of.

## Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Administration** &gt; **Hardware Model Normalization** &gt; **Content Service Setup**.

2.  Read the Hardware Asset Management Content Service agreement.

3.  Select **Yes, I have read and accept the Opt-In Agreement**.

4.  Click **Opt-in**.

5.  If there is any hardware model, consumable model, or lifecycle data that you want to exclude, toggle the option on the Content Service Setup form.

6.  Click **Save**.


## Opt-in to the Hardware Asset Management Content Service

Your organization has decided to enable the Hardware Asset Management Content Service.

Navigate to the Content Service Setup module and review the Hardware Asset Management Content Service agreement.

\[Omitted image "hardware-normalization-content-service.png"\] Alt text: Hardware Asset Management Content Service agreement

Select **Yes, I have read and accept the Opt-In Agreement** to display the Content Service Setup page.

You decide that you don't want to send hardware model data to the Hardware Asset Management Content Service. Toggle the button next to Hardware Models to opt out of sending the hardware model asset data.

\[Omitted image "opt-out-hardware-model.png"\] Alt text: Opt-out of sending hardware model asset data to the Hardware Asset Management Content Service.

Click **Save**.

Your organization has decided that they don't want to send any of their data and they want to opt-out of the Hardware Asset Management Content Service. To stop sending your data, toggle all the buttons off.

A message appears verifying that you want to opt-out of using the Hardware Asset Management Content Service.

\[Omitted image "content-service-opt-out.png"\] Alt text: Hardware Asset Management Content Service opt-out message

Click **Opt-Out**.

You are returned to the Hardware Asset Management Content Service agreement and you can opt back in at anytime.

-   **[Import and export content data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/import-export-ham.md)**  
Import content data from or export content data to the Hardware Asset Management content library service to support hardware normalization of asset models. On-premise users can import or export data via a zip file using the Manage Hardware Library module.

**Parent Topic:**[Configuring Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/configuring-ham.md)

