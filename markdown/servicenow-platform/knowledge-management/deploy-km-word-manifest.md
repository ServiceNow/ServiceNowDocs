---
title: Deploy Knowledge Management - Add-in for Microsoft Word
description: Deploy the Knowledge Management - Add-in for Microsoft Word for authoring knowledge articles from within the Microsoft Word.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/knowledge-management/deploy-km-word-manifest.html
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Knowledge Management - Add-in for Microsoft Word, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Deploy Knowledge Management - Add-in for Microsoft Word

Deploy the Knowledge Management - Add-in for Microsoft Word for authoring knowledge articles from within the Microsoft Word.

## Before you begin

In addition to having one of the following roles on the ServiceNow instance, you must be an Office365 administrator to deploy the Knowledge Management - Add-in for Microsoft Word.

Role required: admin, sn\_outlook\_addin.outlook\_addin\_setup

## Procedure

1.  Navigate to **All** &gt; **ServiceNow Add-Ins for Office** &gt; **Office Add-In-Manifests**.

2.  In the **Add-In Name** column, select **Knowledge Management**.

3.  Select **Download Manifest** to download the add-in manifest file to your desktop.

4.  Open your email account in Microsoft Outlook.

5.  On the ribbon, select **Get Add-ins** &gt; **My add-ins** &gt; **Add a custom add-in** &gt; **Add from file**.

6.  Select the `manifest.xml` file that you downloaded.

7.  Select **Open**.

8.  Select **Install**.

    The **ServiceNow for Knowledge Management** tile is added in the custom add-ins section.

9.  From the more items menu, select **ServiceNow for Knowledge Management**, and log in with your credentials.

    You can connect to your Microsoft Outlook account with your instance.


**Related topics**  


[Import a Word document to a knowledge base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/import-word-platform.md)

[Import a Word document to a knowledge base using Knowledge Management v3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/t_ImportADocument.md)

