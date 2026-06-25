---
title: Configure CRM access from Microsoft Outlook
description: Download and install the ServiceNow CRM for Outlook add-in to access and manage CRM records directly from your Microsoft Outlook inbox, eliminating the need to switch between applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/add-crm-outlook-add-in.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activity Management, Lead and opportunity management apps, Configure, Sales Customer Relationship Management]
---

# Configure CRM access from Microsoft Outlook

Download and install the ServiceNow CRM for Outlook add-in to access and manage CRM records directly from your Microsoft Outlook inbox, eliminating the need to switch between applications.

## Before you begin

The CRM Outlook Add-in must be installed on your ServiceNow instance. For more information, see [Install CRM Outlook Add-in](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/install-crm-outlook-add-in.md).

Role required: sn\_crm\_outlook.crm\_outlook\_admin

## About this task

This procedure describes how to install the ServiceNow CRM for Outlook add-in on your Microsoft Outlook client. For information about how to deploy and centrally manage the add-in across your organization, refer to the Microsoft Outlook product documentation on deploying and publishing Office add-ins.

## Procedure

1.  Log in to your ServiceNow instance.

2.  Download the manifest file.

    1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-in Manifests**.

    2.  Select **ServiceNow CRM for Outlook** from the list.

    3.  Download the file on your computer by selecting **Download Manifest**.

        You can also provide the `manifest.xml` file to your agents so they can install the add-in to their Microsoft Outlook clients.

3.  Install the ServiceNow CRM for Outlook add-in on your Microsoft Outlook client.

    1.  Open your Microsoft Outlook client.

    2.  On the Microsoft Outlook client, select the See more items icon \[Omitted image "ellipsis-horizontal-fill-24.svg"\] Alt text: and select **Get Add-ins**.

    3.  Navigate to **My add-ins** &gt; **Custom Addins**.

    4.  From the **Add a custom add-in** drop-down menu, select **Add from File**.

    5.  Browse to and select the manifest file.

    6.  Review the warning and select **Install**.

        The ServiceNow CRM for Outlook add-in is installed and available in your Microsoft Outlook client.


## What to do next

Log in to the ServiceNow CRM for Outlook add-in to start using it.

**Related topics**  


[Using Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-activity-management.md)

[Activity Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-activity-management.md)

